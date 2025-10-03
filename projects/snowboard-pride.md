---
layout: default
title: 'Snowboard Pride'
---

{% capture text-block %}
Ces portraits ont été réalisés entre 2007 et 2012 dans diverses stations de ski en France.
En reprenant les codes des photographies de rue et documentaires, à la manière de August Sander, cette série témoigne de la diversité des styles vestimentaires et de l'enthousiasme de la tribu des snowboarders. 
L'utilisation d'un appareil argentique ancien (Agfa Isolette III) m'a permis d'établir un pont entre les genres et les époques photographiques tout en donnant au moment de la prise de vue un caractère insolite.
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