---
layout: misc
title: Intro
---

## About me

<img align="left" width="120" height="120" src="/assets/img/perfil_original.png" alt="Profile pic" class="circular-square">

I am a Post Doctoral Research Associate at the [Centre de Regulació Genòmica](https://www.crg.cat/){:target="_blank"} in Barcelona, working in the [Comparative Regulatory Genomics lab](https://www.sebepedroslab.org/){:target="_blank"}. We use comparative genomics and transcriptomics to investigate the evolutionary dynamics of genome regulation and cell type diversity across the eukaryotic tree of life — from animals to protists.

Our latest work includes a transcriptomic reconstruction of the [early evolutionary origin of animal neurons](https://www.cell.com/cell/fulltext/S0092-8674(23)00917-0){:target="_blank"} using single-cell atlases of four placozoans and a [phylogenetic investigation of chromatin evolution in eukaryotes](https://www.nature.com/articles/s41559-022-01771-6){:target="_blank"} combining comparative genomics and proteomics.

[<img width="200" src="/assets/img/cover.tif.jpg" alt="Cell cover 12oct23" align="center">](https://www.cell.com/cell/fulltext/S0092-8674(23)00917-0){:target="_blank"}

I have also released [*Possvm*](https://github.com/xgrau/possvm-orthology/){:target="_blank"}, a handy piece of software that can identify and annotate clusters of orthologous genes directly from phylogenetic trees.

[<img width="200" src="/assets/img/possvm-logo.png" alt="Possvm logo" align="center">](https://github.com/xgrau/possvm-orthology/){:target="_blank"}

In the past, I worked with [David Weetman](https://www.lstmed.ac.uk/about/people/dr-david-weetman){:target="_blank"} at the [Liverpool School of Tropical Medicine](https://www.lstmed.ac.uk){:target="_blank"}, studying the evolution of insecticide resistance adaptations in *Anopheles* mosquitoes responsible for malaria transmission as part of the [*Anopheles gambiae* 1000 Genomes project](https://www.malariagen.net/project/ag1000g/){:target="_blank"} within [MalariaGEN](https://www.malariagen.net/).

<img align="center" width="200" src="/assets/img/phylo-agam.png">

I obtained my PhD from the University of Barcelona in 2017, under the supervision of [Iñaki Ruiz-Trillo](http://multicellgenome.com/){:target="_blank"}, investigating the origin of [multicellularity in animals](https://www.sciencemag.org/news/2018/06/momentous-transition-multicellular-life-may-not-have-been-so-hard-after-all){:target="_blank"} using comparative genomic analyses of animals and their unicellular relatives. You can learn more about this in my favourite publications from my thesis:

* [Dynamics of genomic innovation in the unicellular ancestry of animals](https://elifesciences.org/articles/26036){:target="_blank"} (Grau-Bové *et al.* eLife 2017)

[<img width="180" src="/assets/img/microsynteny-climcowc.png">](https://elifesciences.org/articles/26036){:target="_blank"}

* [Origin of exon skipping-rich transcriptomes in animals driven by evolution of gene architecture](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-018-1499-9){:target="_blank"} (Grau-Bové *et al.* Genome Biology 2018), which I talked about in [this post](_posts/2018-09-18-the-evolution-of-alternative-splicing-in-eukaryotes-and-the-animal-revolution.md).

[<img align="centre" width="200" src="/assets/img/asfig.png">](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-018-1499-9){:target="_blank"}

## Recent posts

From [my blog](/pages/blog.html):

{% for post in site.categories.science limit:4 %}

#### [{{ post.title }}]({{ post.url }})

<span class="post-date"> {% assign d = post.date | date: "%-d"  %} {{ post.date | date: "%B" }} {% case d %} {% when '1' or '21' or '31' %}{{ d }}st {% when '2' or '22' %}{{ d }}nd {% when '3' or '23' %}{{ d }}rd  {% else %}{{ d }}th{% endcase %}, {{ post.date | date: "%Y" }}, by {% if page.author %} {{ page.author }} {% else %} {{ site.author }} {% endif %} </span>

{{ post.excerpt }}

{% endfor %}

<a rel="me" href="https://ecoevo.social/@xgrau">Mastodon</a>
