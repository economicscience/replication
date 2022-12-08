{% for paper in site.data.papers %}

<ul>
	<li>
		<b>Title:</b> {{ paper.title }}
	</li>
	<li>
		<b>Authors:</b>
		{% for author in paper.authors %}
		<ul>
			<li>{{ author.name }}</li>
		</ul>
	</li>
	<li>
		<b>Link to data:</b>
		<a href="{{ paper.data.doi }}">{{ paper.data.doi }}</a>
	</li>	
</ul>


{% endfor %}