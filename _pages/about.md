---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a research scientist at Siemens Corporation Corporate Technology. Before SCCT, I was a research
assistant in Rutgers University, University of Connecticut, and Carnegie Mellon University.  

In SCCT, I've worked in different technology fields to .... {ADD MORE}

Opportunities in Automation Runtime Technologies at SCCT
------
<b>Full-time:</b> ART consist of software developers and researchers in diverse backgrounds. You can email me
to learn about the current opportunities and you: 1. are an expert in runtime system technologies and their applications, 2. have a graduate degree in STEM or fundamental sciences, or 3. are a full stack programming ninja. <br />

<b>Internship:</b> If you are a graduate student interested in an internship at SCCT and/or getting more information
about a project, please send [me](hasan.bank@siemens.com) an email. Please add your resume with the details of current
research with your advisor's name.

Publications
------ 
{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

Talks
------
{% for post in site.talks reversed %}
  {% include archive-single-talk.html %}
{% endfor %}