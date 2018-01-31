## Object Detection Progress Tracker

Last few years have seen great progress made in the domain of Object Detection. With powerful classification networks as backbone, more and more well-designed detection heads have been proposed to handle the dilemma of recognition and localization. This repo serves as a tracker of these progress.

## 2-stage

Model         | Backbone  | Tricks   | mAP@VOC| mAP@COCO| Inference Time | Paper  | Date   | Note
--------------|-----------|----------|--------|---------|----------|------------|--------|---------
R-CNN | VGG16 | - | 
Fast R-CNN |
Faster R-CNN |
Faster R-CNN | ResNet-101-C4 | Yes | - | 34.9 | - | [Deep residual learning for image recognition] | - 
R-FCN | | | | | | 
Deformable Conv | Aligned-Inception-ResNet | Yes | - | 37.5 | - | [Deformable Convolutional Networks] | -
Faster R-CNN w FPN | ResNet-101-FPN | - | - | 36.2 | - | [Feature pyramid Networks for Object Detection] | -
Faster R-CNN by G-RMI | Inception-ResNet-v2 | - | - | 34.7 | - | [Speed/accuracy trade-offs for modern convolutional object detectors] | -
Mask R-CNN |
Light-haed R-CNN |


## 1-stage

Model | Backbone | Tricks | mAP@VOC | mAP@COCO | Inference Time | Paper | Date
---------|-----------|----------|----------|----------|------------|------------|----------
YOLO |
SSD |
YOLO v2 |
RetinaNet |
