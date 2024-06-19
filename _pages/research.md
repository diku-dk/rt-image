---
layout: page
title: Research
permalink: /research/
---

<section id="research">
    {% for project in site.data.projects %}
    <div class="project">
        <h3>{{ project.title }}</h3>
        <p>{{ project.description | markdownify }}</p>
    </div>
    {% endfor %}
</section>
