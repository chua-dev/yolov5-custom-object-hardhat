Yolov5 Custom Object Detection Training  

Custom Object Detection for Hardhat/Safetyhat  

class_dict = {  
    'hat': 0  
    'person': 1  
}  

Datasets  
Name: SafetyHelmetWearing-Dataset(SHWD), 安全帽佩戴检测数据集  
Datasets description: Largly from construction image in China, but still include a portion from others country  
Total Images: 7581 
class 0 safety helmet: 9044 anno  
class 1 normal head person: 111514 anno (I include some normal cap helmet so model wont make normal cap mistake)
Note: Some normal head person are from SCUT-HEAD