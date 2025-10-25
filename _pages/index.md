---
layout: page
title: Home
id: home
permalink: /
---

# Home 🌱

<p>Studying the Tao <br>
of modern life.</p>

<p>Here you will discover <br>
a bunch of notes and ideas <br>
from unrelated topics like <br>
<span title="There is no note that matches this link." class="invalid-link">  <span class="invalid-link-brackets">[[</span>  taoism  <span class="invalid-link-brackets">]]</span></span>, <span title="There is no note that matches this link." class="invalid-link">  <span class="invalid-link-brackets">[[</span>  fitness  <span class="invalid-link-brackets">]]</span></span>, philosophy, psychology, cooking, programming, entrepreneurship,  agriculture, money, languages, music, house, social, books, anime or films.</p>

<blockquote>
  <p>
A Digital Garden is an online space <br>
forming an evolving collection of <br>
interconnected notes, ideas and resources.</p>
</blockquote>

<p>This project came to life <br>
thanks to the concepts of <br>
<a class="internal-link" href="/linking-your-thinking">Linking your thinking</a>, <br>
<span title="There is no note that matches this link." class="invalid-link">  <span class="invalid-link-brackets">[[</span>  Building in public  <span class="invalid-link-brackets">]]</span></span> and <br>
the Chapter 81 from the <br>
Tao Te Ching.</p>

<h3 id="how-to-navigate-this-site">How to navigate this site</h3>

<ol>
  <li>
<strong>Links and Backlinks</strong>: As a free pirate, you can randomly navigate through notes using the links and connections from each note.</li>
  <li>
<strong>Main Index</strong>: When you get trapped in a rabbit hole, feel free to click on the top-left main title <code class="language-plaintext highlighter-rouge">Digital Taoist</code> to go back to this starter note.</li>
  <li>
<strong>Visual Graph</strong>: If you happen to be a visual thinker just like me, a visual graph is added at the bottom of each note showcasing the connections between notes. Just click on the dots to teleport yourself into that idea.</li>
</ol>

<blockquote>
  <p>[!hint] Building your own Digital Garden <br>
If you happen to love this idea <br>
of digital gardening, <br>
please follow this guide <br>
to start sharing with the world <br>
your inner universe: <a href="https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll" target="_blank">Setting up your own digital garden with Jekyll — Maxime Vaillancourt</a></p>
</blockquote>

<p>As Alan Watts once said:</p>

<blockquote>
  <p>I just want you to enjoy, <br>
a point of view which <br>
I enjoy.</p>
</blockquote>

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
