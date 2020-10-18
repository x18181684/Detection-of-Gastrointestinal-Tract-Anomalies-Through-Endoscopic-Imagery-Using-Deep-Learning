## Detection-of-Gastrointestinal-Tract-Anomalies-Through-Endoscopic-Imagery-Using-Deep-Learning
Dataset containing images from inside the gastrointestinal (GI) tract. The collection of images are classified into three important anatomical landmarks and three clinically significant findings. 

Detection and classification of abnormalities in pathological digital images is quite challenging as the machine may not be able detect them perfectly. Researchers are coming up with different kind of algorithms so that machine learns quickly and performs at their best. So, in this paper, Faster R-CNN method has been taken to detect the presence of gastrointestinal anomalies in endoscopic images. Faster R-CNN Inception V2 network has been configured with a pre-trained COCO model and made it adapted to our specific line of task, then it evaluated the dataset consisting of around 900 manually annotated endoscopic medical images. The model’s results were finally analyzed and evaluated using COCO detection metrics Average Precision (AP) and Average Recall (AR). 

# Data Preparation
The selected images have been taken by the process of random sampling class wise and resized to 700x500. Further, chosen mages were annotated by using the labelImg application. All the images are in jpeg format initially. After labeling the images, the annotations were stored in the form of pascal voc xml format.
The three selected classes are – Esophagitis, Polyps and Ulcerative colitis. 


