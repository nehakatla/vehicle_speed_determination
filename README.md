# vehicle_speed_determination
Vehicle Speed Determination From A Video Of Traffic
Vehicle Speed Estimation using Image processing
Introduction: Nowadays, with the continuous increase of vehicle in the road, traffic management authority requires better traffic surveillance system. With more vehicles, the number of accidents on the road rises up each year. Speed is now the single biggest cause of road accidents. Enforcing speed limit is one of the ways to eliminate speed related accidents. 

Traffic surveillance systems for vehicle detection and speed measurement play an important role in enforcing speed limits. They also provide relevant data for traffic control such as vehicle speed, traffic count etc. Those systems are divided in intrusive and non-intrusive sensors [1].

Intrusive sensors are usually based on inductive loop detectors. Although these sensors are used widely, they have complex installation and high maintenance, promotes asphalt deterioration and also can be damaged by wear and tear. It also requires line sight connection between vehicle and the equipment.

Proposed Technique: This section details the main steps of the proposed technique. We use the basics such as background subtraction, thresholding and other morphological transformation to detect the vehicles. After that detecting contour and the center of it, we find the speed of each vehicle. 3.1 Pre-Processing A camera has been used for recording vehicle movement. Before even beginning the image processing, it is vital to convert the video into the frames. In pre-processing the video has converted into the frames. At first, cv2.VideoCapture function is used where the video is passed as an argument.

This helps load up the video for image processing. In OpenCV, the read function is used to get each frame. The various parameters such as number of frames, frame rate, frame size are extracted in pre-processing. There are a total of 1244 frames in this video. It has a frame rate 24 frames per second. The frame size is of 1920x1080 pixels, which has been retrieved using the shape function. The get function has been used to obtain this information but with different flags.

Perspective Transformation Perspective transformation helps to reduce error in speed estimation. A video can be taken from any angle but it is essential to align it with the global coordinate. Since we can find the pixel covering the length and width of an image and pixel value for any angular dimension cannot be found, it is necessary to perform perspective transformation. The purpose of this is to transform each frame into a plain sheet so that position of any vehicle can be found from the pixel values. In OpenCV it is done with cv2.warpPerspective function.

