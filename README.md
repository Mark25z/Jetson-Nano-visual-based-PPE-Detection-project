This repo is a learning project that utilize Jetson Nano to create a visual-based PPE (personal protective equipment) usage application, this project follow Nvidia provided guideline for hands-on Jetson project which can be found here.
https://github.com/dusty-nv/jetson-inference

To Run this project, you will need.

Hardware: Nvidia Jetson Nano / Jetson Orin with Camera (USB Camera or Raspberry Pie Camera) with Internet connection.
Setup your Nvidia Jetson by following this guide:
Getting Started with AI on Jetson Nano
https://learn.nvidia.com/courses/course-detail?course_id=course-v1:DLI+S-RX-02+V2

Software Used: Jetpack 5.1.3, python 3.8.10, torch 2.1 (link), torchvision 0.16

Dataset:
Dataset used for this project can be found on Roboflow at https://roboflow.com/
VOC Format Dataset was used in this instance to train Mobilenet-SSD AI model for object detection project.

Instruction to try using this project:
Clone your Jetson environment repo by following this guide.
https://github.com/dusty-nv/jetson-inference/blob/master/docs/building-repo.md
Remember to pick Mobilenet-SSD model.

Download and place both ssd-mobilenet.onnx and safetyEquipmentDetection.py in the prepared environment.

Run the script with this command to see it in action on your Jetson.
python safetyEquipmentDetection.py /dev/video0

Instruction to replicate this project:
Clone your Jetson environment repo by following this guide.
https://github.com/dusty-nv/jetson-inference/blob/master/docs/building-repo.md
Remember to pick Mobilenet-SSD model.

Login to roboflow.com and download community shared Safe-Unsafe PPE dataset under VOC format.

Place your downloaded Dataset inside jetson-inference/python/training/detection/ssd repo, remember to follow VOC dataset type folder structure.

Follow https://github.com/dusty-nv/jetson-inference/blob/master/docs/pytorch-ssd.md guide to train your Mobilenet-SSD AI model to recognize and correctly classify PPE Safe / Unsafe images.

Export your best-selected model to ONNX, and test it with detectnet command. Or edit the ssd_inference.py python file to call to your newly retrained AI modal for additional outputs / usage needs.

Sample output of this project
![image](https://github.com/user-attachments/assets/2f6b7ce1-61bb-4378-abd2-3f14361c6f3a)
![image](https://github.com/user-attachments/assets/a21a4b1a-712e-4007-bbd2-64b7caae49cc)
