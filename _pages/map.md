---
title: "Map"
permalink: /map/
layout: page
nav: true
nav_order: 3
---

This research map provides an overview of my work within the field of Precision Agriculture, mainly focusing on Precision Livestock Farming and Precision Crop Farming. The map outlines my leading and participating roles in various projects involving pigs, dairy cows, and crops, where I utilize advanced technologies such as computer vision and machine learning. Each project is linked to corresponding academic outputs, including conference presentations and journal papers, reflecting the interdisciplinary nature of my research.

<!-- Embed the XMind Viewer -->

<div style="max-width: 100%; height: 600px;">
  <div id="mount"></div> <!-- The xmind map will be embedded here -->
</div>

<script src="https://unpkg.com/xmind-embed-viewer/dist/umd/xmind-embed-viewer.js"></script>

<script>
  const init = async () => {
    // Ensure the file path is correct
    const res = await fetch('{{ site.baseurl }}/assets/img/PrecisionAgriculture.xmind');
    
    if (!res.ok) {
      console.error("Failed to load XMind file. Please check the file path.");
      return;
    }

    const viewer = new XMindEmbedViewer({
      el: '#mount',
      file: await res.arrayBuffer(),
      region: 'global', // Change to 'cn' if needed for China region
      styles: {
        'height': '600px', // Adjust height to accommodate your map
        'width': '100%',   // Full width to fit the page
        'overflow': 'auto' // Enable scrolling if content overflows
      }
    });

    // Log when the map is ready
    viewer.addEventListener('map-ready', () => console.log('XMind map is ready!'));
  };

  // Initialize the map
  init();
</script>
