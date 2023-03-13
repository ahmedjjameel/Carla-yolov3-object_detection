# YOLOV3 based Object Detection using Carla Simulator

In this project,

YoloV3 Tensorflow implementation forked from: https://github.com/YunYang1994/tensorflow-yolov3 

![gif img](https://user-images.githubusercontent.com/81799459/224787052-b0d1ba36-252d-4dda-9f0a-ceb95feff586.png)




https://user-images.githubusercontent.com/81799459/224787076-0e9bc4b8-806d-4d54-85d4-ef5c9b733003.mp4




# The Environment

Windows 11 Carla 0.9.14 python 3.7.5 tensorflow-gpu 1.15.0 pygame 1.9.6 opencv-python 4.2.0.34 numpy 1.18.3 pillow 7.1.2

    pip install "tensorflow>=1.15,<2.0"
    pip install --upgrade tensorflow-hub


# Project Directory Structure

    ├ .CARLA_0.9.14
    │   ├── CarlaUE4
    │   ├── Co-Simulation
    │   ├── Engine
    │   ├── HDMaps
    │   ├── PythonAPI
    │   │   ├── carla
    │   │   ├── util
    │   │   ├── examples
    │   │   │ 	├── yolov3_object_detection.py
    │   │   │ 	├── tensorflow_yolov3  
    │   │   │ 	│   │ ├── carla
    │   │   │ 	│   │	│   ├── utils.py


# Setup

Open a command line Go to the Carla Simulator examples path ..\CARLA_0.9.14\PythonAPI\examples

Clone this repo without project folder with the below section

    git init
    git remote add origin https://github.com/umtclskn/Carla_Simulator_YOLOV3_Object_Detection.git
    git pull origin master
    git submodule update --init --recursive


Download COCO weights from this link: https://github.com/YunYang1994/tensorflow-yolov3/releases/download/v1.0/yolov3_coco.tar.gz

    wget https://github.com/YunYang1994/tensorflow-yolov3/releases/download/v1.0/yolov3_coco.tar.gz

extract this file under the below path: ..\CARLA_0.9.14\PythonAPI\examples\tensorflow-yolov3\checkpoint
    tar -xvf yolov3_coco.tar.gz

(type these command at the ..\CARLA_0.9.14\\PythonAPI\examples\tensorflow_yolov3)

    cd..
    python convert_weight.py
    python freeze_graph.py


Open CarlaEU4.exe (..\CARLA_0.9.14)

Run generate_traffic python file for adding pedestrians or vehicles.

    python generate_traffic.py 


Start detecting vehicles, pedestrians or bicycles.

    cd C:\CarlaSimulator\PythonAPI\examples && python yolov3_object_detection.py



# References
1. 
2.
3.



