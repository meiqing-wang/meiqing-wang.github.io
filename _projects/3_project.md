---
layout: page
title: Long-term tracking of Holstein cows in free-stall barn environment
description: Continuous identification and tracking of dairy cows using computer vision
img: assets/img/7.jpg
importance: 3
category: work
---

# <span style="font-size: 20px;">Project Background and Objective</span>

Continuous tracking of individual dairy cows supports automated monitoring of behaviour, health, and welfare. However, conventional multi-object tracking methods can lose an animal's identity when it leaves the camera's field of view and later returns. This project developed a tracking-by-classification approach to identify and continuously track Holstein cows in a free-stall barn.

# <span style="font-size: 20px;">Data Collection</span>

Video data were collected from 13 lactating Holstein cows at the AgroVet-Strickhof research dairy farm in Lindau, Switzerland. Two cameras recorded the enclosure from opposite sides during the day and at night. The datasets included 1,005 annotated frames for cow detection, 7,889 cow images for individual classification, and six test videos ranging from 5 minutes to 1 hour, with cows repeatedly leaving and re-entering the field of view.

# <span style="font-size: 20px;">Tracking-by-Classification Method</span>

A YOLOv8 detector first locates the cows in each frame, and a YOLOv8 classifier then estimates the identity probabilities for each detected animal. A two-stage Hungarian matching process associates detections with cow identities, prioritising high-confidence predictions before matching the remaining detections. The method was compared with SORT, DeepSORT, ByteTrack, and TrackFormer.

<div style="text-align: center;">
  <img src="{{ site.baseurl }}/assets/img/7.jpg" alt="Individual Holstein cows identified and tracked in a free-stall barn" style="max-width: 100%; height: auto;">
</div>

# <span style="font-size: 20px;">Results and Resources</span>

Across the six test videos, the method achieved an average IDF1 of 0.946, HOTA of 0.929, and MOTA of 0.894. It maintained cow identities particularly well in longer recordings with repeated re-entry, demonstrating its potential for integration with automated behaviour and health monitoring systems.

The [paper](https://doi.org/10.1016/j.biosystemseng.2026.104420), [source code](https://github.com/meiqing-wang/Cow-TrackingbyClassification), and [dataset](https://doi.org/10.3929/ethz-c-000796658) are publicly available. Daytime and nighttime tracking demos can also be found on the [GitHub project page](https://github.com/meiqing-wang/Cow-TrackingbyClassification#demos).


