# CS3244-ML-Project
Blind people voice guide app
<br/>Created by National University of Singapore CS3244 Machine Learning Group 25 and 26. All of us are equally contributed.
<br/>[Jin Shuyuan](https://github.com/CoderStellaJ), [Mou Ziyang](https://github.com/mouziyanglovestudy), [Tian Xin](https://github.com/tianxin9628), [Tian Xueyan](https://github.com/xueyantian), [Wang Tengda](https://github.com/JacobWangTengda), [Zhao Tianze](https://github.com/tankztz)

### 1. App features
- GPS location share 
  <br/>location is shared to family to ensure blind people's safety in case of emergency.
- Camera based image capturing 
  <br/>capture real-time view in front of the user.
- Object detection and classification
  <br/>focus on human object
- Moving direction determination
  <br/>based on bounding box size in sequencial images to determine whether the peron is moving to/away from the user.
- Voice Guide
  <br/>based on object classification and moving direction, output audio guide (a person is moving to you/ a person is moving away from you)
  
  
### 2. Research on dataset and [neural network](https://towardsdatascience.com/r-cnn-fast-r-cnn-faster-r-cnn-yolo-object-detection-algorithms-36d53571365e) (4.1 ~ 4.2)

Neural Network |NN Link| Description | Paper
--- | --- | ---| --- |
YOLOv3 |https://pjreddie.com/darknet/yolo/    https://github.com/AlexeyAB/darknet  (for both windows and linux) |YOLO is a state-of-the-art, real-time object detection system. It has Pretrained Convolutional Weights which is tarined on Imagenet. | https://pjreddie.com/media/files/papers/yolo.pdf |
Faster R-CNN  |https://github.com/ShaoqingRen/faster_rcnn| |https://papers.nips.cc/paper/5638-faster-r-cnn-towards-real-time-object-detection-with-region-proposal-networks.pdf | 

![github-small](https://github.com/CoderStellaJ/CS3244-ML-Project/blob/master/Baselines.PNG)

Dataset| Link| Description |
---|---|---|
ImageNet | http://www.image-net.org/ |  |
COCO dataset|http://cocodataset.org/#home ||
Pascal VOC challenge|http://host.robots.ox.ac.uk/pascal/VOC/index.html| |

### 3. Detailed instructions for setting up YOLOv3

The official [YOLOv3](https://pjreddie.com/darknet/yolo/) is implemented using C language on Linux OS. For our convenience, a simplified [pytorch version](https://github.com/eriklindernoren/PyTorch-YOLOv3) is used for this project.

The README.md page of [Pytorch-YOLOv3](https://github.com/eriklindernoren/PyTorch-YOLOv3) has instructions for downloading and setting up. But due to difference in OS, the following is details for Windows OS setting up. You can also record down your process of setting up for MacOS.

#### For Windows
- Make sure your laptop has Python installed. Anaconda is recommended for installing Python as it helps to install various dependencies.
- Run the following commands using Git Bash
```
    $ git clone https://github.com/eriklindernoren/PyTorch-YOLOv3
    $ cd PyTorch-YOLOv3/
    $ pip3 install -r requirements.txt
```
- Download pretrained weights
<br/>First, make sure your laptop has wget, download at https://eternallybored.org/misc/wget/. I chose 1.19.1 .zip version because this contains windows certificate. Also remember to add the path of wget.exe to environment path setting. 
<br/> Then run commands to download weights from websites, this process takes about 10 mins.
```
$ cd weights/
$ bash download_weights.sh
```
- Obtain COCO dataset
As it's not practical to download the whole set of data on our own laptop, we can just dowload a part of it. Run the following commands, for the second command, after running some time, you can press Ctrl+C to interrupt it.
```
$ cd data/
$ bash get_coco_dataset.sh
```

### NN implementations (4.3 ~ 4.6)
 
### Moving direction determination (4.7 ~ 4.10)
compare bounding box size in sequential images
 
### Result (4.11 ~ 4.13)
 
### Paper writing (4.16 ~ 4.17)
overleaf online latex using AAAI author toolkit
 
### Detailed implementation

