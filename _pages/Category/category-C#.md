---
title: "Post about C#"
layout: archive
permalink: /categories/csharp
author_profile: true
sidebar_main: true
---

{% assign posts = site.categories.CSharp | sort:"date" %}

{% for post in posts %}
  {% include archive-single.html type=page.entries_layout %}
{% endfor %}

