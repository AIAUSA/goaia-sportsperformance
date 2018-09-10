---
title: Student Opportunities
permalink: "/get-involved/students"
layout: page
---

{% assign opps = site.events | where: "student", "true" %}

<div class="col-md-12">
<h2 class="title-underblock custom mb30">Student Internships</h2>
<div class="panel-group" role="tablist" aria-multiselectable="true">
{% assign subopps = opps | where: "type", "Student-Internship" %}
{% for opp in subopps %}
<div class="panel panel-default">
<div class="panel-heading" role="tab" id="heading{{forloop.index}}">
<h4 class="panel-title">
<a data-toggle="collapse" href="#collapse{{forloop.index}}" aria-expanded="false" aria-controls="collapse{{forloop.index}}">
{{opp.title}}
<span class="panel-icon"></span>
</a>
</h4>
</div><!-- End .panel-heading -->
<div id="collapse{{forloop.index}}" class="panel-collapse collapse" role="tabpanel" aria-labelledby="heading{{forloop.index}}">
<div class="panel-body">
<img class="col-md-4 pull-right" src="{{opp.featured_image}}" /> {{opp.description | markdownify }}
</div><!-- End .panel-body -->
</div><!-- End .panel-collapse -->
</div><!-- End .panel -->
{% endfor %}
</div><!-- End .panel-group -->

</div>
