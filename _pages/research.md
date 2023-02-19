---
layout: page
title: research
permalink: /projects/
description: 
nav: true
nav_order: 2
display_categories: [Gender&IPE, Corporate Social Responsibility in IR]
horizontal: false
---

# Research Question 

How does economic globalization affect workers’ experiences in the domestic labor market, and how do their perceptions of globalization shape their attitudes toward economic policy? I investigate the linkages between economic globalization and workers’ experiences in the domestic labor market, with a special focus on the political consequences of economic and gender inequality in the labor market. I use computational methods, such as text analysis, survey experiments, and causal inference methods to test my claims.

# Dissertation 

My dissertation focuses on firms' and workers' responses to economic globalization and the diffusion of socially responsible norms. To assess these relationships, I employ a multimethod approach by combining natural language processing (NLP) and causal inference methods.

## Three Essays on the International Trade and the Domestic Labor Market

### Protectionism Reconsidered: Economic Insecurity, Social Identity, and the Gender Gap in Trade Attitudes

Using decomposition analysis, a survey experiment, and structural topic models, I examine how economic insecurity, such as the experience of gender discrimination for women and trade shocks for men, explains the gender gap in trade attitudes. 

### Obfuscating Social Responsibility: Global Performance Indicators and Labor Upgrading in Global Production Networks  

Employing the difference-in-differences method, I investigate how Global Performance Indicators (GPIs) induce firms' compliance by obfuscation in supply chains and its impacts on workers' experiences in the labor market.

### Measuring Women’s Economic Rights 

I create a new measure to capture the latent heterogeneity of gender inequality in the labor market. 



<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
