## Object Detection Progress Tracker

Last few years have seen great progress made in the domain of Object Detection. With powerful classification networks as backbone, more and more well-designed detection heads have been proposed to handle the dilemma of recognition and localization. This repo serves as a tracker of these progress.

## 2-stage

Model    | Backbone  | Tricks| mAP@VOC| mAP@COCO| FPS | Paper  | Date   | Note
------------|-----------|-------|----|----|----|------------|------|------
R-CNN | VGG16 | - | 
Fast R-CNN | VGG16 | - | 70.0 | 19.7 | - | [Fast R-CNN] | 15.04 | -
Faster R-CNN | VGG16 | - | 73.2 | - | - | [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks] | 15.06 | -
Faster R-CNN+++ | ResNet-101-C4 | 1,2,3 | 73.8 | 34.9 | - | [Deep Residual Learning for Image Recognition] | 15.12 | -
R-FCN | ResNet-101 | 4 | 80.5 | 29.9 | 6 | [R-FCN: Object Detection via Region-based Fully Convoluational Networks] 16.05 | - 
Deformable Conv | Aligned-Inception-ResNet | 1,3 | - | 37.5 | - | [Deformable Convolutional Networks] | -
Faster R-CNN w FPN | ResNet-101-FPN | - | - | 36.2 | - | [Feature Pyramid Networks for Object Detection] | -
Faster R-CNN by G-RMI | Inception-ResNet-v2 | - | - | 34.7 | - | [Speed/accuracy Trade-offs for Modern Convolutional object detectors] | - | COCO206 winner
Mask R-CNN |  ResNeXt | 6 | - | 39.8 | - | [Mask R-CNN] | 17.03 | ICCV2017 Best Paper
Light-haed R-CNN | ResNet-101-FPN | 4,6 | - | 41.5 | - | [Light-Head R-CNN: In Defense of Two-stage Object Detector] | 17.11 | -
Light-haed R-CNN | Xception | - | - | 30.7 | 102 | [Light-Head R-CNN: In Defense of Two-stage Object Detector] | 17.11 | -

Tricks list
1. box refinement
2. context
3. multi-scale testing
4. multi-scale training
5. OHEM
6. RoIAlign

Note:
1. Pascal VOC AP results are evaluated with IOU 0.5. Models are trained on VOC07+12, tested on VOC07.
2. MS COCO results are reported with training on trainval35k, testing on test-dev set.
## 1-stage

Model    | Backbone  | Tricks| mAP@VOC| mAP@COCO| FPS | Paper  | Date   | Note
------------|-----------|-------|----|----|----|------------|------|------
YOLO | Custom | - | 63.4 | - | 45 | [YOLO: You Only Look Once] | - | -
SSD500 | VGG16 | - | 75.1 | 24.4 | 23 | [SSD: Single Shot Detector] | 15.12 | -
SSD | ResNet-101 | - | - | 31.2 | 8 | [DSSD: Deconvolutional Single Shot Detector] | 17.01 | -
YOLO v2 | DarkNet-19 | - | 78.6 | 21.6 | 40 | [YOLO9000: Better, Faster, Stronger] | - | -
DSSD | ResNet-101 | - | - | 33.2 | 6 | [DSSD: Deconvolutional Single Shot Detector] | 17.01 | -
RetinaNet | ResNet-101-FPN | - | - | 39.1 | - | [Focal Loss for Dense Object Detection] | 17.08 | -
