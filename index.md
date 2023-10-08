---
layout: home
title: Home
---

<div id="intro-wrapper" class="l-text">
	<div id="intro-title-wrapper">
		<div id="intro-image-wrapper">
			<img id="intro-image" src="/images/seongmin.jpg"></div>
		<div id="intro-title-text-wrapper">
			<h1 id="intro-title">Hi, I'm Seongmin Lee</h1>
			<div id="intro-subtitle">CS PhD student at Georgia Tech 🐝</div>
			<div id="intro-title-socials">
				{% for link in site.data.social-links %}
					{% if link.on-homepage == true %}
						{% include social-link.html link=link %}
					{% endif %}
				{% endfor %}
			</div>
		</div>
	</div>
	<div id="everything-else" class="l-middle">
		<a href="{{ site.url }}/cv"><div><i class="fa fa-portrait icon icon-right-space"></i>CV</div></a>
	</div>
	<div>
		My research bridges <span class="intro-ml">machine learning</span> and <span class="intro-hci">human-computer interaction</span>,
		with the pursuit of realizing <b>Responsible AI</b> through the development of
		<b>visual explanations</b> that empower people to gain a clear understanding of machine learning and
		<b>scalable algorithms</b> that enable reliable and active use of machine learning.
	</div>
	<div style="height: 1rem"></div>
	<div>
		I am pursuing my Ph.D. at Georgia Tech, working with <a href="http://www.cc.gatech.edu/~dchau/">Polo Chau</a>.
		I received my B.S. from Seoul National University, where I was supported by <a href="https://www.kosaf.go.kr/eng/jsp/aid/aid02_01_01.jsp">Presidential Science Scholarship</a>.
	</div>
	<div style="height: 1rem"></div>
	<div>
	 	I have collaborated with researchers and developers of Cisco Systems, Inc. and AVAST Software.
		<!-- I have collaborated with designers, developers, artists, and scientists while working at <img class="intro-logo" style="width: 19px; padding-bottom: 5px;" src="/images/apple.svg"> Apple, <img class="intro-logo" style="width: 18px; padding-bottom: 3px;" src="/images/microsoft.svg"> Microsoft Research, <img class="intro-logo" style="width: 24px" src="/images/nasa.svg"> NASA Jet Propulsion Lab, and <img class="intro-logo" style="width: 24px;" src="/images/pnnl.svg"> Pacific Northwest National Lab. -->
	</div>
</div>

<hr class="l-middle home-hr">

<h2 class="feature-title">Featured <a href="/cv/#publications">Research Publications</a></h2>

<!-- vertical spacing -->
<div style="height:10px"></div>

<div class="cover-wrapper cover-wrapper-3-col l-page">
	{% assign sortedPublications = site.categories.papers | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.featured == true %}
			{% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>





<!-- [gt]: http://www.gatech.edu "Georgia Tech"
[cse]: http://cse.gatech.edu "Georgia Tech Computational Science and Engineering"
[coc]: http://www.cc.gatech.edu "Georgia Tech College of Computing"

[cv]: {{ site.url }}/cv
[polo]: http://www.cc.gatech.edu/~dchau/ "Polo Chau"
[poloclub]: http://poloclub.gatech.edu "Polo Club of Data Science" -->