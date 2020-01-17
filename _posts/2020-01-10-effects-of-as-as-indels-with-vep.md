---
layout: post
title: Predicting the effects of alternative splicing events with VEP
description: How to predict the effects of alternative splicing events with the Ensembl Variant Effect Predictor (VEP), by encoding them as indels
categories: science
tags: science
---

This post *is a stub*.

How to predict the effects of alternative splicing (AS) events with the **[Ensembl Variant Effect Predictor](https://www.ensembl.org/info/docs/tools/vep/index.html)** (VEP), by encoding them as indels? 

Here's how we did it in our recent paper:

> [A unicellular relative of animals generates a layer of polarized cells by actomyosin-dependent cellularization](https://elifesciences.org/articles/49801){:target="_blank"} (Dudin et al., eLife 2019)

First, load an `ioe` file generated with [**SUPPA2**](https://genomebiology.biomedcentral.com/track/pdf/10.1186/s13059-018-1417-1), that contains all AS events

```R
ioe = read.table("input_file_from_suppa.ioe", header = T)
iot = ioe[ioe$seqname!="seqname",]
...
```

Encode AS events as indels and save as `csv` for later use in VEP:

```R
psi = data.frame(
  seqname=iot$seqname,
  in_start=NA,
  in_end=NA,
  string=NA,
  in_strand=iot$ev_strand,
  event_id=iot$event_id
)


# SE: codified as deletion (XXX/-) that starts and ends where the exon should be
acceptable = iot$ev_type == "SE"
psi[acceptable,]$in_start  = iot[acceptable,]$ev_start
psi[acceptable,]$in_end    = iot[acceptable,]$ev_end
psi[acceptable,]$string    = paste(
  as.vector(subseq(x=    fi[psi[acceptable,]$seqname],
                   start=psi[acceptable,]$in_start,
                   end=  psi[acceptable,]$in_end)),
  "/-",
  sep=""
)
psi[acceptable,]$string    = paste(psi[acceptable,]$string,"/-",sep="")


# RI, A3, A5: codified as insertions (-/XXX) that start 
# at ev_start-1, and end at ev_start (reversed format!)
acceptable = 
  iot$ev_type == "RI" | 
  iot$ev_type == "A3" | 
  iot$ev_type == "A5"

psi[acceptable,]$in_start  = iot[acceptable,]$ev_start+2
psi[acceptable,]$in_end    = iot[acceptable,]$ev_start+1
psi[acceptable,]$string    = paste(
  "-/",
  as.vector(subseq(x =   fi[psi[acceptable,]$seqname],
                   start=iot[acceptable,]$ev_start,
                   end=  iot[acceptable,]$ev_end-1)),
  sep=""
)


# MX, AF, AL: codified as complex events (YY/XXX) that start 
# at ev_start-1, and end at ev_start (like insertions - reversed!)
acceptable = 
  iot$ev_type == "MX" | 
  iot$ev_type == "AF" | 
  iot$ev_type == "AL"

psi[acceptable,]$in_start  = iot[acceptable,]$ev_start+1
psi[acceptable,]$in_end    = iot[acceptable,]$ev_start
psi[acceptable,]$string    = paste(
  "-/",
  as.vector(subseq(x =   fi[psi[acceptable,]$seqname],
                   start=iot[acceptable,]$ev_start,
                   end=  iot[acceptable,]$ev_end)),
  "/",
  as.vector(subseq(x =   fi[psi[acceptable,]$seqname],
                   start=iot[acceptable,]$ev_startB,
                   end=  iot[acceptable,]$ev_endB)),
  sep=""
)


# format VEP pseudoindel file
psi = na.omit(psi)
write.table(psi,file="as_as_indels.csv", row.names = F,col.names = F, quote = F, sep = "\t")


```

Use the `as_as_indels.csv` file as input for VEP.

```bash
...
```

Bon profit!
