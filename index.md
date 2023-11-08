---
layout: misc
title: Intro
---

## About me

<img align="left" width="120" height="120" src="/assets/img/perfil_original.png" alt="Profile pic" class="circular-square">

I am a Post Doctoral Research Associate at the [Centre de Regulació Genòmica](https://www.crg.cat/){:target="_blank"} in Barcelona, working with [Arnau Sebé-Pedrós](https://www.sebepedroslab.org/){:target="_blank"}. We use comparative genomics and transcriptomics to investigate the evolutionary dynamics of genome regulation and cell type diversity across the eukaryotic tree of life — from animals to protists.

Our latest work includes our study on the [early evolutionary origin of animal neurons](https://www.cell.com/cell/fulltext/S0092-8674(23)00917-0){:target="_blank"}, using single-cell transcriptomes of four placozoan species; a [phylogenetic investigation of chromatin evolution in eukaryotes](https://www.nature.com/articles/s41559-022-01771-6){:target="_blank"} combining comparative genomics and proteomics; and the release of [*_Possvm_*](https://academic.oup.com/mbe/advance-article/doi/10.1093/molbev/msab234/6342420){:target="_blank"}, a handy piece of software to identify clusters of orthologous sequences from gene trees.

<img align="center" width="240" src="/assets/img/cover.tif.jpg">

In the past, I worked with [David Weetman](https://www.lstmed.ac.uk/about/people/dr-david-weetman){:target="_blank"} at the [Liverpool School of Tropical Medicine](https://www.lstmed.ac.uk/about/people/dr-xavier-grau-bov%C3%A9){:target="_blank"}, studying the evolution of insecticide resistance adaptations in *Anopheles* mosquitoes responsible for malaria transmission as part of the [*Anopheles gambiae* 1000 Genomes project](https://www.malariagen.net/projects/ag1000g){:target="_blank"} and MalariaGEN.


<img align="center" width="200" src="/assets/img/phylo-agam.png">

I obtained my PhD from the University of Barcelona in 2017, under the supervision of [Iñaki Ruiz-Trillo](http://multicellgenome.com/){:target="_blank"}, investigating the origin of [multicellularity in animals](https://www.sciencemag.org/news/2018/06/momentous-transition-multicellular-life-may-not-have-been-so-hard-after-all){:target="_blank"} using comparative genomic analyses of animals and their unicellular relatives. You can learn more about this in my favourite publications from my thesis:

* [Dynamics of genomic innovation in the unicellular ancestry of animals](https://elifesciences.org/articles/26036){:target="_blank"} (Grau-Bové *et al.* eLife 2017)

<img width="180" src="/assets/img/microsynteny-climcowc.png">

* [Origin of exon skipping-rich transcriptomes in animals driven by evolution of gene architecture](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-018-1499-9){:target="_blank"} (Grau-Bové *et al.* Genome Biology 2018), which I talked about in [this post](_posts/2018-09-18-the-evolution-of-alternative-splicing-in-eukaryotes-and-the-animal-revolution.md).

<img align="centre" width="200" src="/assets/img/asfig.png">

## Recent posts

From [my blog](/pages/blog.html):

{% for post in site.categories.science limit:4 %}

#### [{{ post.title }}]({{ post.url }})

<span class="post-date"> {% assign d = post.date | date: "%-d"  %} {{ post.date | date: "%B" }} {% case d %} {% when '1' or '21' or '31' %}{{ d }}st {% when '2' or '22' %}{{ d }}nd {% when '3' or '23' %}{{ d }}rd  {% else %}{{ d }}th{% endcase %}, {{ post.date | date: "%Y" }}, by {% if page.author %} {{ page.author }} {% else %} {{ site.author }} {% endif %} </span>

{{ post.excerpt }}

{% endfor %}

<a rel="me" href="https://ecoevo.social/@xgrau">Mastodon</a>
