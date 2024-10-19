---
title: "Map"
permalink: /map/
layout: page
nav: true
nav_order: 3
---

This research map provides an overview of my work within the field of Precision Agriculture, mainly focusing on Precision Livestock Farming and Precision Crop Farming. The map outlines my leading and participating roles in various projects involving pigs, dairy cows, and crops, where I utilize advanced technologies such as computer vision and machine learning. Each project is linked to corresponding academic outputs, including conference presentations and journal papers, reflecting the interdisciplinary nature of my research. 


<!-- Embed the XMind Viewer -->

<div style="max-width: 1280px">
  <div id="mount"></div> <!-- The xmind map will be embedded here -->
</div>

<script src="{{ site.baseurl }}/assets/js/xmind-embed-viewer.js"></script>
<script>
  const init = async () => {
    const res = await fetch('{{ site.baseurl }}/assets/img/PrecisionAgriculture.xmind');  // Adjust the path to your xmind file if necessary
    const viewer = new XMindEmbedViewer({
      el: '#mount',
      file: await res.arrayBuffer(),
      region: 'global',
      styles: {
        'height': '500px',
        'width': '100%'
      }
    });

    viewer.addEventListener('map-ready', () => console.log('Map is ready'));
  }

  init();
</script>

