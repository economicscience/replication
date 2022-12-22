---
title: Economic Science Association Repository for Replication Packages
---

# Economic Science Association Repository for Replication Packages

In 2021 the Economic Science Association implemented a new **Data and Replication Policy**.
The policy requires authors of manuscripts published in the ESA journals
(*Experimental Economics* and the *Journal of the Economic Science Association*) to publish,
in a trusted online repository, any documentation necessary
to reproduce or replicate their study.

On this webpage, we provide a log of the replication packages published since the policy was implemented.
In addition, we aim to log any replications of these articles that we are aware of. 

Examples of often used repositories among the authors of *Experimental Economics* and *JESA* include
the Harvard Dataverse, OSF, Zenodo or the OpenICPSR. 

Useful links:

* [The ESA Data and Replication Policy](https://economicscience.org/page/replication-policy)
* [A curated list of trusted repositories](https://social-science-data-editors.github.io/guidance/Requested_information_hosting.html#trusted-repositories)


### Index of replication materials


{% for paper in site.data.papers %}

<ul>
	<li>
		<b>Title:</b> 
		{% if paper.article.doi != null %}
		<a href="{{ paper.article.doi }}">
		{% endif %}
		{{ paper.title }}
		{% if paper.article.doi != null %}
		</a>
		{% endif %}
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
