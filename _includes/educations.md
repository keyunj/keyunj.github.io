<h2>Education</h2>

<div class="educations">
<ol class="afflication">

{% for link in site.data.educations.main %}

<li>
<div class="edu-row">
  <div class="col-sm-3" style="position: relative;padding-left: 5px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" width="50px">
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title">{{ link.title }}</div>
      <div class="details">{{ link.position }} in {{ link.field }} <t style="float:right">{{link.start}} - {{ link.end }}</t></div>
      {% if link.advisor_url %}
        <div class="advisor">Advisor: <a href="{{ link.advisor_url }}">{{ link.advisor }}</a></div>
      {% else %}
        <div class="advisor">Advisor: {{ link.advisor }}</div>
      {% endif %}
  </div>

</div>
</li>

<br>

{% endfor %}

</ol>
</div>