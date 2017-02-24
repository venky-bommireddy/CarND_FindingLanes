#**Finding Lane Lines on the Road** 

##Writeup Template

###You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

###1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied gaussian blur to reduce noise in the image.

After that to find edges I canny edge detection algorithm to get edges.

Then passed these edges to the region of interest function to get lines from image(avoids unnecessary edges in the image).

Passed above output to houghline transform algorithm to get line image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by finding center and slopes for left line and rightline in the image.

So now we are going to have left slope, left center , right slope & right center.

I will get these values by averaging lines that we get it from Houghline transform algorithm.
And specified line height half of the image height.

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


###2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


###3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
