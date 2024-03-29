# Dataset construction

The SeRM dataset consists of a total of 3 parts.

1. RGB images and semantic labeled images for training (0. SeRM_image)
2. RGB images for validatation (1. SeRM_image_test)
3. Localization and Mapping dataset (2. SeRM_mapping)


The structure of each part is as shown in the figure below.

<div align="center">
<img src="https://user-images.githubusercontent.com/64125124/158113896-efa1cfda-78ca-4068-90e1-aadd06446079.png" width="60%">

</div> 

'0. SeRM_image' provides RGB image of 320 x 1280 size and semantic segmentation label, and '1. SeRM_image_test' provides RGB images only. Finally, '2. SeRM_mapping' provides odometry information of the vehicle and the ground truth obtained by GPS for localization & mapping. In addition, RGB images acquired with the camera mounted on the vehicle are provided in 672 x 1280 size. To apply the trained network from 1.SeRM_image, one can use the lower part (320 x 1280) of the 0.original_full image given in 3.SeRM_mapping for inference.
  
  
  
# Colormap 

> ### Class information 
![Class information](https://user-images.githubusercontent.com/64125124/209811522-47b4285d-fcef-439e-bc14-d63a8941e997.png)


> ### trainannot label information 
|    Name   | Train ID  |  category  |  color   
:----------: | :-----: | :-----: | :-----:
|    Background   | 0  |  ignore  |  [0 0 0];
|    Slow down   | 1  |  SRM  |  [0 0 255];  
|    Go ahead   | 2  |  SRM  |  [0 128 255];  
|    Trun right   | 3  |  SRM  |  [255 128 0]; 
|    Turn left   | 4  |  SRM  |  [255 192 64]; 
|    Ahead or turn right   | 5  |  SRM  |  [64 0 255]; 
|    Ahead or turn left   | 6  |  SRM  |  [128 0 255];   
|    Crosswalk   | 7  |  SRM  |  [255 0 255	]; 
|    Double line (yellow)   | 8  |  RL  |  [0 255 0];  
|    Double line (blue)   | 9  |  RL  |  [192 255 128]; 
|    Broken line (white)   | 10  |  RL  |  [210 210 210];
|    Single line (yellow)   | 11  |  RL  |  [255 255 0]; 
|    Single line (white)   | 12  |  RL  |  [128 128 128]; 
|    Stop line   | 13  |  RL  |  [255 0 0]; 
|    Numbers   | 14  |  SRM  |  [64 192 64];
|    Texts   | 15  |  SRM  |  [128 192 128]; 
|    Others   | 16  |  SRM  |  [128 64 80]; 


# Dataset Details

The odometry data (Log_odom.txt) and ground truth (Log_groundtruth.txt) provided by ‘2.SeRM_mapping’ follow the be configuration, respectively.

> ### Log odom.txt
> image index,    x coordinate,    y coordinate,    heading angle (radian)
> ### Log groundtruth.txt
> image index,    x coordinate,    y coordinate,    heading angle (radian)

Image index shows an index of RGB image in '0.original_full' that matches each x, y, heading angle.
The (x, y) coordinate values and heading angle follow the coordinate system below.

<div align="center">
<img src="https://user-images.githubusercontent.com/64125124/158099443-50411717-edcb-4f94-bdea-00e6965412cd.png" width="60%">
</div> 

  
# Dataset Validation 

Please email [Wonje Jang](mailto:jangwj1256@yonsei.ac.kr) your semantic segmentation result of (1. SeRM_image_test) to obtain validation result. 
The validation results provided are 'recall', 'precision', 'F1-score', 'mIoU', 'mIoU of each class' value as in our [paper](https://ieeexplore.ieee.org/document/9583170).


  
