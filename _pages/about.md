---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---  

<!-- Navigation Menu -->
<div style="text-align: center; margin-bottom: 30px; padding: 15px 0; border-bottom: 1px solid var(--global-border-color);">
  <nav>
    <a href="#vision-approach" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">Vision & Approach</a> |
    <a href="#research-areas" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">Research Areas</a> |
    <a href="#opportunities" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">Opportunities</a> |
    <a href="#student-projects" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">Student Projects</a> |
    <a href="#publications" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">Publications</a> |
    <a href="#talks-presentations" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">Talks/Presentations/Media</a>
  </nav>
</div>

About me
------
I am the Founder and President of Craftnetics, Inc., and a former Assistant Professor at California State University, Chico, in the Department of Mechanical Engineering, Mechatronic Engineering, and Advanced Manufacturing. I have led innovative projects in AI, robotics, and advanced manufacturing and have secured approximately $1.5M in funding as PI, Co-PI, or senior personnel, while leading a group of scientists in grant development efforts at Siemens. My research focuses on data (e.g., [CatalogBank](https://github.com/bankh/catalogbank)), investigation of fundamentals (e.g., workflows, architectures, and algorithmic aspects), and their utilization as software (e.g., [DocumentLabeler](https://github.com/bankh/DocumentLabeler), GenAI Workbench, etc.) or hardware (e.g., [GPU Workstations](https://github.com/bankh/GPU_Compute), etc.) stacks to bridge academia and industry.

<figure style="text-align: center;">
  <img src="/images/former_research.png" alt="Former Research Projects and Future Research Thrusts" style="display: block; margin-left: auto; margin-right: auto;">
  <figcaption style="margin-top: 0.5em;"><em>Figure 1: Overview of previous research projects</em></figcaption>
</figure>

## Research Vision and Approach <a name="vision-approach"></a>

My research focuses on integrating advanced artificial intelligence and systems science into engineering to investigate design and autonomy for cyber-physical production systems and their associated processes. My work primarily addresses the challenges within the design-to-operation pipeline, enhancing operational efficiency and innovation through interdisciplinary collaboration.

My research journey began at Siemens Corporate Technology, where I worked on Industry 4.0 technologies including additive manufacturing support structures, temporal logic-based planning for autonomous systems, and mixed reality programming interfaces. This experience led to the development of innovative concepts like the Siemens SpiderBots—omnidirectional legged robotic systems for expanding 3D printing workspace—and autonomous agricultural production systems (AgPods).

At Colorado State University, I expanded into generative design and engineering of cyber-physical systems, developing multimodal approaches that integrate textual, geometric, and graph data for comprehensive design automation. This work resulted in tools such as CatalogBank (a multimodal engineering design dataset) and DocumentLabeler (for semi-automatic annotation), and GenAI Workbench for advancing the field toward more generalizable and scalable methods.

My research philosophy emphasizes three key principles: developing generalizable and scalable methods that transcend specific applications, maintaining open and reproducible research practices, and fostering an inclusive collaborative environment. This approach has led to high-impact outcomes including patents, publications, and successful grant proposals.

<div style="text-align: center; margin-top: 20px;">
  <a href="#top" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">↑ Go to Top</a>
</div>

<br>
Research Areas (with Past/ Published Research Projects): <a name="research-areas"></a>

<details>
<summary><strong>Artificial Intelligence and Generative Design</strong></summary>
{% assign ai_portfolio = site.portfolio | where: "selected", true | sort: 'date' | reverse %}
{% for post in ai_portfolio %}
  {% if post.keyword contains "Artificial Intelligence and Generative Design" %}
  <table style="width: 100%; border-collapse: collapse; border: none; margin-bottom: 20px;">
    <tr>
      <td style="vertical-align: middle; padding-right: 15px; width: 60%; border: none;">
        <strong>{{ post.title }}</strong><br>
        {% if post.advisor and post.advisor != "" %}<i>{{ post.advisor }}</i>, {% endif %}{{ post.date | default: "1900-01-01" | date: "%Y" }}
        {% if post.keyword %}
          <br><span style="background-color: #e8f4f8; color: #2c5aa0; padding: 2px 6px; border-radius: 3px; font-size: 0.85em; margin-right: 5px;">{{ post.keyword }}</span>
        {% endif %}
        {% if post.selected %}
          <span style="background-color: #d4edda; color: #155724; padding: 2px 6px; border-radius: 3px; font-size: 0.85em;">★ Featured</span>
        {% endif %}
        {% if post.excerpt %}
          <br><small>{{ post.excerpt }}</small>
        {% endif %}
        
        <!-- Publication-style Links -->
        {% capture portfolio_extras %}
          {%- if post.video and post.video != "" and post.video_show != true -%}
            <a href="{{ post.video }}" target="_blank" class="ref-tag" title="Video"><i class="fas fa-video"></i></a>
          {%- endif -%}
          {%- if post.slides and post.slides != "" and post.slide_show != true -%}
            <a href="{{ post.slides }}" target="_blank" class="ref-tag" title="Slides"><i class="fas fa-file-powerpoint"></i></a>
          {%- endif -%}
          {%- if post.github and post.github != "" -%}
            <a href="{{ post.github }}" target="_blank" class="ref-tag" title="GitHub"><i class="fab fa-github"></i></a>
          {%- endif -%}
          {%- if post.publication and post.publication != "" -%}
            {% assign publications = post.publication | split: "," %}
            {% for pub_ref in publications %}
              {% assign pub_ref = pub_ref | strip %}
              {% for publication in site.publications %}
                {% if publication.title == pub_ref or publication.permalink contains pub_ref %}
                  <a href="{{ publication.url }}" target="_blank" class="ref-tag" title="Publication"><i class="fas fa-file-alt"></i></a>
                  {% break %}
                {% endif %}
              {% endfor %}
            {% endfor %}
          {%- endif -%}
        {% endcapture %}
        {% assign portfolio_extras = portfolio_extras | strip %}
        {% if portfolio_extras and portfolio_extras != "" %}{{ portfolio_extras }}{% endif %}
      </td>
      <td style="vertical-align: middle; text-align: center; width: 120px; border: none;">
        <!-- Dynamic Poster/Image Display -->
        {% if post.poster and post.poster != "" %}
          <a href="{{ post.poster }}" target="_blank">
            <img src="{{ post.poster }}" alt="{{ post.title }} Project Image" style="width: 120px; height: 90px; object-fit: cover; margin: 5px; border-radius: 4px;">
          </a>
        {% endif %}
        
        <!-- Dynamic Video Thumbnail Display (if video_show is true) -->
        {% if post.video and post.video != "" and post.video_show == true %}
          <a href="{{ post.video }}" target="_blank">
            {% if post.video_thumbnail and post.video_thumbnail != "" %}
              <img src="{{ post.video_thumbnail }}" alt="{{ post.title }} Video Thumbnail" style="width: 120px; height: 90px; margin: 5px; border-radius: 4px; object-fit: cover;">
            {% else %}
              {% assign video_id = post.video | remove: "https://www.youtube.com/watch?v=" | remove: "https://youtu.be/" | split: "&" | first | split: "?" | first %}
              <img src="https://img.youtube.com/vi/{{ video_id }}/mqdefault.jpg" alt="{{ post.title }} Video Thumbnail" style="width: 120px; height: 90px; margin: 5px;">
            {% endif %}
          </a>
        {% endif %}
        
        <!-- Dynamic Slide Thumbnail Display (if slide_show is true) -->
        {% if post.slides and post.slides != "" and post.slide_show == true %}
          {% if post.slide_thumbnail and post.slide_thumbnail != "" %}
            <a href="{{ post.slides }}" target="_blank">
              <img src="{{ post.slide_thumbnail }}" alt="{{ post.title }} Slide Thumbnail" style="width: 120px; height: 90px; margin: 5px; border-radius: 4px; object-fit: cover;">
            </a>
          {% endif %}
        {% endif %}
      </td>
    </tr>
  </table>
  {% endif %}
{% endfor %}

<p style="text-align: center; margin-top: 20px;">
  <a href="/portfolio/" class="btn btn--primary">View Other Projects</a>
</p>

</details>

<details>
<summary><strong>Advanced Manufacturing (Smart Manufacturing/ Industry 4.0)</strong></summary>
{% assign manufacturing_portfolio = site.portfolio | where: "selected", true | sort: 'date' | reverse %}
{% for post in manufacturing_portfolio %}
  {% if post.keyword contains "Advanced Manufacturing" or post.keyword contains "Smart Manufacturing" %}
  <table style="width: 100%; border-collapse: collapse; border: none; margin-bottom: 20px;">
    <tr>
      <td style="vertical-align: middle; padding-right: 15px; width: 60%; border: none;">
        <strong>{{ post.title }}</strong><br>
        {% if post.advisor and post.advisor != "" %}<i>{{ post.advisor }}</i>, {% endif %}{{ post.date | default: "1900-01-01" | date: "%Y" }}
        {% if post.keyword %}
          <br><span style="background-color: #e8f4f8; color: #2c5aa0; padding: 2px 6px; border-radius: 3px; font-size: 0.85em; margin-right: 5px;">{{ post.keyword }}</span>
        {% endif %}
        {% if post.selected %}
          <span style="background-color: #d4edda; color: #155724; padding: 2px 6px; border-radius: 3px; font-size: 0.85em;">★ Featured</span>
        {% endif %}
        {% if post.excerpt %}
          <br><small>{{ post.excerpt }}</small>
        {% endif %}
        
        <!-- Publication-style Links -->
        {% capture portfolio_extras %}
          {%- if post.video and post.video != "" and post.video_show != true -%}
            <a href="{{ post.video }}" target="_blank" class="ref-tag" title="Video"><i class="fas fa-video"></i></a>
          {%- endif -%}
          {%- if post.slides and post.slides != "" and post.slide_show != true -%}
            <a href="{{ post.slides }}" target="_blank" class="ref-tag" title="Slides"><i class="fas fa-file-powerpoint"></i></a>
          {%- endif -%}
          {%- if post.github and post.github != "" -%}
            <a href="{{ post.github }}" target="_blank" class="ref-tag" title="GitHub"><i class="fab fa-github"></i></a>
          {%- endif -%}
          {%- if post.publication and post.publication != "" -%}
            {% assign publications = post.publication | split: "," %}
            {% for pub_ref in publications %}
              {% assign pub_ref = pub_ref | strip %}
              {% for publication in site.publications %}
                {% if publication.title == pub_ref or publication.permalink contains pub_ref %}
                  <a href="{{ publication.url }}" target="_blank" class="ref-tag" title="Publication"><i class="fas fa-file-alt"></i></a>
                  {% break %}
                {% endif %}
              {% endfor %}
            {% endfor %}
          {%- endif -%}
        {% endcapture %}
        {% assign portfolio_extras = portfolio_extras | strip %}
        {% if portfolio_extras and portfolio_extras != "" %}{{ portfolio_extras }}{% endif %}
      </td>
      <td style="vertical-align: middle; text-align: center; width: 120px; border: none;">
        <!-- Dynamic Poster/Image Display -->
        {% if post.poster and post.poster != "" %}
          <a href="{{ post.poster }}" target="_blank">
            <img src="{{ post.poster }}" alt="{{ post.title }} Project Image" style="width: 120px; height: 90px; object-fit: cover; margin: 5px; border-radius: 4px;">
          </a>
        {% endif %}
        
        <!-- Dynamic Video Thumbnail Display (if video_show is true) -->
        {% if post.video and post.video != "" and post.video_show == true %}
          <a href="{{ post.video }}" target="_blank">
            {% if post.video_thumbnail and post.video_thumbnail != "" %}
              <img src="{{ post.video_thumbnail }}" alt="{{ post.title }} Video Thumbnail" style="width: 120px; height: 90px; margin: 5px; border-radius: 4px; object-fit: cover;">
            {% else %}
              {% assign video_id = post.video | remove: "https://www.youtube.com/watch?v=" | remove: "https://youtu.be/" | split: "&" | first | split: "?" | first %}
              <img src="https://img.youtube.com/vi/{{ video_id }}/mqdefault.jpg" alt="{{ post.title }} Video Thumbnail" style="width: 120px; height: 90px; margin: 5px;">
            {% endif %}
          </a>
        {% endif %}
        
        <!-- Dynamic Slide Thumbnail Display (if slide_show is true) -->
        {% if post.slides and post.slides != "" and post.slide_show == true %}
          {% if post.slide_thumbnail and post.slide_thumbnail != "" %}
            <a href="{{ post.slides }}" target="_blank">
              <img src="{{ post.slide_thumbnail }}" alt="{{ post.title }} Slide Thumbnail" style="width: 120px; height: 90px; margin: 5px; border-radius: 4px; object-fit: cover;">
            </a>
          {% endif %}
        {% endif %}
      </td>
    </tr>
  </table>
  {% endif %}
{% endfor %}

<p style="text-align: center; margin-top: 20px;">
  <a href="/portfolio/" class="btn btn--primary">View Other Projects</a>
</p>

</details>

<details>
<summary><strong>Robotics and Autonomous Systems</strong></summary>
{% assign robotics_portfolio = site.portfolio | where: "selected", true | sort: 'date' | reverse %}
{% for post in robotics_portfolio %}
  {% if post.keyword contains "Robotics and Autonomous Systems" %}
  <table style="width: 100%; border-collapse: collapse; border: none; margin-bottom: 20px;">
    <tr>
      <td style="vertical-align: middle; padding-right: 15px; width: 60%; border: none;">
        <strong>{{ post.title }}</strong><br>
        {% if post.advisor and post.advisor != "" %}<i>{{ post.advisor }}</i>, {% endif %}{{ post.date | default: "1900-01-01" | date: "%Y" }}
        {% if post.keyword %}
          <br><span style="background-color: #e8f4f8; color: #2c5aa0; padding: 2px 6px; border-radius: 3px; font-size: 0.85em; margin-right: 5px;">{{ post.keyword }}</span>
        {% endif %}
        {% if post.selected %}
          <span style="background-color: #d4edda; color: #155724; padding: 2px 6px; border-radius: 3px; font-size: 0.85em;">★ Featured</span>
        {% endif %}
        {% if post.excerpt %}
          <br><small>{{ post.excerpt }}</small>
        {% endif %}
        
        <!-- Publication-style Links -->
        {% capture portfolio_extras %}
          {%- if post.video and post.video != "" and post.video_show != true -%}
            <a href="{{ post.video }}" target="_blank" class="ref-tag" title="Video"><i class="fas fa-video"></i></a>
          {%- endif -%}
          {%- if post.slides and post.slides != "" and post.slide_show != true -%}
            <a href="{{ post.slides }}" target="_blank" class="ref-tag" title="Slides"><i class="fas fa-file-powerpoint"></i></a>
          {%- endif -%}
          {%- if post.github and post.github != "" -%}
            <a href="{{ post.github }}" target="_blank" class="ref-tag" title="GitHub"><i class="fab fa-github"></i></a>
          {%- endif -%}
          {%- if post.publication and post.publication != "" -%}
            {% assign publications = post.publication | split: "," %}
            {% for pub_ref in publications %}
              {% assign pub_ref = pub_ref | strip %}
              {% for publication in site.publications %}
                {% if publication.title == pub_ref or publication.permalink contains pub_ref %}
                  <a href="{{ publication.url }}" target="_blank" class="ref-tag" title="Publication"><i class="fas fa-file-alt"></i></a>
                  {% break %}
                {% endif %}
              {% endfor %}
            {% endfor %}
          {%- endif -%}
        {% endcapture %}
        {% assign portfolio_extras = portfolio_extras | strip %}
        {% if portfolio_extras and portfolio_extras != "" %}{{ portfolio_extras }}{% endif %}
      </td>
      <td style="vertical-align: middle; text-align: center; width: 120px; border: none;">
        <!-- Dynamic Poster/Image Display -->
        {% if post.poster and post.poster != "" %}
          <a href="{{ post.poster }}" target="_blank">
            <img src="{{ post.poster }}" alt="{{ post.title }} Project Image" style="width: 120px; height: 90px; object-fit: cover; margin: 5px; border-radius: 4px;">
          </a>
        {% endif %}
        
        <!-- Dynamic Video Thumbnail Display (if video_show is true) -->
        {% if post.video and post.video != "" and post.video_show == true %}
          <a href="{{ post.video }}" target="_blank">
            {% if post.video_thumbnail and post.video_thumbnail != "" %}
              <img src="{{ post.video_thumbnail }}" alt="{{ post.title }} Video Thumbnail" style="width: 120px; height: 90px; margin: 5px; border-radius: 4px; object-fit: cover;">
            {% else %}
              {% assign video_id = post.video | remove: "https://www.youtube.com/watch?v=" | remove: "https://youtu.be/" | split: "&" | first | split: "?" | first %}
              <img src="https://img.youtube.com/vi/{{ video_id }}/mqdefault.jpg" alt="{{ post.title }} Video Thumbnail" style="width: 120px; height: 90px; margin: 5px;">
            {% endif %}
          </a>
        {% endif %}
        
        <!-- Dynamic Slide Thumbnail Display (if slide_show is true) -->
        {% if post.slides and post.slides != "" and post.slide_show == true %}
          {% if post.slide_thumbnail and post.slide_thumbnail != "" %}
            <a href="{{ post.slides }}" target="_blank">
              <img src="{{ post.slide_thumbnail }}" alt="{{ post.title }} Slide Thumbnail" style="width: 120px; height: 90px; margin: 5px; border-radius: 4px; object-fit: cover;">
            </a>
          {% endif %}
        {% endif %}
      </td>
    </tr>
  </table>
  {% endif %}
{% endfor %}

<p style="text-align: center; margin-top: 20px;">
  <a href="/portfolio/" class="btn btn--primary">View Other Projects</a>
</p>

</details>

<details>
<summary><strong>Optimization, Control, and Systems Engineering</strong></summary>
{% assign optimization_portfolio = site.portfolio | where: "selected", true | sort: 'date' | reverse %}
{% for post in optimization_portfolio %}
  {% if post.keyword contains "Optimization, Control, and Systems Engineering" %}
  <table style="width: 100%; border-collapse: collapse; border: none; margin-bottom: 20px;">
    <tr>
      <td style="vertical-align: middle; padding-right: 15px; width: 60%; border: none;">
        <strong>{{ post.title }}</strong><br>
        {% if post.advisor and post.advisor != "" %}<i>{{ post.advisor }}</i>, {% endif %}{{ post.date | default: "1900-01-01" | date: "%Y" }}
        {% if post.keyword %}
          <br><span style="background-color: #e8f4f8; color: #2c5aa0; padding: 2px 6px; border-radius: 3px; font-size: 0.85em; margin-right: 5px;">{{ post.keyword }}</span>
        {% endif %}
        {% if post.selected %}
          <span style="background-color: #d4edda; color: #155724; padding: 2px 6px; border-radius: 3px; font-size: 0.85em;">★ Featured</span>
        {% endif %}
        {% if post.excerpt %}
          <br><small>{{ post.excerpt }}</small>
        {% endif %}
        
        <!-- Publication-style Links -->
        {% capture portfolio_extras %}
          {%- if post.video and post.video != "" and post.video_show != true -%}
            <a href="{{ post.video }}" target="_blank" class="ref-tag" title="Video"><i class="fas fa-video"></i></a>
          {%- endif -%}
          {%- if post.slides and post.slides != "" and post.slide_show != true -%}
            <a href="{{ post.slides }}" target="_blank" class="ref-tag" title="Slides"><i class="fas fa-file-powerpoint"></i></a>
          {%- endif -%}
          {%- if post.github and post.github != "" -%}
            <a href="{{ post.github }}" target="_blank" class="ref-tag" title="GitHub"><i class="fab fa-github"></i></a>
          {%- endif -%}
          {%- if post.publication and post.publication != "" -%}
            {% assign publications = post.publication | split: "," %}
            {% for pub_ref in publications %}
              {% assign pub_ref = pub_ref | strip %}
              {% for publication in site.publications %}
                {% if publication.title == pub_ref or publication.permalink contains pub_ref %}
                  <a href="{{ publication.url }}" target="_blank" class="ref-tag" title="Publication"><i class="fas fa-file-alt"></i></a>
                  {% break %}
                {% endif %}
              {% endfor %}
            {% endfor %}
          {%- endif -%}
        {% endcapture %}
        {% assign portfolio_extras = portfolio_extras | strip %}
        {% if portfolio_extras and portfolio_extras != "" %}{{ portfolio_extras }}{% endif %}
      </td>
      <td style="vertical-align: middle; text-align: center; width: 120px; border: none;">
        <!-- Dynamic Poster/Image Display -->
        {% if post.poster and post.poster != "" %}
          <a href="{{ post.poster }}" target="_blank">
            <img src="{{ post.poster }}" alt="{{ post.title }} Project Image" style="width: 120px; height: 90px; object-fit: cover; margin: 5px; border-radius: 4px;">
          </a>
        {% endif %}
        
        <!-- Dynamic Video Thumbnail Display (if video_show is true) -->
        {% if post.video and post.video != "" and post.video_show == true %}
          <a href="{{ post.video }}" target="_blank">
            {% if post.video_thumbnail and post.video_thumbnail != "" %}
              <img src="{{ post.video_thumbnail }}" alt="{{ post.title }} Video Thumbnail" style="width: 120px; height: 90px; margin: 5px; border-radius: 4px; object-fit: cover;">
            {% else %}
              {% assign video_id = post.video | remove: "https://www.youtube.com/watch?v=" | remove: "https://youtu.be/" | split: "&" | first | split: "?" | first %}
              <img src="https://img.youtube.com/vi/{{ video_id }}/mqdefault.jpg" alt="{{ post.title }} Video Thumbnail" style="width: 120px; height: 90px; margin: 5px;">
            {% endif %}
          </a>
        {% endif %}
        
        <!-- Dynamic Slide Thumbnail Display (if slide_show is true) -->
        {% if post.slides and post.slides != "" and post.slide_show == true %}
          {% if post.slide_thumbnail and post.slide_thumbnail != "" %}
            <a href="{{ post.slides }}" target="_blank">
              <img src="{{ post.slide_thumbnail }}" alt="{{ post.title }} Slide Thumbnail" style="width: 120px; height: 90px; margin: 5px; border-radius: 4px; object-fit: cover;">
            </a>
          {% endif %}
        {% endif %}
      </td>
    </tr>
  </table>
  {% endif %}
{% endfor %}

<p style="text-align: center; margin-top: 20px;">
  <a href="/portfolio/" class="btn btn--primary">View Other Projects</a>
</p>

</details>
<br>
In many cases, the projects intersect with multiple research areas. For example, Retrieval Augmented work could be considered AI (as its core is in that domain), while its impact extends to Systems Engineering.

These studies in the provided areas have resulted in high-impact outcomes, including publications (such as patents, conference papers, and journal articles) and further collaborations. My portfolio provides more details on past projects. Ongoing and future projects in **Generative Design and Engineering of Cyber-Physical Systems**, **Embodied AI for Advanced Manufacturing**, and **AI-based Scientific Discovery** are not included above; please contact me if you are interested in learning more. Please note that our research will be published and the code will be shared to ensure reproducibility—either fully or partially—to protect intellectual property (the "secret sauce").

<div style="text-align: center; margin-top: 20px;">
  <a href="#top" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">↑ Go to Top</a>
</div>

Opportunities (for Students) <a name="opportunities"></a>
------
<b>Internship:</b> If you are a graduate student interested in an internship and/or getting more information
about a project at Craftnetics, please send an email to info@craftnetics.ai. Please add your resume with details about your current interests.

Student Projects <a name="student-projects"></a>
------
<details>
<summary>Selected Student Projects - Expand to see more</summary>

{% if site.student_projects %}
  {% assign selected_projects = site.student_projects | where: "selected", true | sort: 'date' | reverse %}
  {% for post in selected_projects %}
  <table style="width: 100%; border-collapse: collapse; border: none; margin-bottom: 20px;">
    <tr>
      <td style="vertical-align: top; padding-right: 15px; width: 60%; border: none;">
        <strong>{{ post.title }}</strong><br>
        {% if post.sponsor %}<i>{{ post.sponsor }}</i>, {% endif %}{{ post.date | default: "1900-01-01" | date: "%Y" }}
        {% if post.keyword %}
          <br><span style="background-color: #e8f4f8; color: #2c5aa0; padding: 2px 6px; border-radius: 3px; font-size: 0.85em; margin-right: 5px;">{{ post.keyword }}</span>
        {% endif %}
        {% if post.excerpt %}
          <br><small>{{ post.excerpt }}</small>
        {% endif %}
      </td>
      <td style="vertical-align: top; text-align: center; width: 120px; border: none;">
        <!-- Dynamic Video Display -->
        {% if post.video and post.video != "" %}
          <a href="{{ post.video }}" target="_blank">
            {% if post.video_thumbnail and post.video_thumbnail != "" %}
              <img src="{{ post.video_thumbnail }}" alt="{{ post.title }} Video Thumbnail" style="width: 120px; height: 90px; margin: 5px; border-radius: 4px; object-fit: cover;">
            {% else %}
              {% assign video_id = post.video | split: "youtu.be/" | last | split: "?" | first %}
              {% if video_id == post.video %}
                {% assign video_id = post.video | split: "watch?v=" | last | split: "&" | first %}
              {% endif %}
              <img src="https://img.youtube.com/vi/{{ video_id }}/mqdefault.jpg" alt="{{ post.title }} Video Thumbnail" style="width: 120px; height: 90px; margin: 5px; border-radius: 4px;">
            {% endif %}
          </a>
        {% endif %}
        
        <!-- Dynamic Poster/Image Display -->
        {% if post.poster and post.poster != "" %}
          <a href="{{ post.poster }}" target="_blank">
            <img src="{{ post.poster }}" alt="{{ post.title }} Project Image" style="width: 120px; height: 90px; object-fit: cover; margin: 5px; border-radius: 4px;">
          </a>
        {% endif %}
        
        <!-- Dynamic GitHub Display -->
        {% if post.github and post.github != "" %}
          <a href="{{ post.github }}" target="_blank" style="display: block; margin: 5px;">
            <div style="background-color: #24292e; color: white; padding: 8px; border-radius: 4px; font-size: 0.8em; text-decoration: none;">
              <i class="fab fa-github"></i> GitHub
            </div>
          </a>
        {% endif %}
      </td>
    </tr>
  </table>
  {% endfor %}
{% else %}
  <p>Student projects will be displayed here once the collection is loaded.</p>
{% endif %}
  <p><a href="/teaching/">View Other Student Projects ...</a></p>
</details>
<br>

<div style="text-align: center; margin-top: 20px;">
  <a href="#top" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">↑ Go to Top</a>
</div>

Publications (Newest 5)<a name="publications"></a>
------ 
<!-- <details>
<summary>Publications </summary> -->
{% assign all_pubs = site.publications | sort: 'date' | reverse %}
{% assign sorted_pubs = "" | split: "" %}
{% for pub in all_pubs %}
  {% unless pub.type == 'In Preparation' %}
    {% assign sorted_pubs = sorted_pubs | push: pub %}
  {% endunless %}
{% endfor %}
{% assign conf_count = 0 %}
{% assign pat_count = 0 %}
{% assign jour_count = 0 %}
{% for post in sorted_pubs limit:5 %}
  {% if post.type contains "Patent" %}
    {% assign pat_count = pat_count | plus: 1 %}
    {% assign current_label = '[P' | append: pat_count | append: ']' %}
    {% include archive-single-publication.html post=post type='list' label=current_label %}
  {% elsif post.type contains "Conference" %}
    {% assign conf_count = conf_count | plus: 1 %}
    {% assign current_label = '[C' | append: conf_count | append: ']' %}
    {% include archive-single-publication.html post=post type='list' label=current_label %}
  {% else %}
    {% assign jour_count = jour_count | plus: 1 %}
    {% assign current_label = '[J' | append: jour_count | append: ']' %}
    {% include archive-single-publication.html post=post type='list' label=current_label %}
  {% endif %}
{% endfor %}
<p><a href="/publications/">Read More...</a></p>
<!-- </details> -->

<div style="text-align: center; margin-top: 20px;">
  <a href="#top" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">↑ Go to Top</a>
</div>

Talks/ Presentations/ Media (Newest 5)<a name="talks-presentations"></a>
------
<!-- <details> -->
<!-- <summary>Talks/ Presentations (Newest 5)</summary> -->

<ol style="list-style-type: decimal; padding-left: 20px;">
{% assign sorted_talks = site.talks | sort: 'date' | reverse %}
{% for post in sorted_talks limit:5 %}
    <li style="margin-bottom: 15px;">
    {% include archive-single-talk-cv.html %}
    </li>
{% endfor %}
</ol>
<a href="/talks/">Read More...</a>

<!-- </details> -->

<div style="text-align: center; margin-top: 20px;">
  <a href="#top" style="color: var(--global-text-color); text-decoration: none; font-weight: bold; font-family: var(--global-font-family);">↑ Go to Top</a>
</div>