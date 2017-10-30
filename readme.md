easyMTracking
===================================
## Methods:
  multiple target tracking, only pedestrian tracking was implemented at present!
  Detection by yolov2, calman filter predict motion trajectory, and build assignment problem sovled by Hungarian algorithm .

### Demo video:
	Need cuda8.0 and cudnn6.0 , and opencv3.3.0 on win10,
#### 1.Download video and yolo wieghts:
	yolo-voc.weights:http://pjreddie.com/media/files/yolo-voc.weights
	video: http://pan.baidu.com/s/1cwHj6u or other video.
	put video file and weights file into "x64/Release" 
#### 2. cd  "x64/Release" , and cmd run multi_tracker_yolo_voc_demo.cmd

![](https://github.com/blakeliu/easyMTracking/blob/master/x64/Release/PETS09-S2L1_test_result_20171030174345.gif)

### 3. About paramters:
		"{ t  tracker          |0  | tracker type: 0-video sort kalman, 1- seq sort kalman | }"
		"{ d  debug           |0  | debug : 0-yes, 1-false | }"
		"{ mint  minTraceSize |8  | min trace size > 2 | }"
		"{ in   inFile        |   |input video| }"
		"{ out  outFile       |   |write processed video| }"
		"{ seq  sequences     |PETS09-S2L1 |process sequences| }"
		"{ det  detector      |0  |detector type: 0-identified_seq, 1-yolov2 |}"
		"{ net  netfile       |  |dl net file |}"
		"{ weight  weightfile |  |dl net weight file |}"
		"{ objnamefile  objectnamefile |voc.names  |data sets object names |}"
		"{ filname  filtername |person  | custom made object names like: person,car,bicycle,bus | }"
    
    
 ### Build
	1.Istall win10 vs2015, cuda8.0 and cudnn6.0
	2.Install opencv3.3.0 ,here i used opencv-3.3.0-vc14.zip, link:https://sourceforge.net/projects/opencvlibrary/files/opencv-win/3.3.0/opencv-3.3.0-vc14.exe/download
	3.opencv open_tracker.sln, and build x64 release.
 
 
 
 ### Reference materials and projects:
	1.Multitarget-tracker,https://github.com/Smorodov/Multitarget-tracker
	2.Simple Online and Realtime Tracking, https://arxiv.org/abs/1602.00763
	3.windows yolo https://github.com/unsky/yolo-for-windows-v2

