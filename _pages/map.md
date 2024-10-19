---
title: "Map"
permalink: /map/
layout: page
nav: true
nav_order: 3
---

This research map provides an overview of my work within the field of Precision Agriculture, mainly focusing on Precision Livestock Farming and Precision Crop Farming. The map outlines my leading and participating roles in various projects involving pigs, dairy cows, and crops, where I utilize advanced technologies such as computer vision and machine learning. Each project is linked to corresponding academic outputs, including conference presentations and journal papers, reflecting the interdisciplinary nature of my research.

<div style="text-align: center;">
  <img src="{{ site.baseurl }}/assets/img/PrecisionAgriculture.jpg" alt="Mind Map" style="max-width: 100%; height: auto;">
</div>


<div style="overflow: auto; max-width: 50%; height: 300px; margin: 0 auto;">
  <div id="mount" style="height: 50%; width: 100%;"></div>
</div>

<script src="https://unpkg.com/xmind-embed-viewer/dist/umd/xmind-embed-viewer.js"></script>
<script>
  const init = async () => {
    const res = await fetch('{{ site.baseurl }}/assets/img/PrecisionAgriculture.xmind');
    const viewer = new XMindEmbedViewer({
      el: '#mount',
      file: await res.arrayBuffer(),
      region: 'global',
      styles: {
        'height': '300px',  // adjust height here
        'width': '50%'
      }
    });
    viewer.addEventListener('map-ready', () => console.log('Map is ready'));
  }
  init();
</script>



