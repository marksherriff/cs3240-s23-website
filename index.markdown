---
layout: default
title: Home
nav_order: 1
description: "CS 3240 - Advanced Software Development Techniques"
permalink: /
---

# CS 3240 - Spring 2023
## Advanced Software Development Techniques
_aka Software Engineering_

[Online Coursepack]({{ site.data.externallinks.coursepack }}){: .btn  .btn-primary .mr-2 }
[Gradescope]({{ site.data.externallinks.gradescope }}){: .btn .btn-primary .mr-2  }
[Piazza]({{ site.data.externallinks.piazza }}){: .btn .btn-primary .mr-2  }
[Collab]({{ site.data.externallinks.lms }}){: .btn .btn-primary .mr-2  }
[GitHub]({{ site.data.externallinks.github_organization }}){: .btn .btn-primary .mr-2  }

## End of Semester Information/Schedule

* Mon, May 1 :: [Final Exam Signup available](https://docs.google.com/forms/d/e/1FAIpQLSejAE3crKWN_baCchp8uciewlE_groPjEjRYSIX4juYsPNT6Q/viewform?usp=sf_link)
* Tue, May 2 :: Final Project, Scrum Master Report, and Honor Pledge due by 11:59 PM (no code should be pushed to GitHub after May 2!)
* Tue, May 2 :: [Do Final Team Evaluations](https://docs.google.com/forms/d/e/1FAIpQLSd0hhNykquz7J3EVKKpW468gNU1cylbA3LQGbYw0eGeVEOdwQ/viewform?usp=sf_link)
* Wed, May 3-Fri, May 5 :: [Project Demos w/ Professors](https://docs.google.com/document/d/1jRQ3OJUfjrZu15ucjydgYL5FoOpOJuNcti9CGNhWdts/edit?usp=sharing) 
* Sat, May 6-Sun, May 7 :: Any remaining demo scores returned (most will be returned within 24-48 hours)
* Sun, May 7 :: Final Exam Signup closes at 11:59 PM
* Mon, May 8 :: First Exam Session, 9:00 AM in Rice 130
* Thu, May 11 :: Second Exam Session, 2:00 PM in Rice 130

## Lecture and Lab Sessions
{% for section in site.data.semesterinfo.lecture_sections %} {{ section }}    
{% endfor %}   
## Staff Information

{% for professor in site.data.professors %}

__Instructor:__ {{ professor.name }}   
Office: {{ professor.office }}   
Office Hours: {{ professor.office_hours }}        
Email: [{{ professor.email }}]({{ professor.email }})   
Website: [{{ professor.website }}]({{ professor.website }})   

{% endfor %}

__Teaching Assistants:__ {% for ta in site.data.tas %} {{ ta.name }}, {% endfor %}  