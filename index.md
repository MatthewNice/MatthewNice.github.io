---
layout: default
title: "Matt Nice's Personal Website"
---

<main role="main" class="container-sm" style="max-width: 1080px">
    <div class="row">
        <div class="col">
            <p class="h1 mt-5 page-title">
                <img class="profile-img-small d-md-none" src="{{ '/assets/profile.jpg' | relative_url }}" />
                <span style="clear: right">Matthew W. Nice</span>
            </p>
            <p class="h4 section-title" style="clear: right">About</p>
            {% capture bio %}{% include bio.md %}{% endcapture %}
            <p>{{ bio | markdownify }}</p>

        </div>
        <div class="col-auto d-none d-md-block">
            <img class="profile-img" src="{{ '/assets/profile.jpg' | relative_url }}" />
        </div>
    </div>

    <div class="row">
        <div class="col">
    <p class="h4 section-title" style="clear: right">Featured Videos</p>

    <iframe width="560" height="315" src="https://www.youtube.com/embed/slH9nimpaY8?si=3PwOdrJrvqv7O7ny" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

    {% capture feature_videos0 %}{% include feature_videos0.md %}{% endcapture %}
    <p>{{ feature_videos0 | markdownify }}</p>

  <iframe width="560" height="315" src="https://www.youtube.com/embed/gFwJfEvnogI?si=T1jwTFf3AnHoIrxM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

  {% capture feature_videos %}{% include feature_videos.md %}{% endcapture %}
  <p>{{ feature_videos | markdownify }}</p>

      </div>
  </div>

    <div class="row">
        <div class="col">


          {% capture awards %}{% include awards.md %}{% endcapture %}
          <p>{{ awards | markdownify }}</p>


        </div>
    </div>

    <div class="row">
        <div class="col">
            <p class="h4 section-title">Selected Publications <span class="h6">(*: equal contribution)</span></p>
            <div class="container-fluid" style="padding: 0;">
                {% assign sorted_publications = site.publications | sort:"date" %}
                {% for publication in sorted_publications reversed %}
                <div class="row" style="padding: 0.25rem 0">
                    <div class="col">
                        <p class="h5 publication-title">{{ publication.title }}</p>
                        <span class="publication-authors">{{publication.authors | markdownify}}</span>
                        {% if publication.venue %}
                            <span class="publication-venue">{{publication.venue | markdownify}}</span>
                        {% endif %}
                        <p class="publication-excerpt" style="display: none"> {{publication.excerpt}} </p>
                        <!-- <p>{{ publication.content }}</p> -->
                        {% if publication.paper_url %}
                        <p class="publication-links"> <a href="{{publication.paper_url}}">Paper</a>
                        {% if publication.blog_url %}/ <a href="{{publication.blog_url}}">Blog Post</a>{% endif %}
                        {% if publication.project_page_url %}/ <a href="{{publication.project_page_url}}">Project Page</a>{% endif %}
                        {% if publication.demo_url %}/ <a href="{{publication.demo_url}}">Demo</a>{% endif %}
                        {% if publication.video_url %}/ <a href="{{publication.video_url}}">Video</a>{% endif %}
                        {% if publication.demo_video_url %}/ <a href="{{publication.demo_video_url}}">Demo Video</a>{% endif %}
                        {% if publication.code_url %}/ <a href="{{publication.code_url}}">Code</a>{% endif %}
                        {% if publication.poster %}/ <a href="{{'/assets/posters/' | append: publication.poster | relative_url }}">Poster</a>{% endif %}
                        {% if publication.bibtex_url %}/ <a href="{{publication.bibtex_url}}">BibTex</a>{% endif %}
                        {% if publication.excerpt %}/ <a href="" class="tldr_btn" role="button">TL;DR</a>{% endif %}
                        </p>
                        {% endif %}
                    </div>
                    {% if publication.cover_image %}
                    <div class="col-5 d-none d-md-block align-self-center">
                        <img class="cover-image" src="{{'/assets/cover_images/' | append: publication.cover_image | relative_url }}" />
                    </div>
                    {% endif %}
                </div>
                {% endfor %}
            </div>
        </div>
    </div>

    <div class="row">
        <div class="col">

        {% capture service %}{% include service.md %}{% endcapture %}
        <p>{{ service | markdownify }}</p>

        </div>
    </div>
    <div class="row">
        <div class="col">

        {% capture opensource %}{% include opensource.md %}{% endcapture %}
        <p>{{ opensource | markdownify }}</p>

        </div>
    </div>
</main>

<footer class="footer">
    <div class="container-sm">
        <div class="row">
            <div class="col" style="text-align: center">
            <span class="text-muted">
            {% capture funding %}{% include funding.md %}{% endcapture %}
            <p>{{ funding | markdownify }}</p>
            </span>
                <span class="text-muted">
                    Feel free to use the <a href="https://github.com/MatthewNice/MatthewNice.github.io">source code</a> of this website. References designs from <a href="https://github.com/TonyLianLong/websitev2">Tony Lian</a> and <a href="https://github.com/jonbarron/website">Jon Barron</a>. The fonts are based on <a href="https://checkmyworking.com/cm-web-fonts/">this</a> project. Uses <a href="https://github.com/jekyll/jekyll">Jekyll</a> and <a href="https://getbootstrap.com/">Bootstrap</a>.
                </span>
            </div>
        </div>
    </div>
</footer>
