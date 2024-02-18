# <p align="center">Project-Tachikoma</p>

### <p align="center">Stand Alone General Purpose Explore Mobile Machine</p>
<br/>

<p align="center">
    <img src="https://github.com/estelelenath/ProjectTachikoma/blob/main/img/loading.gif?raw=true" width="673" height="464"></center>
</p>

<br/>
<br/>

## The goals / steps of this project are the following:
 - Step 1: ASD
   - asd
   - asd
 - Step 2: ASD
   - asd
   - asd
 - Step 3: ASD
   - asd
   - asd
     - asd
       - asd
       - asd
     - asd
   - asd
     - asd
     - asd
 - Step 4: ASD
   - asd
     - asd
     - asd
   - asd
 
<br/>


<p align="center">
    <img src="https://github.com/estelelenath/ProjectTachikoma/blob/main/img/loading.gif?raw=true" width="673" height="464"></center>
</p>
<p align="center">Roadmap of Project Tachikoma</p>
<br/>


## Step 1. ASD - Warming up
***
Goal : asd

<br/>

## Vehicle Detection
<figure>
    <p align="center">
        <img src="https://github.com/estelelenath/ProjectAsurada/blob/main/pic/yolo_benchmark.gif?raw=true" width="400" height="225">
        <img src="https://github.com/estelelenath/ProjectAsurada/blob/main/pic/fasterrcnnyolo_benchmark.gif?raw=true" width="400" height="225">
    </p>
    <figcaption align="center"> Comparison of YOLO and Faster R-CNN ( left: YOLO / right: Faster R-CNN )</figcaption>
    <figcaption align="center"> source: https://github.com/alen-smajic/Real-time-Object-Detection-for-Autonomous-Driving-using-Deep-Learning</figcaption>
</figure>

<div align="center">

   Model | Size(pixels) | mAP^val 50-95 | Speed CPU ONNX(ms) | FLOPs     
  :------------: | :-------------: | :-------------: | :-------------: | :-------------:
   YOLO8n | 640 | 37.3 | 80.4 | 8.7
   YOLO8s | 640 | 44.9 | 128.4 | 28.6
   YOLO8m | 640 | 50.2 | 234.7 | 78.9
   YOLO8l | 640 | 52.9 | 375.2 | 165.2
   YOLO8x | 640 | 53.9 | 479.1 | 257.8
</div>

### Implementation
```python
for id, pt in self.center_points.items():
                dist = math.hypot(cx - pt[0], cy - pt[1])

                if dist < 35:
                    self.center_points[id] = (cx, cy)
                    self.box_size[id] = w * h

                    self.distance_from_other[id] = math.dist((cx, cy), self.user_vehicle_point)

                    objects_bbs_ids.append([x1, y1, x2, y2, self.space_difference, self.distance_difference_from_other_vehicle, id, "id_nr"])
                    same_object_detected = True
                    break

            # New object is detected we assign the ID to that object
            if same_object_detected is False:
                self.center_points[self.id_count] = (cx, cy)
                self.box_size[self.id_count] = w * h
                self.distance_from_other[self.id_count] = math.dist((cx, cy), self.user_vehicle_point)
                objects_bbs_ids.append([x1, y1, x2, y2, 0, 0, self.id_count, "id_nr"])
                self.id_count += 1
```


<div align="center">

~~~
CUDA Install and Configuration at Desktop
~~~
</div>

<div align="center">

   
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  +----------------------------------+
  |     Model     |      Version     |
  +===============+==================+
  |  GPU          |   GeFroce 4070 Ti|
  |  CUDA cores   |   7680           |
  |  CUDA         |   11.8           |
  |  cudnn        |   8.9.0          |
  |  torch        |   2.0.1+cu118    |
  |  torchaudio   |   2.0.2+cu118    |
  |  torchvision  |   0.15.2+cu118   |
  |  OS           |   Windows 11     |
  +----------------------------------+
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

</div>
* Don't forget a enviroment variables

```bash
Project Root
├── /control
│ ├── /launch
│  └── yolobot_control.launch.py
│ ├── /scripts
│  └── robot_control.py
│ ├── CMakeLists.txt
│ └── package.xml
├── /description
│ ├── /launch
│  └── spawn_yolobot.py
│  └── spawn_yolobot_launch.launch.py
│ ├── /robot
│  └── yolobot.urdf
│ ├── CMakeLists.txt
│ └── package.xml
├── /gazebo
│ ├── /launch
│  └── yolobot_launch.py
│  └── start_world_launch.py
│ ├── /world
│  └── yolo_test.world
│ ├── CMakeLists.txt
│ └── package.xml
├── recognition
│ ├── /launch
│  └── launch_yolov8.launch.py
│ ├── /scripts
│  └── yolov8n.pt
│  └── yolov8_ros2_pt.py
│  └── yolov8_ros2_subscriber.py
│  └── .dockerignore
│  └── .gitattributes
│  └── .gitignore
│ ├── CMakeLists.txt
│ └── package.xml
├── msg
│ ├── /msg
│  └── InferenceResult.msg
│  └── Yolov8Inference.msg
│ ├── CMakeLists.txt
│ └── package.xml
└── requirements.txt
```

## Conclusion
ASD
<br/>

## Outlining Future Work
ASD
<br/>


<div align="center">

~~~
-Fin.-
~~~
</div>
