# Collagen-Quantification-in-Fish-Muscle-Images

In this project, I created an ImageJ Macro that takes a file of fish msucle images of samples that were stained with Pico-Sirius Red dye. Using past research papers, problem solving, and trial-and-error, I was able to automate the process of quantifying the collagen percent in each fish sample and generating a csv with my data.

## Code Overview

### Code Overview:
1.	Defined a folder with input fish .tif image files and output file destination for our csv with percent collagen. The code iterates through each fish image in the folder and runs the rest of the code.
2.	Part 1 of the code duplicates the fish image and uses one of these to run the Color Deconvolution2 plugin to get collagen pixel count.
3.	Part 2 uses the other duplicated image to generate pixel area of ROI (region of interest) using masking. This masing means all the pixels pertaining to the fish are black while the background is white. This is better than tracing around the fish because I can exclude cracks within the fish sample that are part of the background. To find the percent collagen, I divide the collagen pixel number by the ROI pixel number. 
4.	Data is appended to the csv
