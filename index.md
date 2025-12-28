---
layout: default
title: terminal
---

<div class="system-status">
  <span>STATUS: OPERATIONAL</span>
  <span>SESSION_START: {{ site.time | date: "%Y.%m.%d %H:%M" }} UTC</span>
  <span>OPERATOR: sysnomad</span>
</div>


<div class="terminal-intro">
  <p class="command">> sysinfo -sysnomad</p>
  <div class="sysinfo-box">
    <strong>sysnomad</strong> | chronicler of glitches, observer of film, memory, and human absurdity. 
    <br>All logs are raw; errors expected.
  </div>
</div>

<div class="log-directory">
  <p class="command">> ls ./logs</p>
  <ul class="terminal-list">
    {% for post in site.posts %}
    <li>
      <span class="prompt">></span> 
      <span class="log-id">log_{{ post.date | date: "%j" }}:</span> 
      <a href="{{ post.url }}">{{ post.title | downcase }}</a> 
      <span class="arrow">→</span>
    </li>
    {% endfor %}
  </ul>
</div>