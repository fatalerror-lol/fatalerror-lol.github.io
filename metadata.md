---
layout: default
title: metadata
---

<div class="command">> query --all-signals</div>

{% comment %} 
  This logic looks through all your posts and finds every unique 'signal' 
{% endcomment %}

<div class="signal-map">
  {% assign all_signals = "" | split: "," %}
  {% for post in site.posts %}
    {% assign post_signals = post.signal | split: " / " %}
    {% assign all_signals = all_signals | concat: post_signals | uniq | sort %}
  {% endfor %}

  {% for signal in all_signals %}
	<section id="{{ signal | slugify }}" class="signal-group">
	  <h4># {{ signal | upcase }}</h4>
	  <ul class="terminal-list"> {% for post in site.posts %}
		  {% if post.signal contains signal %}
			<li>
			  <span class="prompt">></span>
			  <span class="log-id">log_{{ post.date | date: "%j" }}:</span>
			  <a href="{{ post.url }}">{{ post.title | downcase }}</a>
			</li>
		  {% endif %}
		{% endfor %}
	  </ul>
	</section>
  {% endfor %}
</div>



