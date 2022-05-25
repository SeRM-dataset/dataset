# SeRM dataset : A Lane-Level Road Marking Map Using a Monocular Camera
<div align=center>
 
<img src="https://user-images.githubusercontent.com/64125124/79951808-5992e400-84b4-11ea-9ab3-7dd37d3266c0.png" width="80%">
 
</div>

## About Image data

For the Road Marking (RM) map building, the RM should be extracted from a camera image at the pixel level using a semantic segmentation network. To train the semantic segmentation network for the lane-level RM map, a large number of images were gathered in South Korea. The RMs in the images were manually annotated at the pixel level. The SeRM dataset included 25,158 images annotated with 16 classes of RMs at the pixel level. The number of images constituting the dataset was 19,998 for training and 5,160 for testing. In the SeRM dataset, “Road Mark” is defined as the union of symbolic road markings (SRMs), road lanes (RLs), and a background 

> ### SRM 
> slow down, go ahead, turn right, turn left, ahead or turn right, ahead or turn left, crosswalk, number markings, text markings, other markings
>
> ### RL 
> yellow double line, blue double line, broken line, white single line, yellow single line, stop line

### Example of RGB Image and pixel-level annotated Image : 
<div align=center>

<img src="https://user-images.githubusercontent.com/64125124/79951811-5a2b7a80-84b4-11ea-9452-26cb8b49d164.png" width="30%">      <img src="https://user-images.githubusercontent.com/64125124/79951804-5861b700-84b4-11ea-8aa0-07a1b3e96927.png" width="30%">

### Colormap
<img src="https://user-images.githubusercontent.com/64125124/79954879-f35c9000-84b8-11ea-8955-f107807a8af2.png" width="80%"> 

</div>

## About Odometry data and Loop-closure

The images annotated with the experimental vehicle pose, where the images were acquired, were needed in building the RM map. To this end, 21,000 images were gathered on three routes in Seoul and Goyang-si and annotated with RTK-GPS and odometry data at the image level. Route 1 data were acquired from Sangam, Seoul. Route 1 is a complex route with many loop closures, including both narrow and wide roads. Route 2 data were obtained from Ilsan, Goyang-si, which consists of wide roads. Route 3 collected data from very large areas in Sangam and contained data obtained while driving the same road in opposite directions. The three routes included several loop closures, as shown below. The total length of our three driving routes was approximately 26 km, with each route being 4.86, 9.47, and 11.63 km, respectively.

> ### Route 1 (Sangam, Seoul / 4.86km )
> <div align=center>
> <img src="https://user-images.githubusercontent.com/64125124/79951851-6ca5b400-84b4-11ea-8c01-82e5a9c30e0c.png" width="60%">
> </div>
> 
> ### Route 2 (Ilsan, Goyang-si / 9.47km)
> <div align=center>
> <img src="https://user-images.githubusercontent.com/64125124/79951854-6e6f7780-84b4-11ea-8280-522cd1ca1dd7.png" width="60%"> 
> </div>
> 
> ### Route 3 (Sangam, Seoul / 11.63km)
> <div align=center>
> <img src="https://user-images.githubusercontent.com/64125124/79951857-6f080e00-84b4-11ea-891b-0f4199295ecf.png" width="60%">
> </div>


## Comparison of Driving Scene Datasets

|    Type   | Name | Year | # of frames | LI<sup>c</sup>  | PLA<sup>d</sup>  | SRM | Cls#<sup>e</sup>  | Od<sup>f</sup>  | GPS | LC<sup>g</sup>  | MT<sup>h</sup>
:----: | :----------: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----:
| RL<sup>a</sup> | Caltech Lanes | 2008 | 1,224  | o   | -    | -   | -       | -   | -   | -   | -   ||
| RL | KITTI road | 2013 | 600  | -   | -    | -   | -   |  o   |  o   | -   | -   ||
| RL | TuSimple | 2017 | 6,408    |  o   | -    | -   | -   | -   | -   | -   | -  || 
| RL | FiveAI | 2018 | 23,980 |  o   | -    | -   | -       | -   | -   | -   | -  || 
| RL | CULane | 2018 | 133,235        |  o   | -    | -   | -       | -   | -   | -   | -  |
| SRM<sup>b</sup> | Road Marking Detection | 2012 | 28,614 | -  | -  |o  | 10  | -  | -  | -   | -  |
| RL+SRM | ROMA | 2008 | 116   |o   |o    |o   | 3  | -   | -   | -   | -   ||
| RL+SRM | CamVid | 2008 | 701   | -   |  o    |  o   | 2    | -   | -   | -   | -   ||
| RL+SRM | Cityscape | 2016 | 25,000  | -   | -    | -   | -       |o   | -   | -   |o   ||
| RL+SRM | Mapillary Vistas | 2017 | 20,000  | -   |o    |o   | 6       | -   | -   | -   |o   ||
| RL+SRM |TRoM | 2017 | 712 |o   |o    |o   | 19      | -   | -   | -   |    || 
| RL+SRM |ApolloScape | 2018 | 143K    |  -   |o    |o   | 27      | -   |o   | -   | -   ||
| RL+SRM |BDD100k | 2018 | 120M<sup>1</sup> |o   |o    | -   | 11      | -   |  o   | -   |o  || 
| RL+SRM |**Ours**  | 2020 | 25,157 | -   |o    |o   | 16      |o  |o   |o   |  o  |

<sup>a</sup>Road Lane; <sup>b</sup> Symbolic Road Markings; <sup>c</sup> Lane Instances; <sup>d</sup> Pixel Level Annotation; <sup>e</sup> Number of Classes; <sup>f</sup> odometry of vehicle; <sup>g</sup> Loop Closure; 
<sup>h</sup> Multi-Trajectory; 

<sup>1</sup> only 5683 images are pixel-level annotated


* * *
# Supplementary Video

[![Watch the video](https://img.youtube.com/vi/h4pIEwkPDd0/maxresdefault.jpg)](https://youtu.be/h4pIEwkPDd0)
Youtube :   https://youtu.be/h4pIEwkPDd0

* * *

# Download

Please email [Wonje Jang](mailto:jangwj1256@yonsei.ac.kr)(jangwj1256@yonsei.ac.kr) to obtain the google drive link for downloading.

> Email Format 
> 
> *Name :
>
> *Organization : 
>
> *Purpose of dataset :
>


* * *
# Citation
Please cite [SeRM dataset](https://ieeexplore.ieee.org/document/9583170) in your publications if it helps your research:

    @article{jang2021JAS,
      author={Wonje Jang, Junhyuk Hyun, Jhonghyun An, Minho Cho and Euntai Kim},
      title={A Lane-level Road Marking Map using a Monocular Camera},
      journal={IEEE/CAA Journal of Automatica Sinica},
      volume={Volume: 9, Issue: 1},
      year={2022}
    }
      
    @inproceedings{jang2018iv,
      author = {Wonje Jang, Jhonghyun An, Sangyun Lee, Minho Cho, Myungki Sun and Euntai Kim},
      title = {Road Lane Semantic Segmentation for High Definition Map},
      booktitle = {Proc. of the 2018 IEEE Intelligent Vehicles Symposium (IV)},
      year = {2018}
    }
