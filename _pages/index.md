---
layout: page
title: Home
id: home
permalink: /
---

# 모두의 OCW에 오신 것을 환영합니다! 🎉

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
<span style="font-weight: bold">[[시작하기]]</span> 에서 자유로운 학습을 시작해 보세요!
</p>


<strong>최근 업데이트된 노트</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 10 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
