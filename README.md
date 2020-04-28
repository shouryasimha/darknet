![Darknet Logo](http://pjreddie.com/media/files/darknet-black-small.png)

# Darknet #
Darknet is an open source neural network framework written in C and CUDA. It is fast, easy to install, and supports CPU and GPU computation.

Yolo v4 paper: https://arxiv.org/abs/2004.10934

Yolo v4 source code: https://github.com/AlexeyAB/darknet

For more information see the [Darknet project website](http://pjreddie.com/darknet).

For questions or issues please use the [Google Group](https://groups.google.com/forum/#!forum/darknet).

## darknet-YoloV3
## Import this repo on command prompt :

echo "# darknet-YoloV3" >> README.md

git init

git add README.md

git commit -m "first commit"

git remote add origin https://github.com/shouryasimha/darknet-YoloV3.git

git push -u origin master

## Link to the Colab Notebook to run the model on windows : https://colab.research.google.com/drive/1CE8RJArN37rdFeZzjjBvR5BXHRwYvi3Z#scrollTo=EoisahzAUWWL

#### crazing_1.txt -the sample for creating the annotation.txt file

#### train.txt - example for the train.txt file (the file that contains the absolute path to the images)

#### input_anomaly.data -the file that contains the path for train.txt,test.txt, number of classes,the path to the output folder(backup folder for weights)

#### class.names-then .names file consisting the name of the classes.

#### Text_worked.py - Creates the predicted object class % and the x_center,y_center, width and height of the bounding boxes for the test images

#### Link to the colab notebook to create inputs for the YoloV3 Model : https://colab.research.google.com/drive/1f3WCUqW2YJt_wesRsRWBSDJui-eWnkw6#scrollTo=pbS6IMpaaJ6e

#### Note: the images annotations should be in the same folder if you are using this repo

## Observations:

1)If the image resolution is low, detecting small object classes becomes difficult for the images.

2)After calculating anchor boxes, still the the small object class detection was not more than 50%

3)Reducing the mini_vatch size = batch/subdivisions will increase the computation speed.

4)Model with highest mAP should be chosen to detect objects in test images


6)Increasing the number of anchors , increases the avg IOU and possibility to detect the small classes.But remember to change the masks.
#### Note : Don't do this unless you are an expert in DL or CNN, bcz this will throw an error.
7)Increasing the max_batches resulted in increase in loss

#### Future Work:
Build Models using yolov3.spp and yolov3_5l as they are customised model and can help in detecting small objects in large images.
