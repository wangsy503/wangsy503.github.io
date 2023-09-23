---
layout: about
title: about
permalink: /
subtitle: Full-stack Developer | DevOps Enthusiast
# subtitle: <a href='#'>Affiliations</a>. Address. Contacts. Moto. Etc.

profile:
  align: right
  image: IMG_5820.jpg
  image_circular: true # crops the image to make it circular
  address: >
    <p>Philadelphia, PA 19104</p>

# news: true  # includes a list of news items
latest_posts: true  # includes a list of the newest posts
# selected_papers: true # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
---

Hello! I'm Shuyue Wang, currently pursuing my Master's in [Computer and Information Science](https://www.cis.upenn.edu/graduate/program-offerings/mse-in-cis/) at the University of Pennsylvania, where I've achieved GPA of **4.00**. Before this, I earned my Bachelor's in Computer Science and Technology from [ShanghaiTech University](https://www.shanghaitech.edu.cn/eng/). 

My professional journey has led me to significant roles at renowned institutions like **Wharton Research Data Services, Dow, and Microsoft**. At these positions, I've worked extensively with technologies like **Kubernetes, Azure, and backend development**, designing innovative solutions to complex problems. 

My passion for technology extends to independent projects, where I've developed tools like the UPENN Course Calendar and collaborated on distributed systems like PennCloud. Competitions like FemmeHack 2023 and Google Girl Hackathon have further honed my skills. 

I'm proficient in a range of programming languages and DevOps tools and am always eager to expand my knowledge and take on new challenges!

<br/>
<br/>
<br/>


## Selected Projects
<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <h2 class="category">{{ category }}</h2>
      {% assign categorized_projects = site.projects | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <!-- Generate cards for each project -->
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-1">
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
    {% assign sorted_projects = site.projects | sort: "importance" %}
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

<br/>
<br/>
<br/>