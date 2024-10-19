---
title: "Map"
permalink: /map/
layout: page
nav: true
nav_order: 3
---

This research map provides an overview of my work within the field of Precision Agriculture, mainly focusing on Precision Livestock Farming and Precision Crop Farming. The map outlines my leading and participating roles in various projects involving pigs, dairy cows, and crops, where I utilize advanced technologies such as computer vision and machine learning. Each project is linked to corresponding academic outputs, including conference presentations and journal papers, reflecting the interdisciplinary nature of my research. 

<!-- Embed the XMind Viewer -->
<div style="max-width: 100%; height: 600px;"">
  <div id="mount"></div> <!-- The xmind map will be embedded here -->
</div>

<!-- Load the xmind-embed-viewer.js from the CDN -->
<script src="https://unpkg.com/xmind-embed-viewer/dist/umd/xmind-embed-viewer.js"></script>

<script>
  const init = async () => {
    const res = await fetch('{{ site.baseurl }}/assets/img/PrecisionAgriculture.xmind');  // Adjust the path to your xmind file if necessary
    const viewer = new XMindEmbedViewer({
      el: '#mount',
      file: await res.arrayBuffer(),
      region: 'global',
      styles: {
        'height': '600px',  // Adjust height if needed
        'width': '100%',    // Full width for better visibility
        'overflow': 'auto'
      }
    });

    viewer.addEventListener('map-ready', () => console.log('Map is ready'));
  }

  init();
</script>
