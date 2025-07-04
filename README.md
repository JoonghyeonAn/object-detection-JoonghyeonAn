 0. YOLOv5 설치
# 모델 다운로드
!git clone https://github.com/ultralytics/yolov5.git
%cd yolov5
!pip install -r requirements.txt

# 사전 학습된 파라미터 다운로드
!wget https://github.com/ultralytics/yolov5/releases/download/v7.0/yolov5s.pt

1. 라이브러리 import

import cv2
import matplotlib.pyplot as plt
from ultralytics import YOLO
import numpy as np
from google.colab import files
import io
from PIL import Image
import torch

device = '0' if torch.cuda.is_available() else 'cpu'

2. 이미지 업로드
from google.colab import files
uploaded = files.upload()

3. YOLO 모델 로드

detect: weights=['yolov5s.pt'], source=car image.jpg, data=data/coco128.yaml, imgsz=[640, 640], conf_thres=0.25, iou_thres=0.45, max_det=1000, device=cpu, view_img=False, save_txt=False, save_format=0, save_csv=False, save_conf=False, save_crop=False, nosave=False, classes=None, agnostic_nms=False, augment=False, visualize=False, update=False, project=runs/detect, name=exp, exist_ok=False, line_thickness=3, hide_labels=False, hide_conf=False, half=False, dnn=False, vid_stride=1
YOLOv5 🚀 v7.0-421-g79c4c31d Python-3.11.13 torch-2.6.0+cu124 CPU

Fusing layers... 
YOLOv5s summary: 213 layers, 7225885 parameters, 0 gradients, 16.4 GFLOPs
image 1/1 /content/yolov5/car image.jpg: 480x640 2 cars, 263.5ms
Speed: 2.1ms pre-process, 263.5ms inference, 50.4ms NMS per image at shape (1, 3, 640, 640)
Results saved to runs/detect/exp

4. 추론 실행

from IPython.display import Image
Image(filename='runs/detect/exp/car image.jpg')

5. 결과 시각화
from google.colab import files
files.download('runs/detect/exp/car image.jpg')


# object-detection-JoonghyeonAn
## 📸 개요
직접 촬영한 사진에 대해 YOLOv5 모델을 활용하여 객체 감지를 수행하였습니다.  
Google Colab에서 실행되었으며, 결과 이미지를 아래에 첨부합니다.

---

## 🔧 실행 환경
- Google Colab
- Ultralytics YOLOv5 (PyTorch 기반)
- CPU 모드

---


---

## 🟦 결과 이미지 (Bounding Box 적용)

![결과](result_car_image.jpg)

---

## ▶️ 실행 명령어 (Colab)

```bash
!git clone https://github.com/ultralytics/yolov5
%cd yolov5
!pip install -r requirements.txt
!python detect.py --weights yolov5s.pt --img 640 --conf 0.25 --source "car image.jpg" --device cpu
🔗 참고 오픈소스
YOLOv5 GitHub



---

##최종 URL 제출


https://github.com/JoonghyeonAn/object-detection-JoonghyeonAn










