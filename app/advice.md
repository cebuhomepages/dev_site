---

layout:     post-with-cards
title:      Help you need

nav_list: 
  - href:     "/"
    scrollto: 
    icon:     fa-user
    description: About Luchelle
  - href:     "/listings.html"
    scrollto: 
    icon:     fa-home
    description: I Want to Buy
  - href:     "/advice.html"
    scrollto: 
    icon:     fa-book
    description: I Need Advice
  - href:     "/"
    scrollto: 
    icon:     fa-phone
    description: I Want to Meet You

---

{% for post in site.posts %}
<article class="col-xs-12 col-sm-12 col-md-6 single-card-box single-post">
  <div class="card">
    <div class="card-image">
      <div class="card-img-wrap">
          {% if post.thumbnail_type == 'audio' %}
            <div class="blog-post-thumb waves-effect waves-block waves-light">
            <div class="player" id="audio2" data-file-sec="audios/audio.mp3" data-height="40"></div>
            </div>
          {% elsif post.thumbnail_type == 'video' %}
          <div class="blog-post-thumb videoPost">
          <iframe src="//player.vimeo.com/video/7449107" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
          </div>
          {% elsif post.thumbnail_type == 'multi_image' %}
          <div class="blog-post-thumb waves-effect waves-block waves-light">
          <div class="thumb-slides-container">
            <img class="activator" src="http://placehold.it/350x200" alt="">
            <img class="activator" src="http://placehold.it/350x200" alt="">
            <img class="activator" src="http://placehold.it/350x200" alt="">
          </div>
        </div>
          {% else %}
          <div class="blog-post-thumb waves-effect waves-block waves-light">
          <a href="single.html"><img class="activator" src="http://placehold.it/350x200" alt="">
          </a>
        </div>
          {% endif %}
        
        <div class="post-body">
          <a href="single.html" class="post-title-link"><h2 class="green-text post-title">{{ post.title }}</h2></a>
          <p class="post-content">In consectetuer turpis ut velit. Sed lectus. Ut varius tincidunt libero. Vivamus euismod mauris. Vestibulum fringilla pede sit amet augue. Ut varius tincidunt libero. Pellentesque dapibus hendrerit tortor. </p>
        </div>
      </div>
    </div>
    <div class="clearfix card-content">
      <a href="#" class="left js-favorite" title="Love this"><i class="mdi-action-favorite"></i><span class="numb">23</span></a>
      <a href="{{ site.baseurl }}{{ post.url }}" class="green-text right">read more</a>
    </div>
  </div>
</article> <!--./single post-->
{% endfor %}