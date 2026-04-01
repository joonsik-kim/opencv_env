# OpenCV + Deep Learning for Manufacturing Vision

제조업 비전검사 (PCB AOI → 스마트팩토리/2차전지/반도체) 학습 기록

## 커리큘럼 (14주)

| 주차 | 주제 | 상태 |
|------|------|------|
| 1-2 | OpenCV 핵심 (전처리, 윤곽선) | 🔲 |
| 3-4 | 계측 & 이미지 정렬 | 🔲 |
| 5 | 데이터 라벨링 | 🔲 |
| 6-8 | YOLO 결함 검출 | 🔲 |
| 9-10 | 분류 & 세그멘테이션 | 🔲 |
| 11-12 | 파이프라인 & 시스템 설계 | 🔲 |
| 13-14 | 포트폴리오 마무리 | 🔲 |

## 프로젝트

### 1. PCB AOI 자동 검사 시스템
OpenCV 전처리 + YOLO 결함 검출 파이프라인

### 2. 캐글 범용 결함 검출
Steel Defect / MVTec AD / Wafer Map 등 다양한 도메인

## 기술 스택
- Python 3.13, OpenCV, NumPy, Matplotlib
- Ultralytics YOLO (YOLOv8 / YOLO11)
- Roboflow (라벨링)
- Streamlit (대시보드)

## 폴더 구조
```
week01_opencv_basics/    # 주차별 학습 노트북
week03_measurement/
week06_yolo/
projects/                # 최종 프로젝트
data/                    # 데이터 (이미지는 .gitignore로 제외)
learning_log.md          # 매일 학습 기록
```
