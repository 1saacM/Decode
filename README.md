Decode
======

Photos  must be decoded to find the hidden message

This project explores multidimensional list is python via images. This is the final project and is worth a substantial percentage of your grade. No late projects will be accepted.

In this project you will need to analyze pixel data in images and find the hidden messages. You will be given three images that are encoded to look like nondescript noise. Follow the directions below to decode the images and find the hidden message.

Project DUE: 12/12 10PM


Links:
  GitHub Project - https://github.com/capu/spyi
  Notes on Git -  http://en.wikipedia.org/wiki/Git_(software)
  Git Tutorial - http://git-scm.com/docs/gittutorial
  PNG Specification (for extra credit) - http://www.w3.org/TR/PNG/
  TkInter Docs (for extra credit) - https://wiki.python.org/moin/TkInter

Image Functions:
You are provided with two image function utilities:

	def openImage(fileName):
		# This function will open an image file (only PNGs) and 
		# return a reference image (See below for details).

        	# fileName is the name of the image you want to open. 

	def createImage(refImage, fileName):
		# This function will take a reference image (refImage) and save it to a image file 
		# in the same directory named fileName



Reference Image:
A reference image is a simplified image format using the list data structure in python. Each reference image is a two dimensional list of pixels, stored as (r,g,b) tuples.
A 2 by 2 all black image would be defined as:
blackRefImage = [
	[ (0,0,0), (0,0,0) ],
	[ (0,0,0), (0,0,0) ],
]


Decode Single Channel Image:
The image named SingleChannel.png stores the secret message in the the red color channel. The value of 245 is stored in the red channel(the first value of the tuple) of each pixel that is part of the message. Change the image to filer for all of these important pixels and reveal the message.


Decode Gray Scale Image:
The image named GrayAverage.png stores the secret message in each color channel. GreyAverage.png is really meant to be a grayscale image(one where r=g=b). Calculate the grayscale value of each pixel by taking the average of all the colors r,b,g in the original image.
SO: grayValue = (r+b+g)/3


Decode the Upscaled image:
The image named UpScale.png is much more intricately encoded than the previous two types of images.  This image encodes the message by spreading the color information for the message across four pixels. See the diagram below.

 encoded:       decoded:

---------
| a | b |        -----
---------  --->  | r | 
| c | d |        -----
---------


r: resulting pixel
v: (not in the image above) v = r/2
a: pixel containing values for computation.
b: pixel containing the result of v mod a
c: pixel containing the result of v / a  (floor division)
d: 1 if r is odd 0 if r is even.  d = r % 2





EXTRA CREDIT:
EXTRA CREDIT:

Note: If you receive more than 90pts of extra credit in this project by 10PM 12/9 You may opt out of taking the final exam and receive an automatic 95 for the exam. Contact the professor with questions.

Merge Colors (10pts):
Write a function that will merge three reference images into a single image. Each reference image will represent a single color channel.

Custom Filter (10 pts each, MAX 30pts):
Look up a common filter and implement it.  Examples: Radial Blur, Sepia tone, Desaturate, High Pass Filter. Write a description about your algorithm.


GitHub Image Library(Max 50pts):
Make a substantial improvement to the image library on GitHub - https://github.com/capu/spyi
Examples: Major bug fix, Expand functionality, Add a new image format (jpeg, gif, etc)

Create and image Viewer(Max 90pts, Group):
In a group, create and integrate an image viewer to display your results and filters. This viewer needs to be worked on by at least three people and committed to the groups own GitHub Repository. Each teammate will be given points based on their contribution. TkInter is a good place to start if you want to pursue this.








