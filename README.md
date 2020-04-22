# SeRMdataset
![fig2](https://user-images.githubusercontent.com/64125124/79951808-5992e400-84b4-11ea-9ab3-7dd37d3266c0.png)

## About Image data

For the RM map building, the RM should be extracted from a camera image at the pixel level using a semantic segmentation network. To train the semantic segmentation network for the HD RM map, a large number of images were gathered in South Korea. The RMs in the images were manually annotated at the pixel level. The SeRM dataset included 25,157 images annotated with 17 classes of RMs at the pixel level. The number of images constituting the dataset was 21,085 for training and 4072 for testing. In the SeRM dataset, “Road Mark” is defined as the union of symbolic road markings (SRMs), road lanes (RLs), and a background 

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

The images annotated with the experimental vehicle pose, where the images were acquired, were needed in building the HD RM map. To this end, 21,000 images were gathered on three routes in Seoul and Goyang-si and annotated with RTK-GPS and odometry data at the image level. Route 1 data were acquired from Sangam, Seoul. Route 1 is a complex route with many loop closures, including both narrow and wide roads. Route 2 data were obtained from Ilsan, Goyang-si, which consists of wide roads. Route 3 collected data from very large areas in Sangam and contained data obtained while driving the same road in opposite directions. The three routes included several loop closures, as shown in \figref{fig:ourtrajectory}. The total length of our three driving routes was approximately 26 km, with each route being 4.86, 9.47, and 11.63 km, respectively.

<img src="https://user-images.githubusercontent.com/64125124/79951851-6ca5b400-84b4-11ea-8c01-82e5a9c30e0c.png" width="33%"> <img src="https://user-images.githubusercontent.com/64125124/79951854-6e6f7780-84b4-11ea-8280-522cd1ca1dd7.png" width="33%"> <img src="https://user-images.githubusercontent.com/64125124/79951857-6f080e00-84b4-11ea-891b-0f4199295ecf.png" width="33%">

    Route 1    Route 2     Route 3

[More Details about SeRM dataset ](http://cilab.yonsei.ac.kr/datasetSeRM)


* * *
# Supplementary Video

will be uploaded soon...!

* * *
# Download
You can download the SpeRM dataset through contacting
email : <jangwj1256@yonsei.ac.kr>

