---
title: Recognizing human actions as the evolution of pose estimation maps
authors: Mengyuan Liu, Junsong Yuan
year: 2018
DOI: 10.1109/CVPR.2018.00127
---

[Notes::
the meaning of pose estimation maps:
	 pose estimation maps provide richer cues for inferring body parts and their movements, which makes them useful for recognizing human actions from videos
How does this method compare to traditional video-based action recognition approaches?
	Traditional video-based approaches rely on analyzing the motion of pixels in a video to recognize actions, which can be noisy and less accurate.
the detail method to generate pose estimation maps 
	1. Predict pose estimation maps: Given each frame of a video, a convolutional pose machine is used to predict a pose estimation map for each body part. These maps represent the likelihood of each pixel in an image being part of a specific body joint. 
	2. Generate heatmaps: The pose estimation maps are then used to generate heatmaps, which are averaged over all body parts to produce a single heatmap for each frame. These heatmaps provide richer information to reflect human body shape. 
	3. Generate poses: Finally, the heatmaps are used to generate poses that denote the location of each body part in the image. These poses can be used to recognize human actions from videos.]