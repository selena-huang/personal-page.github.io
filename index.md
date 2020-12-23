## This is my public repos listing page

The following repos are all open source projects. The routine-recommendation is for COMS 4995 - Open Source Development.

{% assign orderedRepos = site.github.public_repositories | sort: 'stargazers_count' | reverse %}
{% for repository in orderedRepos %}
{% assign homepageLength = repository.homepage | size %}
{% if homepageLength > 0 %}
### {{repository.name}} | [repo]({{ repository.html_url }}) | [pages]({{ repository.homepage }}) 
{% else %}
### {{repository.name}} | [repo]({{ repository.html_url }})
{% endif %}
<div style="border-left: 3px solid #CCC; padding-left: 10px; margin-bottom: 30px">
<i>{{repository.description}}</i>
<p style="margin-top: 5px"><span style="margin-right:10px">{% octicon repo-forked size:small%} {{repository.forks_count}}</span> {% octicon star size:small %} {{repository.stargazers_count}} </p>
</div>

{% endfor %}

I also worked on another project for a different class, which will also be open source:

### [MyBind3r](https://github.com/salvolpe/MyBind3r)
We want to create an online version of the binders that stage managers use in theater. This would help with digitalizing their notes, and smoother communication in this post-corona world. 
