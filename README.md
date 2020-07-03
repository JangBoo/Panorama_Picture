# Panorama_Picture

## Ransac function
first find 4 random from match, from that match, calculate H with cv2.findhomography. with that H use function computeinliercount and than add it the array.
after the many iteration, sort it to find the best H which has the highest number of inliers.
wth this H, find inlier again.-> find new H again.


## Computerinliner
it calculate the number of inlying points. project the point with project function. 
if the projected point's distance is less than the threshold it is inlier, and counted it and return the point, ( i didn't return the total number becuase, i can just use len(array) at the end)

## Stitch
it calculate max size to make the screen large enough, by projecting the 4 corners
copy image1 to the screen and use getRectSubPix to input the next image.


![GitHub Logo](https://github.com/JangBoo/Panorama_Picture/blob/master/lb.png)
![GitHub Logo](https://github.com/JangBoo/Panorama_Picture/blob/master/3.jpg)
![GitHub Logo](https://github.com/JangBoo/Panorama_Picture/blob/master/4.jpg)




reference
https://www.pyimagesearch.com/2016/01/11/opencv-panorama-stitching/
https://towardsdatascience.com/image-panorama-stitching-with-opencv-2402bde6b46c
