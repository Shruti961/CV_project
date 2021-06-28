# CV_project
Brand Logo Detection using Template Matching

What is Template Matching?
Template Matching is a method for searching and finding the location of a template image in a larger image.


OBJECTIVE
Detection and identification of logos present in images using predefined templates .

IMPLEMENTATION DESCRIPTION 

LOADED THE SOURCE IMAGE AND TEMPLATE

PRE PROCESSING THE IMAGE :
We resize the template, then applied the Canny edge detector(which includes gaussian blurring )on the template as well as the image to detect edges because template matching works better after edge detection .
We subtracted the mean of the image to normalise the image and take care of different levels of illumination and brightness .
We used feature pyramid to create the pyramids of image at different scales(The image is resized to various scales and the sliding window is run on these resized images.)

TEMPLATE MATCHING:
We used the inbuilt cv.match_Template() for this purpose. It slides the template image over the input image (analogy from convolution) and compares the template and patch of input image under the template image.The function returns a grayscale image, where each pixel denotes how much neighbourhood of that pixel matches with the sliding template.

IMPLEMENTATION OF THE MAIN FUNCTION:
Here , we make use of all the previously defined functions and implement them on the test image . The max_score represents the better matches of the test image with the template. Then it gives the output of the image along with the brand name with which it matches the best.  


