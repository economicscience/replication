---
title: Economic Science Association Repository for Replication Packages
layout: default
---

<img src="https://economicscience.org/images/esa/logo-dark.png"
     class="rounded float-end ml-5"
	 />

### Economic Science Association Repository for Replication Packages

<p class="lead">
In 2021 the
<a href="https://economicscience.org">Economic Science Association</a>
implemented a new
<strong>Data and Replication Policy</strong>.
The policy requires authors of manuscripts published in the ESA journals
(<em>Experimental Economics</em> and
<em>Journal of the Economic Science Association</em>) to publish,
in a trusted online repository, any documentation necessary
to reproduce or replicate their study.
</p>

On this webpage, we provide a log of the replication packages published since the policy was implemented.
In addition, we aim to log any replications of these articles that we are aware of. 

Examples of repositories used by authors of papers in
*Experimental Economics* and *JESA* include the
[Harvard Dataverse](https://dataverse.harvard.edu),
[OSF](https://osf.io),
[Zenodo](https://zenodo.org),
and
[OpenICPSR](https://www.openicpsr.org/openicpsr/). 

Useful links:

* [Current version of the ESA Data and Replication Policy](https://economicscience.org/page/replication-policy)
* [A curated list of trusted repositories](https://social-science-data-editors.github.io/guidance/Requested_information_hosting.html#trusted-repositories)


### Index of replication materials


{% for paper in site.data.papers %}
<div class="card my-2">
  <div class="card-header">
    {% if paper.article.doi != null %}
	<a href="{{ paper.article.doi }}">
	{% endif %}
	{{ paper.title }}
	{% if paper.article.doi != null %}
	</a>
	{% endif %}
	</div>
	<div class="card-body">
		<b>Authors:</b>
	    {{ paper.authors | map: "name" | join: "; " }}
	<br/>
       <b>Link to data:</b>
	   <a href="{{ paper.data.doi }}">{{ paper.data.doi }}</a>
    </div>
</div>

{% endfor %}
