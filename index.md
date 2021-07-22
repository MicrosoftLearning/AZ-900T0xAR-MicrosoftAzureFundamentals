<div id="readme" class="Box-body readme blob js-code-block-container p-5 p-xl-6 gist-border-0" dir="rtl">
    <article class="markdown-body entry-content container-lg" itemprop="text"><table>
  <thead>
  <tr>
  <th>title</th>
  <th>permalink</th>
  <th>layout</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div>لتعليمات المستضافة عبر الإنترنت</div></td>
  <td><div>index.html</div></td>
  <td><div>home</div></td>
  </tr>
  </tbody>
</table>

# دليل المحتوى

ارتباطات تشعبية لكل معاينة من المعاينات. قد يختار المعلمون استخدام المعاينة كعرض توضيحي أو معمل للطلاب. 

## المعاينات

{% assign wts = site.pages | where_exp:"page", "page.url contains '/Instructions/Walkthroughs'" %}
| الوحدة | المعاينة |
| --- | --- | 
{% for activity in wts %}| {{ activity.wts.module }} | [{{ activity.wts.title }}{% if activity.wts.type %} - {{ activity.wts.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

