---
title: "メンバー"
permalink: /members/
author_profile: true
---

{% assign groups = site.data.members %}
{% for group in groups %}
## {{ group.title }}

<div class="member-grid">
{% for member in group.people %}
  {% include member-card.html member=member %}
{% endfor %}
</div>
{% endfor %}

> 掲載内容はサンプルです。学生の氏名・写真・研究テーマを掲載する際は、本人の同意と大学の規程を確認してください。
