
# basasuya-yolo3

[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE)

<img src="./desktop.png" width="450px" height = "300px"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src="./detect.png" width="400px" height = "300px"/>


A Keras implementation of YOLOv3 (Tensorflow backend) inspired by [allanzelener/YAD2K](https://github.com/allanzelener/YAD2K) and [qqwweee/keras-yolo3](https://github.com/qqwweee/keras-yolo3)

---

## Use Official Parameter 

1. Download YOLOv3 weights from [YOLO website](http://pjreddie.com/darknet/yolo/).
2. Convert the Darknet YOLO model to a Keras model.
3. Run YOLO detection.

```
wget https://pjreddie.com/media/files/yolov3.weights
python convert.py yolov3.cfg yolov3.weights model_data/yolo.h5
# yolo.h5 is the netwoerk parameter
```

## Training By Yourself

1. Generate your own annotation file and class names file.  
    One row for one image;  
    Row format: image_file_path box1 box2 ... boxN;  
    Box format: x_min,y_min,x_max,y_max,class_id (no space).  
    For VOC dataset, try `python voc_annotation.py`
2. download backend from below and place yolo_weights.h5 in model_data folder
    https://drive.google.com/drive/u/2/folders/1Qj46bDCBWMbIXm7rPZCIjCVIczxaj2l_
3. Modify train.py and start training.  
    `python train.py`  
    You will get the trained model model_data/my_yolo.h5.

---

## Prepare The Environment
1. install python3 and some library(recommend through virtualenv)
```
 pip install -r requirements.txt
```
2. install mongodb

## Run The System
start three terminal and run the next command.
```
$ monogod
```
```
$ cd Visual
$ python3 manage.py runserver 8000
```
```
$ python3 ui.py
```
Wish you enjoy it!