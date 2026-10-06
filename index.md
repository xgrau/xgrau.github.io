---
layout: misc
title: Intro
---

## About me

<img align="left" width="120" height="120" src="/assets/img/perfil_original3.png" alt="Profile pic" class="circular-square">

I am a Postdoctoral Fellow and La Caixa-Junior Leader at the [Centre de Regulació Genòmica](https://www.crg.cat/){:target="_blank"} in Barcelona. In [our lab](https://www.sebepedroslab.org/) we use comparative genomics, population genetics and single-cell omics to investigate the evolutionary dynamics of genome regulation and cell type diversity across the eukaryotic tree of life — from animals to protists.

My latest work includes studies on the evolution of environmental resilience in corals, including [the unique facultatively symbiotic lifestyle of the Mediterranean coral *Oculina patagonica*](https://www.nature.com/articles/s41586-025-09623-6), and the dynamics of cell-level [transcriptomic responses to heat stress in *Stylophora pistillata*](https://www.biorxiv.org/content/10.64898/2026.07.18.739195v1){:target="_blank"}. I have also taken a deep dive into the genetic determinants of cell type innovation in animal evolution using using [single-cell transcriptomic atlases of four placozoan species](https://www.cell.com/cell/fulltext/S0092-8674(23)00917-0){:target="_blank"}.

[<img width="300" src="/assets/img/oculina_small.jpg" alt="Partially bleached Oculina patagonica colony" align="center" class="circular-square">](https://xgrau.github.io/science/oculina-coral-atlas.html){:target="_blank"}

I have also released [*Possvm*](https://github.com/xgrau/possvm-orthology/){:target="_blank"}, a handy piece of software that can identify and annotate clusters of orthologous genes directly from phylogenetic trees.

[<img width="200" src="/assets/img/possvm-logo.png" alt="Possvm logo" align="center">](https://github.com/xgrau/possvm-orthology/){:target="_blank"}

In the past, I worked with [David Weetman](https://www.lstmed.ac.uk/about/people/dr-david-weetman){:target="_blank"} at the [Liverpool School of Tropical Medicine](https://www.lstmed.ac.uk){:target="_blank"}, studying the evolution of insecticide resistance adaptations in *Anopheles* mosquitoes responsible for malaria transmission as part of the [*Anopheles gambiae* 1000 Genomes project](https://www.malariagen.net/project/ag1000g/){:target="_blank"}.

[<img align="center" width="200" src="/assets/img/phylo-agam.png">](https://academic.oup.com/mbe/article/37/10/2900/5843798){:target="_blank"}

I obtained my PhD from the University of Barcelona in 2017, under the supervision of [Iñaki Ruiz-Trillo](http://multicellgenome.com/){:target="_blank"}, investigating the origin of [multicellularity in animals](https://www.sciencemag.org/news/2018/06/momentous-transition-multicellular-life-may-not-have-been-so-hard-after-all){:target="_blank"} using comparative genomic analyses of animals and their unicellular relatives.

[<img width="180" src="/assets/img/microsynteny-climcowc.png">](https://elifesciences.org/articles/26036){:target="_blank"}

[<img align="centre" width="200" src="/assets/img/asfig.png">](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-018-1499-9){:target="_blank"}

You can follow my updates in Mastodon (<a rel="me" href="https://ecoevo.social/@xgrau">ecoevo.social/@xgrau</a>) or Bluesky (<a rel="me" href="https://bsky.app/profile/xgrau.bsky.social">xgrau.bsky.social</a>).


## Recent posts

From [my blog](/pages/blog.html):

{% for post in site.categories.science limit:4 %}

#### [{{ post.title }}]({{ post.url }})

<span class="post-date"> {% assign d = post.date | date: "%-d"  %} {{ post.date | date: "%B" }} {% case d %} {% when '1' or '21' or '31' %}{{ d }}st {% when '2' or '22' %}{{ d }}nd {% when '3' or '23' %}{{ d }}rd  {% else %}{{ d }}th{% endcase %}, {{ post.date | date: "%Y" }}, by {% if page.author %} {{ page.author }} {% else %} {{ site.author }} {% endif %} </span>

{{ post.excerpt }}

{% endfor %}
