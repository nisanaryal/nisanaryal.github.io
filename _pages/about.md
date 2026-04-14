---
layout: about
title: about
permalink: /
subtitle: 

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular


news: false # includes a list of news items
latest_posts: true # includes a list of the newest posts
selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

I am an AI Engineer with experience in Medical AI and Acoustic Scene Classification. My technical background includes classification, detection, segmentation, and time-series analysis. I am also experienced in developing multi-model pipelines, such as detection-based classification and multi-stage inference workflows.

I handle the full development lifecycle, from initial pipeline architecture and annotation strategy to data analysis, model training, and deployment (MLOps).


I am particularly interested in 3D Vision, Generative AI, and Edge AI, with a focus on building high-performance systems for complex real-world environments.


### Featured Projects

<div class="projects">
  {% assign selected_projects = site.projects | where: "selected", "true" %}
  {% for project in selected_projects %}
    {% include projects_horizontal.liquid %}
  {% endfor %}
</div>