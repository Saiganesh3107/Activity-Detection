LIBRARIES USED : 
Commands to install :  
          pip install opencv-python-headless 
          pip install ultralytics 
          pip install numpy 
          pip install matplotlib

ACTIVATE IN TERMINAL: 
1.Setup and Imports: 
This cell imports required libraries, such as OpenCV and 
Ultralytics, and loads any pre-trained YOLO models. Run it to 
ensure all dependencies are ready. 
2. Load Video Input: 
Locate this cell to specify the path of the video you want to 
analyze. Modify the file path here if needed to use a different input 
video. 
3. Activity Detection and Situation Analysis: 
This core processing cell uses YOLO and activity recognition 
techniques to detect and classify actions within the video frames. 
Running it will analyze each frame and apply activity classification 
logic. 
4. Generate Video Summary: 
This cell creates a summarized video based on detected activities 
and situations. It processes the analyzed frames, selecting key 
moments for the final summary output.
