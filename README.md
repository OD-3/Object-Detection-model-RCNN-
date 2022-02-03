# Object Detection (model RCNN)
The purpose of this project is to detect object in given images. For detecting object first, the dataset is created and then it is trained using RCNN model. After training dataset, the trained dataset is used to detect object in different images.


## Project Title:
### Object Detection and Image Segmentation.

Project Members:
Drashti Dobariya, Jahanvi Gajera, Shruti Shekhat

# 1.	Abstract:
The purpose of this project is to detect object in given images and videos. For detecting object first, the dataset is created and then it is trained using different models. In this we have used RCNN model (Region based Convolution Neural Networks). After training dataset, the trained dataset is used to detect object in different images and videos.

# 2.	Creating Dataset:
For creating dataset, the selected object was ‘Car’. Some images were having single car, some with 3-4 cars, some with 6-8 cars and with heavy traffic were used. For this project 11 images were trained.

**Labeling Data in Dataset:**<br />
There is different type of Labels:<br />
•	Image Segmentation<br />
•	Object Detection<br />
•	Classification<br /><br />
 ![alt text](https://user-images.githubusercontent.com/57354105/152315913-9a28844a-01ce-44a2-92b8-c4e44ad82c37.png)
 

In this project labels for object detection are done using Rectangles (Draw boxes to detect specific objects within images.) and Polygons (Segment objects for detection within image frames.).<br /><br />
![alt text](https://user-images.githubusercontent.com/57354105/152317048-133507db-6d38-490d-aad5-8860535cc362.png) <br />

Then export the dataset in JSON document.<br /><br />
![alt text](https://user-images.githubusercontent.com/57354105/152317282-b0c350a3-4843-4d72-bf9f-deb728916277.png) <br />

 

# 3.	Implementation: 
There are quite a few implementations for different model types and our dataset should work with all of them.
We chose to use ones included in tensorflows official repo. Note that most of the models are under the research directory. These are not always officially maintained.

There is a great resource to get started with the included tensorflow model here:
•	Tensorflow object detection setup guide
•	Tensorflow Model Zoo
Any implementation we use will need to read in the images and annotations. So, keep it in mind that we’ll want to check we’re reading them correctly.



# 4.	Training Dataset:
**There are many different models for object detection:**<br />
i.	SSD (Single Shot MultiBox Detector)<br />
ii.	YOLO (You Only Look Once)<br />
iii.	Mask R-CNN<br />

->	In this project Mask R-CNN model is used.<br />
->	The model generates bounding boxes and segmentation masks for each instance of an object in the image. It's based on Feature Pyramid Network (FPN) and a ResNet101 backbone.<br /><br />

**-> The repository includes:**<br /><br />
•	Source code of Mask R-CNN built on FPN and ResNet101.<br />
•	Training code for MS COCO<br />
•	Pre-trained weights for MS COCO<br />
•	Jupyter notebooks to visualize the detection pipeline at every step<br />
•	ParallelModel class for multi-GPU training<br />
•	Evaluation on MS COCO metrics (AP)<br />
•	Example of training on your own dataset<br /><br />

**-> Training own Dataset:**<br /> <br />
->	To train the model on our own dataset we will need to extend two classes:<br /><br />
i.	Config: This class contains the default configuration. Subclass it and modify the attributes we need to change.<br />
ii.	Dataset: This class provides a consistent way to work with any dataset. It allows us to use new datasets for training without having to change the code of the model. It also supports loading multiple datasets at the same time, which is useful if the objects we want to detect are not all available in one dataset.<br /><br />
 ![alt text](https://user-images.githubusercontent.com/57354105/152317424-c5a485f6-99b8-4cb7-99af-796573bf7bf8.png)

             

# 5.	Use of Trained Dataset:
After training dataset using model, use trained dataset to detect specified object in non-trained images.<br /><br />
![alt text](https://user-images.githubusercontent.com/57354105/152317497-8e5cbaf0-4f61-4877-aa23-cce9d2f32cc5.png)

 
