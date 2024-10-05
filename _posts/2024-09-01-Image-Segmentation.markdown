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
header-img: "img/Science_Background10.jpg"
title: Image Segmentation Using MATLAB
author: Vignesh
tags: ImagePreparation ComputerVision Segmentation cilia Pattern
subtitle: Cell Segmentation
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

![Frame](/img/Cell Segmentation/Despeckle.jpg)
<p align="center">An example de-speckling of a noisy image using MATLAB filters is shown above </p>

## Cell Segmentation Using MATLAB
Image processing toolbox in MATLAB can be used for segmenting cells manually using an ROI (region of interest) tool or using in-built functions such as watershed or edge detection functions such as canny, sobel, etc. The custom written <a href=" https://github.com/vignesharavind/Cell-Segmentation/blob/main/Auto%20Cell%20Segmentation/Sobel_All_Cells_TWO.m">MATLAB script</a> can be used to automatically identify and create masks or skeleton of the cells. The quality of the image and the threshold chosen for watershed in the script might affect the accuracy of the traced cells. Segmentation of cells specifically near the edges might be erroneous.   

![Frame](/img/Cell Segmentation/Slide1.jpg)
<p align="center">Automated cell segmentation using MATLAB</p>

## Multiciliated Cell Segmentation (Manual)
In case of small image sets or tracing specific cells that require high accuracy  or if segmentation is difficult to automate because of heterogeneity in the image, polygon tool in MATLAB can be used to trace cells manually. Running the <a href="https://github.com/vignesharavind/Cell-Segmentation/blob/main/Manual%20Cell%20Segmentation/Final_Manual_Segmentation.m">MATLAB script</a> will ask the user to input images (For multiciliated cell choose actin and cilia images). The images are overlayed and then the user can start tracing the cells. The coordinates of the traced cells will be stored and loop can be exited by clicking the ‘Quit’ button in the dialogue box. If the tracing needs to be done in several parts, ‘save work in progress’ and ‘continue working’ section can be run to save and resume working on manual segmentation later.         
 
![Frame](/img/Cell Segmentation/Manual_Segmentation.jpg)
<p align="center">An example showing manual segmentation of multiciliated cells on the skin of Xenopus tropicalis embryo using ‘drawpolygon’ ROI tool in MATLAB</p>

![Frame](/img/Cell Segmentation/Slide3.jpg)
<p align="center">Automated segmentation of non-multiciliated cells (center) and manual segmentation of multiciliated cells (right)</p>

## Cell Property Visualization & Analysis
After running the first three blocks of the <a href="https://github.com/vignesharavind/Cell-Segmentation/blob/main/Manual%20Cell%20Segmentation/Final_Manual_Segmentation.m">MATLAB script</a>, ‘Get region properties’ can be run to create cell property plots utilizing the ‘regionprops’ function. Pixel to micron factor (pf) value needs to be set to get the cell properties in the units of microns along with surface color gradient plots normalized to the physical values.    

![Frame](/img/Cell Segmentation/Slide4.jpg)
<p align="center">Example cell properties (cell area, cell aspect ratio, and cell circularity) are shown for non-multiciliated cells (top row) and multiciliated cell (bottom row) based on the previous image</p>

![Frame](/img/Cell Segmentation/Slide55.jpg)
<p align="center">Another example multiciliated cell properties (cell area, cell aspect ratio, and cell circularity) extracted from animal cap explants (Xenopus tropicalis explants) are shown.</p>

## Basal Body Segmentation
In multiciliated cells (MCCs), during ciliogenesis hundreds of centriole derived basal bodies dock to the cell membrane giving rise to hair-like projections or cilia. Centrin or chibby are usually used as protein markers to visualize the base portion of cilia. This custom written <a href="https://github.com/vignesharavind/Cell-Segmentation/blob/main/Centrin%20Segmentation/Master_Centrin.m">MATLAB script</a> can automatically segment fluorescent centrin/chibby images after trying out different threshold values. The script also returns total number of basal bodies within a cell based on region of interest (ROI) mask drawn around the cell. Alternatively, this <a href="https://github.com/vignesharavind/Cell-Segmentation/blob/main/Centrin%20Segmentation/Segment_Basal_Body.m">MATLAB script</a> can also be used for segmenting noisier centrin/chibby signals.

![Frame](/img/Cell Segmentation/Slide7.jpg)
<p align="center">An example basal body segmentation is shown using centrin marker.</p>

## Cilia orientation
In multiciliated cells (MCCs), cilia orientation can be found by tracing clamp (cylindrical) to centrin (spherical) signals. Running this <a href="https://github.com/vignesharavind/Cell-Segmentation/blob/main/Cilia%20Orientation/Master_Clamp_Centrin_Tracer.m">MATLAB script</a> allows the user to trace each cilia direction for a cell followed by tracing the cell boundary of corresponding to the cilia orientations. It allows users to trace cilia orientations in multiple cells. The results are saved in an excel file and stored in the local path of the code. The angles are measured from -180o to +180o (counter-clockwise). For only tracing cilia orientations but not cell boundaries pertaining to those cilia use this<a href="https://github.com/vignesharavind/Cell-Segmentation/blob/main/Cilia%20Orientation/Only_Clamp_Tracing.m">MATLAB script</a>         

![Frame](/img/Cell Segmentation/Slide8.jpg)
<p align="center">Cilia orientations traced for a multiciliated cell along with corresponding polar histograms are shown in the figure above.</p>
