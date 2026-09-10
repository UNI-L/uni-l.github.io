---
layout: page
title: News
permalink: /news/
nav: true
nav_order: 6
---

<div class="news">
  {% assign news = site.news | sort: "date" | reverse %}

  <div class="table-responsive">
    <table class="table table-sm table-borderless">
      {% for item in news %}
        <tr>
          <th scope="row" style="width: 20%">
            {{ item.date | date: "%b %d, %Y" }}
          </th>
          <td>
            {% if item.inline %}
              {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
            {% else %}
              <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
            {% endif %}
          </td>
        </tr>
      {% endfor %}
    </table>
  </div>
</div>
