# Error Level Analysis using C++ and OpenCV #


1. implement ELA algorithm on a jpeg image using C/C++.
2. for above C/C++ code, Implement a python wrapper using cython.
3. compare the results of ELA for an image captured from your mobile phone versus the same image after photoshop (or any kind of image editing). This part of scripting should be done in python using cython wrapper that you wrote earlier.


## About the Project ##

### The Algorithm ###
Error Level Analysis (ELA) permits identifying areas within an image that are at different compression levels. With JPEG images, 
the entire picture should be at roughly the same level. If a section of the image is at a significantly different error level, 
then it likely indicates a digital modification. ELA highlights differences in the JPEG compression rate. Regions with uniform 
coloring, like a solid blue sky or a white wall, will likely have a lower ELA result (darker color) than high-contrast edges.


### Description of the folders and files in the repository ###
1. **Initial_Test**: Contains the images on which I tested the implementation of the algorithm in C++ sans the python wrapper
2. **Photoshop_Test**: Contains the images on which I tested the implementation of the wrapper and in a sense the working of thw whole 
project.
3. **Wrapper_Files**:
  * ela.hpp: Contains the function definitions that were used in the file ela_cython.cpp.
  * setup.py: Builds the wrapper.cpp file which makes the function callable from a python scripts.
  * wrapper.pyx: Cython file which acts as the interface between the C++ code and the python interpreter.
4. **ela.cpp**: The first implementation of the algorithm in C++. Works fine on it's own 
5. **ela_cython.cpp**: The actual code for the algorithm modified to make it compatible with the cython compiler.
6. **run.py** : The file to run on your python interpreter.
