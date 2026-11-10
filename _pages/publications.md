---
layout: page
permalink: /publications/
title: publications
description: Papers and preprints, most recent first, with links to the arXiv and published versions, code and slides.
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">

{% bibliography -f {{ site.scholar.mybibliography }} -T bib_publications --group_by year --group_order descending --sort_by year,month --order descending,descending %}

</div>
