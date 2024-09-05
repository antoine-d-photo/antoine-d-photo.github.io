---
layout: default
title: 'Snowboard Pride'
---

{% capture text-block %}
Entre 2007 et 2012, muni d'un appareil photo moyen format ancien, j'ai réalisé ces protraits de snowboarders dans diverses stations de ski en France.
{% endcapture %}

{% capture gallery-block %}
      <script  type="module">
        import PhotoSwipeLightbox from 'https://unpkg.com/photoswipe/dist/photoswipe-lightbox.esm.js';
        
        const lightbox = new PhotoSwipeLightbox({
          gallery: '#my-gallery',
          children: 'a',
          pswpModule: () => import('https://unpkg.com/photoswipe'),
        });
        
        lightbox.init();
      </script>

      <div class="pswp-gallery" style="" id="my-gallery">
        {% for snowbord-pride-images in site.data.snowboard-pride-images %}
          <a
            href="{{ site.github.url }}/assets/img/projects/snowboard-pride/{{ snowbord-pride-images.image-name }}"
            data-pswp-width="500"
            data-pswp-height="500"
            target="_blank"
          >
            <img
              src="{{ site.github.url }}/assets/img/projects/snowboard-pride/thumbs/{{ snowbord-pride-images.image-name }}"
              width="100"
              height="100"
              alt=""
            />
          </a>
        {% endfor %}
      </div>
{% endcapture %}

{% include main-text-and-gallery.html %}