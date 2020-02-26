---
layout: misc
title: Intro
---

## About me

<img align="left" width="143" height="143" src="/assets/img/perfil_original.png">

I am a Post Doctoral Research Associate at the Vector Biology department of the [Liverpool School of Tropical Medicine](https://www.lstmed.ac.uk/about/people/dr-xavier-grau-bov%C3%A9){:target="_blank"}, with [David Weetman](https://www.lstmed.ac.uk/about/people/dr-david-weetman){:target="_blank"} and [Martin Donnelly](https://www.lstmed.ac.uk/about/people/professor-martin-james-donnelly){:target="_blank"}.

I am currently working on the evolution of insecticide resistance adaptations in *Anopheles* mosquitoes responsible for malaria transmission as part of the [*Anopheles gambiae* 1000 Genomes project](https://www.malariagen.net/projects/ag1000g){:target="_blank"} and MalariaGEN.

In the past, I have worked with [Iñaki Ruiz-Trillo](http://multicellgenome.com/){:target="_blank"} studying the origin of [multicellularity in animals](https://www.sciencemag.org/news/2018/06/momentous-transition-multicellular-life-may-not-have-been-so-hard-after-all){:target="_blank"}, using comparative genomic analyses of animals and their unicellular relatives. You can learn more about this in my favourite publications from my thesis:

* [Dynamics of genomic innovation in the unicellular ancestry of animals](https://elifesciences.org/articles/26036){:target="_blank"} (Grau-Bové *et al.* eLife 2017)

<img width="200" src="/assets/img/microsynteny-climcowc.png">

* [Origin of exon skipping-rich transcriptomes in animals driven by evolution of gene architecture](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-018-1499-9){:target="_blank"} (Grau-Bové *et al.* Genome Biology 2018), which I talked about in [this post](_posts/2018-09-18-the-evolution-of-alternative-splicing-in-eukaryotes-and-the-animal-revolution.md).

<img align="centre" width="200" src="/assets/img/asfig.png">

Starting in 2020, I will join the [lab of Arnau Sebé-Pedrós](https://www.crg.eu/en/programmes-groups/sebe-pedros-lab){:target="_blank"} in the [Centre de Regulació Genòmica](https://www.crg.cat/){:target="_blank"}, in Barcelona.

## Recent posts

From [my blog](/pages/blog.html):

{% for post in site.categories.science limit:4 %}

**[{{ post.title }}]({{ post.url }})**, , {% assign d = post.date | date: "%-d" %} {{ post.date | date: "%B" }} {% case d %} {% when '1' or '21' or '31' %}{{ d }}st {% when '2' or '22' %}{{ d }}nd {% when '3' or '23' %}{{ d }}rd {% else %}{{ d }}th{% endcase %}, {{ post.date | date: "%Y" }}

> {{ post.excerpt }}

{% endfor %}
