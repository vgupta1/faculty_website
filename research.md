---
author: Vishal Gupta
layout: page
title: Publications
excerpt: data-driven optimization small-data regime operations research robust uncertainty decision-making scarce data
---
<!-- Only perform this section if there are WIP papers-->
 {% assign papers = site.papers | where: "journal", "Work in Progress" | sort: 'sort_order'  | reverse %}

{%unless papers ==empty %}
# In Preparation
{%endunless%}

{% assign papers = site.papers | where: "journal", "Work in Progress" | sort: 'sort_order'  | reverse %}
 <dl>{% for paper in papers %}
   <dt><strong>&middot; &nbsp;  
		<a href="{{paper.pdf_path}}"> 
   		{{paper.title}}. </a> </strong>
   		
	   	<!-- Author List if Necessary -->
	 	{%if paper.authors %}
	 	 with {{paper.authors}}.
	 	{% endif %}    		
 	</dt>

 	<!-- Journal -->
 	<dd><strong>{{paper.journal}}</strong>{%if paper.pub_date %}
 		({{paper.pub_date}})
 	{% endif %}.
 	</dd>

 	<!-- Abstract Paper Links -->
 	<dd><a id="{{paper.shorttitle}}toggle" href="">[Abstract]</a>
		
		<!-- Main Link --> 		
<!-- 		&nbsp; <a href="{{site.baseurl}}/Papers/{{paper.pdf_path}}">
   		[PDF] </a>
 -->
 		<!-- Auxiliary Paper Links As Necessary -->
 		{% for link in paper.links %}
 		  &nbsp; <a href="{{link.path}}">[{{link.name}}] </a>
 		{% endfor %}

 	</dd>

 	<!-- Awards if Necessary -->
 	{% for note in paper.notes %}
 		<dd>{{note.name}}</dd>
 	{% endfor %}

 	<!-- Actual Abstract -->
 	<dd id="{{paper.shorttitle}}content" style="display: none">
 		{{paper.content}}
 	</dd>

 	<dd> <br> </dd>
 	{% endfor %}
 </dl>



# Accepted and Under Review
{% assign papers = site.papers | sort: 'sort_order'  | reverse %}

{% assign iter = 0 %}
 <dl>{% for paper in papers %}
   {% if paper.journal == "Work in Progress"%}
   	{% continue %}
   {% endif %}

	{% assign iter = iter | plus: 1 %}
   <dt><strong>{{iter}}. &nbsp;  
		<a href="{{site.baseurl}}/Papers/{{paper.pdf_path}}"> 
   		{{paper.title}}. </a> </strong>
   		
	   	<!-- Author List if Necessary -->
	 	{%if paper.authors %}
	 	 with {{paper.authors}}.
	 	{% endif %}    		
 	</dt>

 	<!-- Journal -->
 	<dd><strong>{{paper.journal}}</strong>{%if paper.pub_date %}
 		({{paper.pub_date}})
 	{% endif %}.
 	</dd>

 	<!-- Abstract Paper Links -->
 	<dd><a id="{{paper.shorttitle}}toggle" href="">[Abstract]</a>
 		<!-- Auxiliary Paper Links As Necessary -->
 		{% for link in paper.links %}
 		  &nbsp; <a href="{{link.path}}">[{{link.name}}] </a>
 		{% endfor %}

 	</dd>

 	<!-- Awards if Necessary -->
 	{% for award in paper.awards %}
		<dd style="color:Orange" >**{{award.name}}**</dd>
 	{% endfor %}

 	<!-- Actual Abstract -->
 	<dd id="{{paper.shorttitle}}content" style="display: none">
 		{{paper.content}}
 	</dd>

 	<dd> <br> </dd>
 	{% endfor %}
 </dl>



<!-- Javascript to make the abstracts work -->
<script src="//code.jquery.com/jquery-1.11.2.min.js"></script>
<script src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script>
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>

<script>
 {% for paper in site.papers %}
  $("#{{paper.shorttitle}}toggle").click( function() { $("#{{paper.shorttitle}}content").toggle(); return false; });
 {% endfor %}
</script>

