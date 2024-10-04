---
slideinit: >-
  <section markdown="1"
  data-background="http://projectpages.github.io/project-pages/img/slidebackground.png"><section
  markdown="1">
vertical: </section><section markdown="1">
horizontal: >-
  </section></section><section markdown="1"
  data-background="http://projectpages.github.io/project-pages/img/slidebackground.png"><section
  markdown="1">
layout: post
header-img: "img/Science_Background11_3.jpg"
title: Image Segmentation Using MATLAB
author: Vignesh
tags: ImagePreparation ComputerVision Segmentation cilia Pattern
subtitle: Endothelium force maps
category: project
published: true
visualworkflow: true
---
<!-- Start Writing Below in Markdown -->
<section markdown="1" data-background="http://projectpages.github.io/project-pages/img/slidebackground.png"><section markdown="1">
## {{ page.title }}
<hr>
#### {{ page.author }}
## Image Preparation using MATLAB
Image contrast can be adjusted using several functions such as histeq, imadjust, and adapthisteq available in the image processing toolbox. Sample contrast enhancement code can be found in this <a href=" https://github.com/vignesharavind/Cell-Segmentation/blob/main/Image%20Preparation/Enhance_Contrast.m">github repository</a>.  
 
![Frame](/img/Cell Segmentation/Contrast.jpg)
<p align="center">An example image is shown above (left most) after adjusting the contrast with different functions</p>

Background noise in the image can be subtracted by selecting a rectangular region of interest (ROI) and subtracting the average grayscale value over the 8 bit or 16 bit images. An example MATLAB code to do background subtraction can be found in this <a href=" https://github.com/vignesharavind/Cell-Segmentation/blob/main/Image%20Preparation/Background_Subtraction.m">github repository</a>.  

![Frame](/img/Cell Segmentation/Subtracted.jpg)
<p align="center">An example background subtraction is shown for a saturated image</p>

White noise or speckles in the background can be removed using wiener or median filters in MATLAB among other functions which are also available in the image processing toolbox. An example code can be found <a href=" https://github.com/vignesharavind/Cell-Segmentation/blob/main/Image%20Preparation/Despeckle_Filters.m">here</a>.  

![Frame](/img/Cell Segmentation/Subtracted.jpg)
<p align="center">An example de-speckling of a noisy image using MATLAB filters is shown above </p>


## Cell Segmentation Using MATLAB
Image processing toolbox in MATLAB can be used for segmenting cells manually using an ROI (region of interest) tool or using in-built functions such as watershed or edge detection functions such as canny, sobel, etc. The custom written <a href=" https://github.com/vignesharavind/Cell-Segmentation/blob/main/Auto%20Cell%20Segmentation/Sobel_All_Cells_TWO.m">MATLAB script</a> can be used to automatically identify and create masks or skeleton of the cells. The quality of the image and the threshold chosen for watershed in the script might affect the accuracy the traced cells. Segmentation of cells specifically near the edges might be erroneous.   

![Frame](/img/Cell Segmentation/Slide1.TIF)
<p align="center">Automated cell segmentation using MATLAB</p>
