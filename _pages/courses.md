---
layout: page
title: teaching
permalink: /courses/
description: Teaching practice and course materials
nav: true
nav_order: 3
display_categories: [caltech]
horizontal: false
---

My teaching aims to engage students actively with the subject of the course and to generate lasting and meaningful knowledge. I design course activities to be challenging while adapted to the background and level of the students, and feedback plays a fundamental role in that adaptation. Over fifteen years of teaching in Chile, France and the United States, this view has settled into three practices.

* **Students collaborate to solve problems in class.** Some class periods are workshops: students work in groups of two or three on a set of problems; members rotate between groups at regular intervals and disseminate ideas, and I engage directly with each group. The workshop problem sets are on each course page below.
* **The course adapts to the students.** I begin each course with a survey of students' backgrounds, motivations and interests, and I adjust as the term goes. In *Algebraic and Differential Topology*, I rebuilt the course around how its ideas arose from problems in analysis; in *Mathematical Chaos*, students chose the topics of their presentations ([proposed subjects]({{ site.baseurl }}/Ma4/subjects/)).
* **Feedback counts more than grades.** In the 2024 offering of *Probability*, students chose each week which problems to submit, received comments from the teaching assistant and from peers, and wrote a short reflection on their progress; at mid-term and at the end, they assembled a portfolio and proposed their own grade. I used the same approach in *Mathematical Chaos*. I describe it in [An invitation to ungrade]({{ site.baseurl }}/blog/2024/ungrading/), and will present it at the Joint Mathematics Meetings in January 2027.

<!-- pages/projects.md -->
<div class="courses">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.courses | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
 <div class="container">
    <div class="row row-cols-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.html %}
    {% endfor %}
    </div>
  </div> 
  
  {% else %}
  <div class="grid">
    {% for project in sorted_projects %}
      {% include projects.html %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.courses | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.html %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="grid">
    {% for project in sorted_projects %}
      {% include projects.html %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
