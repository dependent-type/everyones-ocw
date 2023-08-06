---
layout: page
title: Home
id: home
permalink: /
---

# 모두의 OCW에 오신 것을 환영합니다! 🎉

<span style="font-weight: bold">모두의 OCW</span>는 비영리 목적의 웹사이트로, 배움의 자유를 실현하기 위해 만들어졌습니다. 원하는 주제를 자유롭게 학습하고, 더 나아가 자신만의 OCW를 개설하거나 공동 작업에 참여하여 사이트에 기여할 수 있습니다. <span style="font-weight: bold">[[노트 작성 튜토리얼]]</span>을 참고해 보세요 :)

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
