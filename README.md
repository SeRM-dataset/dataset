# SeRMdataset
![fig2](https://user-images.githubusercontent.com/64125124/79951808-5992e400-84b4-11ea-9ab3-7dd37d3266c0.png)

## About Image data

For the Road Marking (RM) map building, the RM should be extracted from a camera image at the pixel level using a semantic segmentation network. To train the semantic segmentation network for the lane-level RM map, a large number of images were gathered in South Korea. The RMs in the images were manually annotated at the pixel level. The SeRM dataset included 25,157 images annotated with 17 classes of RMs at the pixel level. The number of images constituting the dataset was 21,085 for training and 4072 for testing. In the SeRM dataset, “Road Mark” is defined as the union of symbolic road markings (SRMs), road lanes (RLs), and a background 

> ### SRM 
> slow down, go ahead, turn right, turn left, ahead or turn right, ahead or turn left, crosswalk, number markings, text markings, other markings
>
> ### RL 
> yellow double line, blue double line, broken line, white single line, yellow single line, stop line

### Example of RGB Image and pixel-level annotated Image : 

<img src="https://user-images.githubusercontent.com/64125124/79951811-5a2b7a80-84b4-11ea-9452-26cb8b49d164.png" width="30%">      <img src="https://user-images.githubusercontent.com/64125124/79951804-5861b700-84b4-11ea-8aa0-07a1b3e96927.png" width="30%">

### Colormap
<img src="https://user-images.githubusercontent.com/64125124/79954879-f35c9000-84b8-11ea-8955-f107807a8af2.png" width="80%"> 


## About Odometry data and Loop-closure

The images annotated with the experimental vehicle pose, where the images were acquired, were needed in building the RM map. To this end, 21,000 images were gathered on three routes in Seoul and Goyang-si and annotated with RTK-GPS and odometry data at the image level. Route 1 data were acquired from Sangam, Seoul. Route 1 is a complex route with many loop closures, including both narrow and wide roads. Route 2 data were obtained from Ilsan, Goyang-si, which consists of wide roads. Route 3 collected data from very large areas in Sangam and contained data obtained while driving the same road in opposite directions. The three routes included several loop closures, as shown in \figref{fig:ourtrajectory}. The total length of our three driving routes was approximately 26 km, with each route being 4.86, 9.47, and 11.63 km, respectively.

<img src="https://user-images.githubusercontent.com/64125124/79951851-6ca5b400-84b4-11ea-8c01-82e5a9c30e0c.png" width="33%"> <img src="https://user-images.githubusercontent.com/64125124/79951854-6e6f7780-84b4-11ea-8280-522cd1ca1dd7.png" width="33%"> <img src="https://user-images.githubusercontent.com/64125124/79951857-6f080e00-84b4-11ea-891b-0f4199295ecf.png" width="33%">

                 Route 1                              Route 2                                   Route 3

# Comparison of Driving Scene Datasets


# Comparison of Driving Scene Datasets

|    Type   | Name | Year | # of frames | LI^c^  | PLA^d^  | SRM | Cls# ^e^  | Od^f^  | GPS | LC^g^  | MT^h^
:----: | :----------: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----:
|   | Caltech Lanes | 2008 | 1,224  | o   | -    | -   | -       | -   | -   | -   | -   ||
|   | KITTI road | 2013 | 600  | -   | -    | -   | -   |  o   |  o   | -   | -   ||
| RL | TuSimple | 2017 | 6,408    |  o   | -    | -   | -   | -   | -   | -   | -  || 
|   | FiveAI \cite{34} | 2018 | 23,980 |  o   | -    | -   | -       | -   | -   | -   | -  || 
|   | CULane \cite{35} | 2018 | 133,235        |  o   | -    | -   | -       | -   | -   | -   | -  |
| SRM | Road Marking Detection | 2012 | 28,614 | -  | -  |o  | 10  | -  | -  | -   | -  |
|   | ROMA | 2008 | 116   |o   |o    |o   | 3  | -   | -   | -   | -   ||
|  | CamVid | 2008 | 701   | -   |  o    |  o   | 2    | -   | -   | -   | -   ||
|  | Cityscape | 2016 | 25,000  | -   | -    | -   | -       |o   | -   | -   |o   ||
| RL+SRM | Mapillary Vistas | 2017 | 20,000  | -   |o    |o   | 6       | -   | -   | -   |o   ||
|   |TRoM | 2017 | 712 |o   |o    |o   | 19      | -   | -   | -   |    || 
|   |ApolloScape | 2018 | 143K    |  -   |o    |o   | 27      | -   |o   | -   | -   ||
|   |BDD100k | 2018 | 120M^{1} |o   |o    | -   | 11      | -   |  o   | -   |o  || 
|   |**Ours**  | 2019 | 25,157 | -   |o    |o   | 16      |o  |o   |o   |  o  |

^a^Road Lane; ^b^ Symbolic Road Markings; ^c^ Lane Instances; ^d^ Pixel Level Annotation; ^e^ Number of Classes; ^f^ odometry of vehicle; ^g^ Loop Closure; ^h^ Multi-Trajectory; 
^1^ only 5683 images are pixel-level annotated




* * *
# Supplementary Video

[![Watch the video](https://img.youtube.com/vi/1x0EDhLCMTs/maxresdefault.jpg)](https://youtu.be/1x0EDhLCMTs )
Youtube : https://youtu.be/1x0EDhLCMTs

* * *
# Download

The full dataset will be uploaded very soon. 

