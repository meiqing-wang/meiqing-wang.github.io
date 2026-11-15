---
layout: page
title: MushroomSegDepth for oyster mushroom growth monitoring
description: Joint segmentation and depth prediction from RGB images
img: assets/img/project4-cover.jpg
importance: 4
category: work
github: https://github.com/meiqing-wang/MushroomSegDepth
---

# <span style="font-size: 20px;">Project Background and Objective</span>

Reliable monitoring of oyster mushroom growth is important for determining harvest time, maintaining product quality, and improving yield management. RGB images provide useful information about size and shape but do not directly capture the three-dimensional structure of mushroom clusters. This project developed MushroomSegDepth, a multitask model that jointly segments oyster mushrooms and predicts depth from standard RGB images.

# <span style="font-size: 20px;">Data Collection</span>

Data were collected from 19 to 26 May 2025 under farm conditions at the Greenacre facility of University College Dublin. Three Intel RealSense D435i cameras captured RGB images and corresponding depth maps from top, front, and side views at 30-minute intervals. After quality control, the dataset contained 705 paired RGB-depth samples. Mushroom regions were manually annotated in CVAT, and the data were divided into training, validation, and test sets using a 70:15:15 ratio.

# <span style="font-size: 20px;">Model</span>

MushroomSegDepth combines a ConvNeXt encoder, a Feature Pyramid Network, a pyramid-fusion module, and separate heads for segmentation and depth prediction. The shared multi-scale features allow the model to learn both mushroom boundaries and fine geometric variations. Depth supervision is applied only within valid mushroom regions, reducing the influence of irrelevant background pixels.

# <span style="font-size: 20px;">Results and Demos</span>

The ConvNeXt-tiny configuration achieved an Intersection over Union of 0.935 for segmentation and a depth Root Mean Square Error of 26.1 mm. Predicted depth trends closely followed the ground-truth changes during the growth cycle, providing complementary information to two-dimensional area measurements for identifying maturity and supporting harvest-timing decisions. The method also showed favourable performance compared with Depth Anything v2, DepthPro, and Marigold while remaining lightweight and computationally efficient.

The first demo presents paired RGB and depth timelapse images during mushroom development.

<div style="text-align: center;">
  <video controls loop muted playsinline preload="metadata" style="max-width: 100%; height: auto;">
    <source src="{{ site.baseurl }}/assets/img/project4-1.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

<br>

The second demo shows selected mushroom clusters, their corresponding depth maps, and their area-growth curves over time.

<div style="text-align: center;">
  <video controls loop muted playsinline preload="metadata" style="max-width: 100%; height: auto;">
    <source src="{{ site.baseurl }}/assets/img/project4-2.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

<br>

The [paper](https://doi.org/10.1016/j.compag.2026.111680) and [source code](https://github.com/meiqing-wang/MushroomSegDepth) are publicly available.
