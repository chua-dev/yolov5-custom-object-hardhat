In this repository, I going to use the latest Yolov5 (Object D. Model) to perform Custom Object Detection training.  
The custom Object in this detection model are Hardhat/Safetyhat. But i include second class which is normal head so model can differentiate who wear and who didn't.  

Class list as below:  
class_dict = { 'hat': 0, 'person': 1 }  

### Reason I wanted try with yolov5 as base model  
i) Lighter speed and slightly better accuracy  
ii) Option to choose for n(nano), s(small), m(medium), l(large), x(extra large) as pretrained base model weight to fit your need, depend on where you deploy.  
iii) You Only Look Once had been one of the most reputable; and favored by alot of people who want to train a custom object detection model!  


### Datasets Information  
Name: SafetyHelmetWearing-Dataset(SHWD), 安全帽佩戴检测数据集  
Datasets description: Largly from construction image in China, but still include a portion from others country  
Total Images              : 7581 images  
class 0 safety helmet     : 9044 anno instance  
class 1 normal head person: 111514 anno instance (I include some normal cap helmet so model wont make normal cap mistake)  
Note: Some normal head person are from SCUT-HEAD  

### Data Preprocessing
The datasets i collected are annotated in VOC .xml method, the yolo v5 require us to use YOLO txt annotation format, I managed to convert from xml to txt YOLO by using [this method](https://github.com/chua-dev/yolov5-xml-VOC_anno--to-txt-YOLO_format-). 


### Training Result (12/4/22)  

#### Precision  
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)  

#### Precision & Recall  
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)  

#### Recall  
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)  

#### 30 Epoch Result  
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)  

#### Prediction Validation Image Compare to Label  
Label 0  
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)  

Pred 0  
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)  

Label 1  
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)  

Pred 1  
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)  

Label 2  
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)  

Pred 2  
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)  