---
layout: page
title: Invitees
permalink: /invitees/
---

Welcome to our invitees page! Here you can find information about all the talented staff members who have been invited to contribute to CipherSchool.

{% if site.staff_members.size > 0 %}
  <ul class="staff-list">
    {% for staff_member in site.staff_members %}
      <li>
        <h3>
          <a href="{{ staff_member.url | relative_url }}">{{ staff_member.title | escape }}</a>
        </h3>
        {% if staff_member.role %}
          <p><strong>Role:</strong> {{ staff_member.role }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>No staff members found.</p>
{% endif %}

---