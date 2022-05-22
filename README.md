# Korean-Number-Plate-Recognition-using-yolo-V4

A comprehensive list of custom functions for YOLOv4, YOLOv4-tiny, YOLOv3, and YOLOv3-less used in TensorFlow, TFLite and TensorRT.

EXERCISE: This repository is very similar to my repository: tensorflow-yolov4-tflite. I created this repository to test custom coding functions that will be used with YOLOv4, and may make the application very difficult and slow down in terms of time complexity. So if you want to use the best YOLOv4 code with TensorFlow than move on to my other final site. This is a test of cool customization and apps that can be created using YOLOv4!

This model is trained on Korean Number plates.

weights:
https://drive.google.com/file/d/1RPzuUCOq6h1iswFNace0D1msF54xCuu1/view?usp=sharing

Results:
https://drive.google.com/file/d/1YUv6IQvpM8FVsEij1RfmzjX8Zl4X7YT0/view?usp=sharing


![](https://github.com/TalhaaaYaqoob/Korean-Number-Plate-Recognition-using-yolo-V4/blob/main/detections/crop/ezgif.com-gif-maker.gif)


## How to Run

<pre>
# Tensorflow CPU
conda env create -f conda-cpu.yml <br/>
conda activate yolov4-cpu

# Tensorflow GPU
conda env create -f conda-gpu.yml <br/>
conda activate yolov4-gpu
</pre>

## Pip

<pre>
# TensorFlow CPU
pip install -r requirements.txt

# TensorFlow GPU
pip install -r requirements-gpu.txt

</pre>


# Convert darknet weights to tensorflow

<pre>

## yolov4
python save_model.py --weights ./data/yolov4.weights --output ./checkpoints/yolov4-416 --input_size 416 --model yolov4 

# Run yolov4 tensorflow model
python detect.py --weights ./checkpoints/yolov4-416 --size 416 --model yolov4 --images ./data/images/kite.jpg

# Run yolov4 on video
python detect_video.py --weights ./checkpoints/yolov4-416 --size 416 --model yolov4 --video ./data/video/video.mp4 --output ./detections/results.avi

# Run yolov4 on webcam
python detect_video.py --weights ./checkpoints/yolov4-416 --size 416 --model yolov4 --video 0 --output ./detections/results.avi

</pre>
