#BoxFilter
###Jordan Hughes :see_no_evil:
###UC Santa Barbara
####hughesj919 at gmail.com

This is a Python 2 based grayscale image box filter.  It uses the open cv module just to read our image in and create a matrix.
From there it calculates an integral image, i.e. a summed area table, then uses that to find an average of the surrounding filter size
squared pixels and replaces the current value with the new value.

Usage example is as follows:

```python BoxFilter.py -—filter_size 5 mary_small.png```

The script will run and print some preview values for the integral image and final image.  
For more help with the code run ```pydoc BoxFilter``` at a terminal.

File output will be:

* integral_image.png — the integral image.
* finalimage.png — the final blurred result.

Box blurs are often used to approximate Gaussian blurs quickly. This script will blur images using a box based on the filter size parameter. 
As filter size increases, the level of blurring increases because all pixels inside the boxes bounds are averaged. 
The integral image is calculated first, allowing the sum of the pixel values in any rectangular area of the image can
be computed in constant time. This is significantly faster than other techniques. For more information refer to the following links:

* [Box Blur](https://en.wikipedia.org/wiki/Box_blur)
* [Summed Area Table AKA Integral Image](https://en.wikipedia.org/wiki/Summed_area_table)
* [Approximating Image Filters With Box Filters](http://www.contrib.andrew.cmu.edu/~bpires/pdfs/box_filters.pdf)

#####This is the original image: 

![Mary Original](/images/mary_small.png)

#####Box filter using size 5:

![Mary 5](/images/mary_small_5.png)

#####Box filter using size 9:

![Mary 9](/images/mary_small_9.png)

#####Box filter using size 13:

![Mary 13](/images/mary_small_13.png)