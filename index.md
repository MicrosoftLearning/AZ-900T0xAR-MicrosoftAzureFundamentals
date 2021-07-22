---
title: لتعليمات المستضافة عبر الإنترنت
permalink: index.html
layout: home
---

# دليل المحتوى

ارتباطات تشعبية لكل معاينة من المعاينات. قد يختار المعلمون استخدام المعاينة كعرض توضيحي أو معمل للطلاب. 

## المعاينات

{% assign wts = site.pages | where_exp:"page", "page.url contains '/Instructions/Walkthroughs'" %}
| الوحدة | المعاينة |
| --- | --- | 
{% for activity in wts %}| {{ activity.wts.module }} | [{{ activity.wts.title }}{% if activity.wts.type %} - {{ activity.wts.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

