---
title: Start
layout: default
weight: 10
---

{{ site.github | jsonify }}
<h3>Repositories</h3>
<ul>
    {% for repository in site.github.public_repositories %}
    <li>{{ repository.full_name }}</li>
    {% endfor %}
</ul>
<h3>Contributors</h3>
<ul>
    {% for contributor in site.github.contributors %}
    <li>
        <img src="{{ contributor.avatar_url }}" width="32" height="32"/> {{ contributor.login }}
    </li>
    {% endfor %}
</ul>