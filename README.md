# DeepFE: Deep Learning for Frog Eggs Quantification

The Aquatic Department at LSU (AGGRC), works to address the lack of standardization and reproducibility in cryopreservation for aquatic species. Hence, the statistics of the eggs to be preserved is important for record. Our mission was to develop software capable of accurately counting frog eggs in images using deep learning with varying image sizes.

<img src = "https://github.com/ishulsu/Deep-Learning-for-Frog-Eggs-Quantification/blob/main/images/236.jpg" width = "50%" height="45%" hspace="30" /> <img src = "https://github.com/ishulsu/Deep-Learning-for-Frog-Eggs-Quantification/blob/main/images/IMG_7008.jpeg" width = "28%" height = "50%" /> 

To address this, we used the architecture ``StarDist" , which has  U-Net neural network as its backbone, followed by the  Non-Maximum Suppression algorithm.  The following are references for our work.
- Uwe Schmidt, Martin Weigert, Coleman Broaddus, and Gene Myers.  
[*Cell Detection with Star-convex Polygons*](https://arxiv.org/abs/1806.03535).  
International Conference on Medical Image Computing and Computer-Assisted Intervention (MICCAI), Granada, Spain, September 2018.

- Martin Weigert, Uwe Schmidt, Robert Haase, Ko Sugawara, and Gene Myers.  
[*Star-convex Polyhedra for 3D Object Detection and Segmentation in Microscopy*](http://openaccess.thecvf.com/content_WACV_2020/papers/Weigert_Star-convex_Polyhedra_for_3D_Object_Detection_and_Segmentation_in_Microscopy_WACV_2020_paper.pdf).  
The IEEE Winter Conference on Applications of Computer Vision (WACV), Snowmass Village, Colorado, March 2020

### Training and Testing
Training on 144 images and testing on 36 images yielded us an accuracy upto 98 % accuracy.  

The image on the left is a test image with the total count of 2006 eggs and the image on the right is the prediction with predicted count of 1992 eggs, which accounts for 99.3\% of the actual count.

<img alt="Input Image" src = "https://github.com/ishulsu/Deep-Learning-for-Frog-Eggs-Quantification/blob/main/images/2006count.png" title="Input Image"  height = "50%" width = "49%" />  <img src = "https://github.com/ishulsu/Deep-Learning-for-Frog-Eggs-Quantification/blob/main/images/prediction_0.png" height= "51%" width = "50%"/>

### Objectives
One of our objective during this project was the assessment of feasibility. We wanted to address the following problems. 
 **Problem 1**: How many images in the training set do we need to achieve more than 95% accuracy?
 **Problem 2**: How many epochs do we need to train on to achieve more than 95% accuracy?

To tackle this, we trained our model on different training set sizes, including 24, 48, 72, 96, 120 and 144 images, while keeping the test size constant at 36 images. For each of this six training set sizes, we trained the model on varying epoch numbers of 10, 75, 150, 200 and 300. 

To compare the results, we selected two distinct versions of data set for each training size. These versions were created by using the random state seed 42 and 101 from the total pool of 180 images. 

**Results and conclusions**: We tested our results on the test data set of 36 images. We concluded that it was enough to train the model with 120 images on 150 epochs to get accuracy of up to 95%. 


---

# Made by the Summer 2023 DeVision Team

https://github.com/devision2023/Summer-Research-

## Advisor
Dr. Peter Wolenski

wolenski@math.lsu.edu

## Mathematics Graduate Students:


David Agbolade, Gyaneshwar Agrahari, Kiran Bist, Hayden Bromley, Jackson Knox, Monika Pandey, Iswarya Sitiraju, Gowri Priya Sunkara

## Undergraduate Students:


Narek Bayramyan, Addison DeBlieux, Rohan Durgum, Atif Iqbal, Steph Moore, Artem Mukhamedzianov, Sunella Ramnath, Sahithi Rampally, Houston Smith, Jamar Whitfield, Skylar Wilson
<br>
<br>

<img src="images/mcclogo.gif" alt="Image 2" width="100">
LSU Math Consultation Clinic:<br>
https://www.math.lsu.edu/courses/capstone_course
<br>
<br>

<img src="images/lsulogo.png" alt="Image 1" width="250">
https://lsu.edu/
