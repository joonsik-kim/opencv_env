# OpenCV 2개월 마스터 코스 — 제조 검사 특화

제조업 비전검사 포지션 이직을 위한 OpenCV 실무 학습 기록

## 커리큘럼 (8주)

| 주차 | 주제 | 폴더 | 상태 |
|------|------|------|------|
| 1 | 이미지 기초 체력 | W1_image_basics/ | 🔄 |
| 2 | 노이즈 제거와 강조 | W2_filtering/ | 🔲 |
| 3 | 결함 영역 분리 (세그멘테이션) | W3_segmentation/ | 🔲 |
| 4 | 결함 검출 + 측정 | W4_contour_edge/ | 🔲 |
| 5 | 기하학적 변환 + 정렬 | W5_geometric_transform/ | 🔲 |
| 6 | 특징점 매칭 + 차이 검출 | W6_feature_matching/ | 🔲 |
| 7 | 비디오 + 실시간 처리 | W7_video_processing/ | 🔲 |
| 8 | 최종 프로젝트 | W8_final_project/ | 🔲 |

## 포트폴리오 산출물

| # | 프로젝트 | 완성 시점 |
|---|---------|----------|
| 1 | NEU 결함 자동 검출 + 정량화 | Week 4 |
| 2 | 참조 비교 결함 검사 시스템 | Week 6 |
| 3 | 실시간 결함 판정 시뮬레이션 | Week 7 |
| 4 | 최종 통합 검사 시스템 (Kaggle 공개) | Week 8 |

## 데이터셋
- NEU Steel Surface Defect (6종 결함, 1440장)
- Casting Product Quality (OK/NG 이진 분류)
- MVTec AD (정상 vs 불량 참조 비교)

## 기술 스택
- Python 3.13, OpenCV 4.12, NumPy, Matplotlib
- Jupyter Notebook
- 바이브 코딩 (Claude Code)

## 다른 컴퓨터에서 시작하기
```bash
git clone https://github.com/joonsik-kim/opencv_env.git
cd opencv_env
python -m venv .
Scripts/activate          # Windows
pip install -r requirements.txt
```
그 후 Kaggle에서 NEU Steel Surface Defect 데이터셋 다운로드 → `data/kaggle/archive/NEU-DET/`에 압축 해제

## 폴더 구조
```
W1_image_basics/         # Week 1: 이미지 기초
W2_filtering/            # Week 2: 필터링
W3_segmentation/         # Week 3: 세그멘테이션
W4_contour_edge/         # Week 4: 컨투어 + 미니 프로젝트 1
W5_geometric_transform/  # Week 5: 기하학적 변환
W6_feature_matching/     # Week 6: 특징점 매칭 + 미니 프로젝트 2
W7_video_processing/     # Week 7: 비디오 처리
W8_final_project/        # Week 8: 최종 프로젝트
data/                    # 데이터 (.gitignore로 제외)
CURRICULUM.md            # 상세 커리큘럼
```
