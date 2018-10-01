# Saliency-Detection-in-360-Videos

### Introduction
This repo contains the code that used in paper **Saliency Detection in 360° Videos** by Ziheng Zhang, Yanyu Xu, Jingyi Yu and Shenghua Gao.

### Requirements
  - 0.3.0 <= Pytorch <= 0.3.1 
  - numpy >= 1.13
  
### File structure
```
- test.py
  purpose: Provide test model that uses spherical convolution.
- sconv
  - functional
    - common.py
      Purpose: Contains some helper functions used in sphercal convolution.
    - sconv.py
      Purpose: Provide the spherical convolution function for Pytorch.
    - spad.py
      Purpose: Provide the spherical pooling function for Pytorch.
  - module
    - sconv.py
      Purpose: Provide the spherical convolution module for Pytorch.
    - smse.py
      Purpose: Provide the spherical mean-square loss module for Pytorch.
    - spad.py
      Purpose: Provide the spherical padding module for Pytorch.
    - spool.py
      Purpose: Provide the spherical pooling module for Pytorch.
```

### Usage
  We currently provide a sample model in `test.py`. The model and checkpoint that used in original paper will be released later.
  
### Known issues
  - The process of determining the kernel area for different θ location is unstable, which will produce some `nan` values in output feature maps. However, this bug seems to have minor effects during training and testing.
  
### TODO
  - [x] Release core functions and modules
  - [ ] Release training and testing code for saliency detection
  - [ ] Resolve the math unstability when calculating the kernel area in different θ location
  - [ ] Rewrite spherical convolution for torch 0.4+
