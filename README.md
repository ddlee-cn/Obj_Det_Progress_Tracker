# Object Detection Progress Tracker

Last few years have seen great progress made in the domain of Object Detection. With powerful classification networks as backbone, more and more well-designed detection heads have been proposed to handle the dilemma of recognition and localization. This repo serves as a tracker of these progress.

## 2-stage

Model    | Backbone  | Tricks| VOC| COCO| FPS | Paper  | Date   | Note | Code
------------|-----------|-------|----|----|----|------------|------|------|-------
R-CNN | VGG16 | - | - | - | -| [Rich Feature Hierarchies for Accurate Object Detection and Semantic Segmentation] | - | CVPR2014 Oral
Fast R-CNN | VGG16 | - | 70.0 | 19.7 | - | [Fast R-CNN] | 15.04 | CVPR2014 Oral | [caffe](https://github.com/rbgirshick/fast-rcnn)
Faster R-CNN | VGG16 | - | 73.2 | - | - | [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks] | 15.06 | NIPS2015 | [MATLAB](https://github.com/ShaoqingRen/faster_rcnn)
Faster R-CNN+++ | ResNet-101-C4 | 1,2,3 | 73.8 | 34.9 | - | [Deep Residual Learning for Image Recognition] | 15.12 | CVPR2016 Best Paper
R-FCN | ResNet-101 | 4 | 80.5 | 29.9 | 6 | [R-FCN: Object Detection via Region-based Fully Convoluational Networks] | 16.05 | NIPS2016 | [caffe](https://github.com/daijifeng001/caffe-rfcn)
Deformable Conv | Aligned-Inception-ResNet | 1,3 | - | 37.5 | - | [Deformable Convolutional Networks] | 17.03 | ICCV2017 Oral | [MXNet](https://github.com/msracver/Deformable-ConvNets)
Faster R-CNN w FPN | ResNet-101-FPN | - | - | 36.2 | - | [Feature Pyramid Networks for Object Detection] | 16.12 | CVPR2017 Poster | [caffe2](https://github.com/facebookresearch/Detectron)
Faster R-CNN by G-RMI | Inception-ResNet-v2 | - | - | 34.7 | - | [Speed/accuracy Trade-offs for Modern Convolutional object detectors] | - | COCO206 winner | [TesnsorFlow](https://github.com/tensorflow/models/tree/master/research/object_detection)
Mask R-CNN |  ResNeXt | 6 | - | 39.8 | - | [Mask R-CNN] | 17.03 | ICCV2017 Best Paper | [caffe2](https://github.com/facebookresearch/Detectron)
Light-haed R-CNN | ResNet-101-FPN | 4,6 | - | 41.5 | - | [Light-Head R-CNN: In Defense of Two-stage Object Detector] | 17.11 | -
Light-haed R-CNN | Xception | - | - | 30.7 | 102 | [Light-Head R-CNN: In Defense of Two-stage Object Detector] | 17.11 | -


## 1-stage

Model    | Backbone  | Tricks| VOC| COCO| FPS | Paper  | Date   | Note | Code
------------|-----------|-------|----|----|----|------------|------|------|-------
YOLO | Custom | - | 63.4 | - | 45 | [YOLO: You Only Look Once] | - | CVPR2016 Oral | [darknet](https://github.com/pjreddie/darknet)
SSD500 | VGG16 | - | 75.1 | 24.4 | 23 | [SSD: Single Shot Detector] | 15.12 | ECCV2016 Oral | [caffe](https://github.com/weiliu89/caffe/tree/ssd)
SSD | ResNet-101 | - | - | 31.2 | 8 | [DSSD: Deconvolutional Single Shot Detector] | 17.01 | -
YOLO v2 | DarkNet-19 | - | 78.6 | 21.6 | 40 | [YOLO9000: Better, Faster, Stronger] | - | CVPR2017 | [darknet](https://github.com/pjreddie/darknet)
DSSD | ResNet-101 | - | - | 33.2 | 6 | [DSSD: Deconvolutional Single Shot Detector] | 17.01 | -
RON384++ | VGG16 | 3,7,8 | 77.6 | 27.4 | - | [RON: Reverse Connection with Objectness Prior Networks for Object Detection] | - | CVPR2017 | [caffe](https://github.com/taokong/RON)
RetinaNet | ResNet-101-FPN | - | - | 39.1 | - | [Focal Loss for Dense Object Detection] | 17.08 | ICCV2017 Best student paper | [caffe2](https://github.com/facebookresearch/Detectron)
RefineDet512 | VGG16 | - | 81.8 | 33.0 | 24.1 | [Single-Shot Refinement Neural Network for Object Detection] | 17.11 | - | [caffe](https://github.com/sfzhang15/RefineDet)
RefineDet512+ | ResNet-101 | 3 | - | 41.8 | - | [Single-Shot Refinement Neural Network for Object Detection] | 17.11 | -


Tricks list

1. box refinement
2. context
3. multi-scale testing
4. multi-scale training
5. OHEM
6. RoIAlign
7. box voting
8. flip

Disclaimer:

1. Pascal VOC AP results are evaluated with IOU 0.5. Models are trained on VOC07+12, tested on VOC07.
2. MS COCO results are reported with training on trainval35k, testing on test-dev set.
3. All code repos are official implementation.
4. Reported FPS are usually on GPU, not comparable actually.
