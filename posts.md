---
title: Posts
layout: default
---

<div class="home">

  <h2 class="page-heading">Todos os posts publicados até o momento</h2>
  <p><em>
  OBS: Neste endereço encontram-se meus posts mais atualizados,
  eu congelei meus posts mais antigos neste
  <a href="http://adlermedrado.com.br/all-posts.html">local</a> para fins
  de histórico apenas.
  </em></p>

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%d/%m/%Y" }}</span>
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">Assine <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
