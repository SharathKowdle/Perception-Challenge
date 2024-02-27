# Perception-Challenge

The methodology involves converting the image to HSV color space, defining color bounds for the cones, and applying thresholding to isolate cone colors. Gaussian blur and morphological operations are then used to reduce noise. Contours are found and filtered based on area and aspect ratio to detect cone-like shapes. The centers of these shapes are calculated and split into two halves based on x-coordinate. The highest and lowest cones in each half are identified, and lines are drawn through them. The final image with lines is saved.

Libraries used:
OpenCV - for image processing tasks
NumPy - for numerical operations

I tried using Hough Line Transfrom to detect lines passing through the centers of the cones but I think I implemented it wrong because the HoughLinesP function expects an edge map as input, but the mask_filtered variable is not an edge map; it is a binary mask obtained from thresholding.




