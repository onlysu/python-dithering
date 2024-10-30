
找到得一个可以用于电子纸，墨水屏的抖动dithering算法 python程序：
可以修改里面的COLORS，为BW，BWR，BWRY，或者7C，等其它彩色，采用基础的FS 抖动算法；

其中里面的效果，可以修改错误比，默认为16，亲测修改为20比较适合于墨水屏。

# Image Dithering the Redundant Way

A basic python function to dither a target image. Uses the [Floyd-Steinberg dithering](https://en.wikipedia.org/wiki/Floyd%E2%80%93Steinberg_dithering) algorithm,
implemented using the Python Imaging Library (PIL) fork, [Pillow](https://github.com/python-pillow/Pillow) (even though it has an inbuilt dithering function).

### Usage

Call function from the python environment:
```
>>> ditherImage(target, saveOutput=True, outputType=type, showFinal=True)
```

Saved output images will have '(dithered)' appended to the file name.

##### Parameters

- `target`: file path to target image
- `saveOutput`: whether or not output image should be saved
- `outputType`: the output file format. Some [supported types](https://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html) may negate dithering effect.
- `showFinal`: whether or not the output image should be displayed using the default image viewer

### Note

This project was undertaken as a way to develop skills using a new language, and is still under development.
The intended stages of the project thus far are:

- [X] Use image processing functions external libraries
- [X] Create and manipulate tuples and 2-dimensional lists
- [X] Implement dithering algorithm using nested loops
- [X] Internal documentation
- [ ] Improve color matching performance; currently done in O(C) time per pixel
- [ ] Extend to dithering video files
- [ ] Accelerate video processing with multi-threading

##### Pull Requests

As this is intended to be an educational endeavour, pull requests for _*existing features*_
are welcomed. Extending existing functionality will be done by me, though I am
open to any and all fun/challenging suggestions.
