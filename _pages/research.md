---
layout: page
title: Research
permalink: /research/
---

<section id="research">
    {% for project in site.data.projects %}
    <div class="project" style="display: flex; align-items: flex-start; margin-bottom: 20px;">
        <div class="project-description" style="flex: 1;">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description | markdownify }}</p>
        </div>
        {% if project.image %}
        <div class="project-image" style="margin-left: 20px;">
            <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" style="max-width: 100%; height: auto;">
            {% if project.image_license %}
            <p style="font-size: 0.8em; margin-top: 5px;">
                {{ project.image_license | markdownify }}
            </p>
            {% endif %}
        </div>
        {% endif %}
    </div>
    {% endfor %}
</section>
