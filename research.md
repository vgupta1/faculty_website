---
author: Vishal Gupta
layout: page
title: Publications
---
{% assign papers = site.papers | sort: 'sort_order'  | reverse %}
 <dl>{% for paper in papers %}
   <dt><strong>{{forloop.index}}. &nbsp;  
		<a href="{{site.baseurl}}/Papers/{{paper.pdf_path}}"> 
   		{{paper.title}}. </a> </strong>
   		
	   	<!-- Author List if Necessary -->
	 	{%if paper.authors %}
	 	 with {{paper.authors}}
	 	{% endif %}    		
 	</dt>

 	<!-- Journal -->
 	<dd><strong>{{paper.journal}}</strong>  
 	({{paper.pub_date}}).</dd>

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