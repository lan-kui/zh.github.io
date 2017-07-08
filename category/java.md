---
layout: page
title: Java
---


{% for post in paginator.posts %}
    {% if post.categories.java %}
        <div class="post-preview">
            <a href="{{ post.url | prepend: site.baseurl }}">
                <h2 class="post-title">            
                    {{ post.title }}
                </h2>
                {% if post.subtitle %}
                <h3 class="post-subtitle">
                    {{ post.subtitle }}
                </h3>
                {% endif %}
                <div class="post-content-preview">
                    {{ post.content | strip_html | truncate:150 }}
                </div>
            </a>
            <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
        </div>
        <hr>
    {% endif %}
{% endfor %}