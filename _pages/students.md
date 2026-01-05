---
title: "Teaching and Mentoring"
permalink: "/contact/students.html"
---

### Teaching
#### 2025 Fall
- CEE 372: [Transportation Engineering](https://catalog.apps.asu.edu/catalog/classes/classlist?searchType=all&collapse=Y&keywords=60289&term=2257) (Undergraduate)
  - 82 students enrolled. Fundamental background in highway and traffic engineering, covering planning, design, and operations.

#### 2025 Spring
- CEE 598: [Traffic Flow Theory](https://catalog.apps.asu.edu/catalog/classes/classlist?searchType=all&collapse=Y&keywords=30966&term=2251) (Graduate)

### Current team

<div class="container">
  <div class="row gap-y" style="margin-bottom: -20px;">
    {% assign current_team = site.data.people | where: "status", "current" | sort: "mentored" | reverse %}
    {% for person in current_team %}
      <div class="col-lg-4 mb-4 text-center">
        <img src="{{ person.profile_pic }}" alt="{{ person.name }}" style="width:100%; max-width:200px; height:200px; object-fit:cover; border-radius:50%">
        <h5 class="mb-1 font-weight-bold mt-2">{{ person.name }}</h5>
        <small class="text-muted">Mentored: {{ person.mentored }}</small><br>
        {% if person.current_affiliation %}
        <small class="text-muted">Current: {{ person.current_affiliation }}</small> 
         {% endif %}
      </div>
    {% endfor %}
  </div>
</div>

### Perspective students

I have funded PhD positions on a rolling basis. If you are interested, you are welcome to [<u>submit your PhD application</u>](https://ssebe.engineering.asu.edu/graduate-applications/) through the ASU School of Sustainable Engineering and the Built Environment, Civil and Environmental Engineering (Tempe Campus), with a specialization in Transportation.


<div class="alert alert-secondary" role="alert">
<strong>Attention:</strong> Please ensure your application includes your transcripts, research statement, and reference letters. Mention my name in your application materials for consideration. Shortlisted candidates will be contacted for interviews.
</div>


### Previously mentored students

<div class="container">
  <div class="row gap-y" style="margin-bottom: -20px;">
    {% assign previous_team = site.data.people | where_exp: 'person', 'person.status != "current"' | sort: 'mentored' | reverse %}
    {% for person in previous_team %}
      <div class="col-lg-4 mb-4 text-center">
        <img src="{{ person.profile_pic }}" alt="{{ person.name }}" style="width:100%; max-width:200px; height:200px; object-fit:cover; border-radius:50%;">
        <h5 class="mb-1 font-weight-bold mt-2">{{ person.name }}</h5>
        <small class="text-muted">Mentored: {{ person.mentored }}</small><br>
        {% if person.current_affiliation %}
        <small class="text-muted">Current: {{ person.current_affiliation }}</small>
        {% endif %}
      </div>
    {% endfor %}
  </div>
</div>

