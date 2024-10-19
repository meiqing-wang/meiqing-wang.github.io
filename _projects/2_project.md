---
layout: page
title: An end-to-end approach to monitor the respiration rate of dairy cows
description: 
img: assets/img/3.jpg
importance: 2
category: work
giscus_comments: false
---

# <span style="font-size: 20px;">Project Background and Objective</span>

Respiratory rate (RR) is an important indicator of the health and welfare status of dairy cows. In recent years, progress has been made in monitoring the RR of dairy cows using video data and learning methods. However, existing approaches often involve multiple processing modules, such as region of interest (ROI) detection and tracking, which can introduce errors that propagate through successive steps. The objective of this project was to develop an end-to-end computer vision method to predict RR of dairy cows continuously and automatically. 

# <span style="font-size: 20px;">Model</span>

The method leverages the capabilities of a state-of-the-art Transformer model, [VideoMAE](https://proceedings.neurips.cc/paper_files/paper/2022/hash/416f9cb3276121c42eebb86352a4354a-Abstract-Conference.html), which divides video frames into patches as input tokens, enabling the automated selection and featurization of relevant regions, such as a cow's abdomen, for predicting RR. The original encoder of VideoMAE was retained, and a classification head was added on top of it. 

# <span style="font-size: 20px;">Data Collection</span>

 We collected data from 6 dairy cows (1 Holstein Friesian and 5 Brown Swiss) across 3 periods (period 1: November 2022; period 2: May 2023; period 3: June 2023). Each period involved 2 cows, and each cow was individually kept in her designated stall in a tie-stall barn. For each cow, 2 2D cameras (DAHUA, model: DH-SD1A404XBGNR, 2.8 mm–12 mm lens) were installed: one on the side and one above, to capture abdominal movements related to respiration. The cameras were linked to a DAHUA network video recorder (NVR, model: DHINVR4216–16P-4KS2/L). The positions of the cameras and the infrastructure of the data collection system are illustrated in the picture below.

 <div style="text-align: center;">
   <img src="{{ site.baseurl }}/assets/img/project2-1.jpg" alt="Data Collection Setup" style="max-width: 100%; height: auto;">
</div>





