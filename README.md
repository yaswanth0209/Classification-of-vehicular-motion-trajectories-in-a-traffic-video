# Classification-of-vehicular-motion-trajectories-in-a-traffic-video
Vehicle trajectory classification is an essential task in various applications, including traffic management, autonomous driving, and transportation analysis. It involves categorizing the movement patterns and paths followed by vehicles on road networks. There are several ways to classify vehicle trajectories, depending on the criteria and objectives of the classification. 
![Screenshot (4)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(4).png)
As first phase of this project tracking has been done.
# Segmentation
 Segmentation involves dividing an image into multiple regions or segments, where each segment represents a distinct object(here it is an individual vehicle) or region of interest. In this project segmentation has been done in three phases
1. Background detection
2. Vehicle Detection
3. Shadow detection and shadow removal
## Background detection
Background detection is used to identify and separate the background in an image or video from the foreground objects or subjects.Here for background detection "Histogram based" approach is used,in this method histogram of each pixel with respect to their respective locations through out video is calculated.With the help of these histograms background image has been detected,below the flow diagram for this approach,input video and extracted background image are presented
![Screenshot (5)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(5).png)


https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/assets/143112500/aa5e8951-8c78-4e61-87ca-b64ae256293b

#Detected background image form above video



![background_rgb](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/background_rgb.jpg)

## Vehicle detection
Using substraction method vehicles or objects have been detected,for this substract each frame of the video with the detected background image,below we can see the detected vehicles. In this detected vehicles Shadow has been detected as the vehicles body wich creates a false values during tracking.

![Screenshot (6)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(6).png)

## Shadow detection and removal
To detect the shadow from the segmented vehicles "Optical Gain matrix" has been calculated which is the fraction of current frame's gray image to the detected background image's gray image.From this optical gain matrix and by the segmented vehicles shadow part of each vehicle has been detected

![Screenshot (10)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(10).png)

Once the shadow part has been detected remove it from respective segmented vehicles.We ended with an image of segmented vehicles along with shadow edge wich create same false values as previous during tracking.

![Screenshot (11)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(11).png)

## Shadow edge removal by traversing method
To remove this shadow edge for each vehicle traverse from right to left or left to right inside respective bounding box if there is a change in pixel values from 1--> 0 -->1 treat initiall one's as shadow eddge part and assigned with zeros similarly while traversing from right to left if there is a change in pixel values from 1--> 0 -->1 the lateral one's treat as shadow edge and assigned with zeros.Similarly traversed from top to bottom and from bottom to top. In below figure we can observe that shadow part has been removed completely. 

![Screenshot (13)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(13).png)
# Tracking

![Screenshot (16)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/assets/143112500/87336a49-106b-49a9-a97d-5696b91f3d3f)

With the help of above flowchart track each segmented vehicle after shadow removal and labell each vehicle with unique number the results are shown in below video's,this videos shown are for upto first 500 frames of the original video


https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/assets/143112500/b7b3c3f5-057f-4e71-85c0-e19687515da1

The above video show's the tracking of each vehicle with different numbering.


https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/assets/143112500/09e5530a-c849-4972-acad-6d09eb6ea69e
In this above video each vehicles centroid has been marked with different colour and has been tracked for all existing frames.


# Polynomial fitting

![Screenshot (15)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(15).png)

# Using UNET
For better results i have tried with UNET,it can be seen in following videos



https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/assets/143112500/986c592d-33a6-4109-8fe9-635af1defe28


https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/assets/143112500/3af30648-f73f-4417-b757-d72e2479e25d

