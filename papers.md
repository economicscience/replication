{% for paper in site.data.papers %}

<ul>
	<li>
		<b>Title:</b> {{ paper.title }}
	</li>
	<li>
		<b>Authors:</b>
		<ul>
			{% for author in paper.authors %}
			<li>{{ author.name }}</li>
			{% endfor %} 
		</ul>
	</li>
	<li>
		<b>Link to data:</b>
		<a href="{{ paper.data.doi }}">{{ paper.data.doi }}</a>
	</li>	
</ul>
<hr/>

{% endfor %}