---
title: Gallery
permalink: /gallery
---



{% assign externalgallery = "
https://via.placeholder.com/600x1200,
https://via.placeholder.com/130,
https://via.placeholder.com/800x500,
https://via.placeholder.com/800x600,
https://via.placeholder.com/600x800,
https://via.placeholder.com/900x1200,
https://via.placeholder.com/900x1300,
https://via.placeholder.com/900x2200,
https://via.placeholder.com/1200x900,
https://via.placeholder.com/2200x900,
https://via.placeholder.com/750/x325,
https://via.placeholder.com/2200,
https://via.placeholder.com/600,
https://via.placeholder.com/700x500" %}

# External normalised 

{% include_cached snippets/carousel.html indicators="true" controls="true" normalize="true" external=externalgallery %}

# External normalised

{% include_cached snippets/carousel.html controls="true" external=externalgallery %}


