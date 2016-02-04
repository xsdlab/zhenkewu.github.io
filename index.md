---
layout: default
title: Zhenke Wu, PhD
categories:
 - home
---
{% include JB/setup %}
{% for page in site.categories.misc %}
{% if page.homepage %}
	{% assign homepage = page %}
{% endif %}
{% endfor %}

<div class="row">
	<div class="col-md-12">
		<object class="pull-left biglogo" data="assets/themes/lab/images/logo/logo-none.svg" type="image/svg+xml"></object>
		<div class="bigtitle logobox">
			Zhenke Wu Research
		</div>
	</div>				
</div>

<div class="bigspacer"></div>
			
My main research interests include:

* Bayesian hierarchical models: biomarkers, data integration, scalable computation, model-averaging;
* Latent variable models: measurement errors, local dependence, partial-identifiability; 
* Robust inference: bias reduction, efficiency enhancement by covariate-calibration, semiparametric locally efficient estimation, deductive inference;
* Causal analysis of modern study designs;
* Collaborations: infectious disease, medical diagnosis, epidemiology, health policy.

<div class="bigspacer"></div>
<hr/>
<div class="bigspacer"></div>
I am a postdoctoral fellow in the [Department of Biostatistics](http://www.jhsph.edu/departments/biostatistics/) at [Johns Hopkins University](http://www.jhsph.edu/). I am advised by Professor [Scott Zeger](http://www.jhsph.edu/faculty/directory/profile/3859/Zeger/Scott), and work closely with [Hopkins inHealth](http://hopkinsinhealth.jhu.edu/) methodology group, [Causal Inference Working Group](http://jhsphcausalinference.weebly.com/), and [International Vaccine Access Center (IVAC)](http://www.jhsph.edu/research/centers-and-institutes/ivac/).

<br />
I conduct reasearch on the design and application of statistical methods that inform health decisions made by individuals, or precision medicine. My current focus is on latent variable and causal inference
methods that can support disease etiology studies, medical diagnosis, and health policy evaluation. Broadly, the statistical goal is to discover simple latent structures that improve inferences and population parameters and individual latent states. I have also worked on causal inference methods 1) to evaluate novel treatment rules under special designs like matched-pair cluster randomized design, as these designs are useful for interventions that can only be applied at cluster level; and 2) to facilitate the inference for novel estimands in semiparametric models by automating and unifying the derivation of efficient influence functions (EIF) and ensuing estimation.

<br />
Currently a major focus of my work is on the analysis of multiple mixed-type longitudinal measurements with feedbacks in treatment assignments. I am working on hierarchical Bayesian methods to to infer latent trajectories that represent individual disease progressions that have direct applications to childhood pneumonia etiology studies and disease surveillance.


<br />
[Here](/papers/) are my publication samples. My CV is [here](/assets/pdfs/team/zhenkewu-cv.pdf). My contact info is [here](/team/zhenke-wu)

<br />
[**Click Here for the Pronounciation of My Name**](https://soundcloud.com/zhenke-wu/zhenke-wu-name)


<div class="bigspacer"></div>

<hr/>

<div class="row">
	<div class="col-md-12">
		<div class="head">
			{{ homepage.content }}
		</div>
	</div>				
</div>

<div class="hugespacer"></div>

<div class="row">
	
	<div class="col-md-4">
		<div class="head">
			<a class="off" href="/news/">News</a>
		</div>
		<div class="bigspacer"></div>
		<div class="feedbox pad-left">
			{% for news in site.categories.news limit:4 %}
			
				{% for member in site.categories.team %}
					{% if member.handle == news.author_handle %}
						{% assign author = member %}
					{% endif %}
				{% endfor %}		
				
				<div class="note-title">
					<i class="fa fa-bullhorn"></i>
					<a class="off" href="{{ news.url }}">
					{{ news.title }}
					</a>
				</div>
				<div class="note">
					{{ news.content }}
				</div>
				<div class="smallspacer"></div>
				<div class="smallnote">
					Posted
					{{ news.date | date_to_string }}
					{% if author %}
					by <a class="off" href="{{ author.url }}">{{ author.handle }}</a>
					{% endif %}						
				</div>
				<div class="spacer"></div>	
				<div class="spacer"></div>				
			{% endfor %}
		</div>
		<div class="bigspacer"></div>		
	</div>
	
	
	<div class="col-md-4">
		<div class="head">
			<a class="off" href="/papers/">Recent Papers
			</a>
		</div>
		<div class="bigspacer"></div>
		<div class="feedbox pad-left">		
			{% for paper in site.categories.papers limit:4 %}
				<div class="note-title">
					<i class="fa fa-file-text-o fa-fw"></i>
					<a class="off" href="{{ paper.url }}">
					{{ paper.title }}
					</a>
					<br/>
					<div class='shortref note'>
					{{ paper.shortref }}
					</div>
				</div>
				<div class="smallspacer"></div>
				<div class="smallnote">
					Published
					{{ paper.date | date_to_string }}
				</div>
				<div class="spacer"></div>	
				<div class="spacer"></div>				
			{% endfor %}
		</div>
		<div class="bigspacer"></div>		
	</div>
	

	<div class="col-md-4">
		<div class="head">
			<a class="off" href="/blog/">Blogs</a>
		</div>
		<div class="bigspacer"></div>
		<div class="feedbox pad-left">
			{% for blog in site.categories.blog limit:4 %}
				<div class="note-title">
					<i class="fa fa-comment-o fa-fw"></i>
					<a class="off" href="{{ blog.url }}">
					{{ blog.title }}
					</a>
					<br/>
					<div class='shortref note'>
					{{ blog.description }}
					</div>
				</div>
				
				<div class="smallspacer"></div>
				<div class="smallnote">
					Posted
					{{ blog.date | date_to_string }}
					{% if author %}
					by <a class="off" href="{{ author.url }}">{{ author.handle }}</a>
					{% endif %}						
				</div>
				<div class="spacer"></div>	
				<div class="spacer"></div>
				
				<div class="smallspacer"></div>
				<div class="spacer"></div>
				<div class="spacer"></div>
			{% endfor %}
		</div>
		<div class="bigspacer"></div>
	</div>
	
	<!-- <div class="col-md-4">
		<div class="head">
			<a class="off" href="/projects/">Projects</a>
		</div>
		<div class="bigspacer"></div>
		<div class="feedbox pad-left">
			{% for project in site.categories.project limit:4 %}
				<div class="note-title">
					<i class="fa fa-terminal"></i>
					<a class="off" href="{{ project.url }}">
					{{ project.title }}
					</a>
					<br/>
					<div class='shortref note'>
					{{ project.tags }}
					</div>
				</div>
				<div class="smallspacer"></div>
				<div class="spacer"></div>
				<div class="spacer"></div>
			{% endfor %}
		</div>
		<div class="bigspacer"></div>
	</div> -->


</div>

<div class="bigspacer"></div>
