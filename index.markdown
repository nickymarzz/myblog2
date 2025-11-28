---
layout: home
title: Home
description: A blog about programming, technology, and cryptography
---

# Welcome to {{ site.title }}

{{ site.description }}

## About This Blog

Welcome to {{ site.title }}, your destination for exploring the fascinating world of cryptography, programming, and technology. Here, we dive deep into various encryption techniques, programming concepts, and the latest developments in the tech world.

### What You'll Find Here

- **Cryptography Deep Dives**: Learn about different ciphers and encryption methods, from classical ciphers like Caesar and Vigenère to modern cryptographic systems like RSA.
- **Programming Tutorials**: Practical guides and tutorials to help you master various programming languages and technologies.
- **Tech Insights**: Stay updated with the latest trends and insights in the technology industry.

{% if site.data._members.size > 0 %}
### Our Community

We have {{ site.data._members.size }} active members contributing to our community:
- {% for member in site.data._members limit:3 %}
  {{ member.name }}{% if member.role %} ({{ member.role }}){% endif %}{% unless forloop.last %}, {% endunless %}
  {% endfor %}
  {% if site.data._members.size > 3 %}and more!{% endif %}
  
  <p><a href="{{ '/members' | relative_url }}">View all members →</a></p>
{% endif %}

---

*Happy coding and stay secure!*
