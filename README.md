# Detection-of-Gastrointestinal-Tract-Anomalies-Through-Endoscopic-Imagery-Using-Deep-Learning
Dataset containing images from inside the gastrointestinal (GI) tract. The collection of images are classified into three important anatomical landmarks and three clinically significant findings. 

Detection and classification of abnormalities in pathological digital images is quite challenging as the machine may not be able detect them perfectly. Researchers are coming up with different kind of algorithms so that machine learns quickly and performs at their best. So, in this paper, Faster R-CNN method has been taken to detect the presence of gastrointestinal anomalies in endoscopic images. Faster R-CNN Inception V2 network has been configured with a pre-trained COCO model and made it adapted to our specific line of task, then it evaluated the dataset consisting of around 900 manually annotated endoscopic medical images. The model’s results were finally analyzed and evaluated using COCO detection metrics Average Precision (AP) and Average Recall (AR). 

### Research Objective
To implement a developed robust deep learning process using faster regional convolutional neural network from raw endoscopic medical images to perform Gastrointestinal tract anomalies detection.

### Research Question (RQ)

How can Faster R-CNN Inception V2 network can improve in detecting the gastrointestinal tract anomalies from raw endoscopic medical images? 

### Dataset Details

We have chosen Kvasir dataset for our research project (Pogorelov et al., 2017). The chosen dataset comprises of 4000 gastrointestinal tract jpg format pictures and having 8 classes. The resolution of every GI tract image is different, and it ranges from 720x576 up to 1920x1072. So as to perform the task to create object detection classifier we have chosen a secondary image dataset which consist of 500 images per class. But we have considered a total of 900 images and out of which only three classes have been considered for this disease detection experiment.

### Data Preparation

The selected images have been taken by the process of random sampling class wise and resized to 700x500. Further, chosen mages were annotated by using the labelImg application. All the images are in jpeg format initially. After labeling the images, the annotations were stored in the form of pascal voc xml format.
The three selected classes are – Esophagitis, Polyps and Ulcerative colitis. 

### Model Building and Training

In order to train and build the model, we have used tensorflow library an open sourced library used for doing high computational work. Anaconda virtual environment was used for training, evaluating the model. Here, we have applied Faster RCNN inception V2 network. (Pre trained models have been used in this project i.e, COCO).
The image dataset has been randomly divided into 80% training and 20% test data i.e, 720 training images and 180 test images. Here, the training dataset have been used to train the model and the test dataset for analyzing and assessing the model. The loss values have been recorded and the model which is trained will be used to understand the quality of anomaly prediction.

### Implementation

In order to train and build the model, we have used tensorflow library an open sourced library used for doing high computational work. Anaconda virtual environment was used for training, evaluating the model. Here, we have applied Faster RCNN inception V2 network. (Pre trained models have been used in this project i.e, COCO).
The image dataset has been randomly divided into 80% training and 20% test data i.e, 720 training images and 180 test images. Here, the training dataset have been used to train the model and the test dataset for analyzing and assessing the model. The loss values have been recorded and the model which is trained will be used to understand the quality of anomaly prediction.

### Evaluation

Implementation has been done by tensorflow installing Object Detection library and utilizing a pre-trained tensorflow model. The detection evaluation metrics we have used here is Pycocotools is a python API specially designed to work for Microsoft COCO dataset. This API assists in loading, parsing and displaying the visualizations of annotations in COCO. Pycocotools 2.0 have been installed using pip in our conda environment. The evaluation metrics such as average recall (AR), Average Precision (AP) for each category or class to measure object detector performance.
The tensorboard provides the graphs and other metrics such as learning rate, classification loss, Total loss graphs while the model is training. The loss graph in figure 4 shows the values ranging from 0 to 0.01 after the model being trained for 50,000 oversteps iterations. Which is a good loss graph, meaning the model will not overfit. Also, in figure 5 the box classifier loss/classification loss graph shows that the graph in the range of 0 to 0.1. This is the final layer of faster R-CNN architecture which determines which class belongs to polyps or ulcerative colitis or esophagitis.
The localization loss graph represents the final layer of the architecture for the bounding boxes of the object that is coordinates of the objects (ulcerative colitis, polyps and esophagitis). Figure 6 represents graph values are ranging between 0 to 0.1, shows the model is learning well to localize the objects

### Results

Keeping IOU between 0.5:0.95, we evaluated our models and have calculated the average precision and average recall for the model. Our detection model has showed average precision (AP) of 65.2% in time = 0.28 seconds. When we considered all the test images bounding box, the average recall (AR) turned out to be 50% which showed to be little lesser than the precision.  Thus, we can say that the design was not well enough, or we can say that the pre-trained model couldn’t perform up to the mark. Also, we have observed that our model has failed most of the times in detecting the presence of esophagitis in test images.

### Conclusion and Future Work

In our report, we have presented our state-of-art gastrointestinal tract anomaly detection model on KVASIR dataset using Faster RCNN. Our experiment suggested that the average accuracy was 65.2% using optimizer IOU 05:0.95 for time at 0.28 seconds, which can be fine in case of real scenario. The average recall found out to be 50%, which was not fully up to our expectations. The detection results also showed us that the test images of esophagitis were not detected by our detection model most of the time.
In future, we will include more training images and try to combine two more pre-trained inception models to improve our current detection performance.








