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

![Screenshot (6)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(6).png)

## Shadow detection and removal

![Screenshot (10)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(10).png)

![Screenshot (11)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(11).png)

## Shadow edge removal by traversing method

![Screenshot (13)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(13).png)
# Tracking

![Screenshot (14)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(14).png)


https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/assets/143112500/b7b3c3f5-057f-4e71-85c0-e19687515da1



https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/assets/143112500/09e5530a-c849-4972-acad-6d09eb6ea69e



# Polynomial fitting

![Screenshot (15)](https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/blob/main/Images/Screenshot%20(15).png)

# Using UNET
For better results i have tried with UNET,it can be seen in following videos



https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/assets/143112500/986c592d-33a6-4109-8fe9-635af1defe28


https://github.com/yaswanth0209/Classification-of-vehicular-motion-trajectories-in-a-traffic-video/assets/143112500/3af30648-f73f-4417-b757-d72e2479e25d

