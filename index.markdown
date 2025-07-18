---
layout: default
---
  <main class="main-content">
  <div class="left-column">
  {% assign lead_posts = site.posts | where:"section","lead" %}
  {% for post in lead_posts %}
  <article class="lead-story">
  <h2 class="lead-headline">{{ post.title }}</h2>
  <p class="lead-summary">{{ post.summary }}</p>
  <p class="byline">{{ post.byline }}</p>
  <div class="article-content">
  {{ post.content }}
  </div>
  </article>
  {% endfor %}
  <section class="secondary-stories">
  {% assign secondary_posts = site.posts | where:"section","secondary" %}
  {% for post in secondary_posts %}
  <article class="story">
  <h3 class="story-headline">{{ post.title }}</h3>
  <p class="story-summary">{{ post.summary }}</p>
  <p class="story-text">{{ post.content }}</p>
  </article>
  {% endfor %}
  </section>
  </div>
  
  <aside class="right-column">
  <div class="sidebar">
  <h3 class="sidebar-headline">Music Industry News</h3>
  {% assign sidebar_posts = site.posts | where:"section","sidebar" %}
  {% for post in sidebar_posts %}
  <article class="sidebar-story">
  <h4 class="sidebar-story-headline">{{ post.title }}</h4>
  <p class="sidebar-story-text">{{ post.content }}</p>
  </article>
  {% endfor %}
  </div>
  </aside>
  </main>
  
  <section class="bottom-stories">
  {% assign bottom_posts = site.posts | where:"section","bottom" %}
  {% for post in bottom_posts %}
  <article class="bottom-story">
  <h3 class="bottom-headline">{{ post.title }}</h3>
  <p class="bottom-text">{{ post.content }}</p>
  </article>
  {% endfor %}
  </section>

