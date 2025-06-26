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










