# OpenCV 2개월 마스터 코스 — 제조 검사 특화

## 개요
- 기간: 8주 (주 14시간: 평일 2h + 토요일 4h)
- 방식: 바이브 코딩 — Claude Code가 코드 작성, 학습자는 결과 분석·판단·메모
- 최종 산출물: 포트폴리오 프로젝트 4개 + Kaggle 공개 노트북
- 목표 함수: 약 60개

## 데이터셋
| 데이터셋 | 용도 |
|----------|------|
| NEU Steel Surface Defect | 6종 결함, 기초~심화 전 과정 |
| Casting Product Quality | OK/NG 이진 분류, 정상-불량 비교 |
| MVTec AD (무료 샘플) | 정상 vs 불량 참조 비교, template/feature matching |

---

### Week 1: 이미지 기초 체력 (W1_image_basics/)
| 날 | 파일명 | 주제 | 함수 |
|----|--------|------|------|
| D1 | W1D1_image_loading.ipynb | 로딩·저장·표시 | imread, imwrite, shape |
| D2 | W1D2_colorspace_roi.ipynb | 색공간 + ROI | cvtColor, ROI slicing, resize |
| D3 | W1D3_histogram.ipynb | 히스토그램 | calcHist |
| D4 | W1D4_contrast.ipynb | 밝기·대비 | equalizeHist, createCLAHE |
| D5 | W1D5_arithmetic.ipynb | 이미지 연산 | absdiff, addWeighted, bitwise |
| Sat | W1_summary.ipynb | 종합 | 전체 복습 |

### Week 2: 노이즈 제거와 강조 (W2_filtering/)
| 날 | 파일명 | 주제 | 함수 |
|----|--------|------|------|
| D1 | W2D1_blur_compare.ipynb | blur 비교 | GaussianBlur, medianBlur, bilateralFilter |
| D2 | W2D2_blur_defect_types.ipynb | 결함별 blur | 동일 + 비교 분석 |
| D3 | W2D3_custom_filter.ipynb | 커스텀 필터 | filter2D |
| D4 | W2D4_noise.ipynb | 노이즈 추가·제거 | randn, PSNR |
| D5 | W2D5_optimal_blur.ipynb | 최적 blur 탐색 | 전체 조합 |
| Sat | W2_summary.ipynb | 종합 | 파이프라인화 |

### Week 3: 결함 영역 분리 (W3_segmentation/)
| 날 | 파일명 | 주제 | 함수 |
|----|--------|------|------|
| D1 | W3D1_threshold_basic.ipynb | Otsu threshold | threshold(OTSU) |
| D2 | W3D2_threshold_adaptive.ipynb | adaptive threshold | adaptiveThreshold |
| D3 | W3D3_morphology_basic.ipynb | morphology 기초 | erode, dilate, morphologyEx(OPEN,CLOSE) |
| D4 | W3D4_morphology_advanced.ipynb | morphology 심화 | GRADIENT, TOPHAT, BLACKHAT |
| D5 | W3D5_hsv_masking.ipynb | 색공간 마스킹 | cvtColor(HSV), inRange, split, merge |
| Sat | W3_summary.ipynb | 종합 | 전체 조합 최적화 |

### Week 4: 결함 검출 + 측정 (W4_contour_edge/)
| 날 | 파일명 | 주제 | 함수 |
|----|--------|------|------|
| D1 | W4D1_contour_basic.ipynb | contour 기초 | findContours, drawContours |
| D2 | W4D2_contour_measure.ipynb | contour 측정 | contourArea, arcLength, moments |
| D3 | W4D3_bounding.ipynb | bounding 도형 | boundingRect, minAreaRect, minEnclosingCircle |
| D4 | W4D4_edge_detection.ipynb | edge detection | Canny, Sobel, Scharr, Laplacian |
| D5 | W4D5_drawing_label.ipynb | 드로잉·라벨링 | rectangle, putText, circle, line |
| Sat | **W4_mini_project_1.ipynb** | **미니 프로젝트 1** | 전체 파이프라인 → CSV |

### Week 5: 기하학적 변환 (W5_geometric_transform/)
| 날 | 파일명 | 주제 | 함수 |
|----|--------|------|------|
| D1 | W5D1_rotation_flip.ipynb | 회전·반전 | getRotationMatrix2D, warpAffine, flip |
| D2 | W5D2_perspective.ipynb | perspective 변환 | getPerspectiveTransform, warpPerspective |
| D3 | W5D3_scale_crop.ipynb | 스케일 + 크롭 | resize(INTER_LINEAR/CUBIC/AREA) |
| D4 | W5D4_alignment.ipynb | 이미지 정합 | warpAffine + translation |
| D5 | W5D5_pixel_to_mm.ipynb | 픽셀↔실측 변환 | 비율 계산 |
| Sat | W5_summary.ipynb | 종합 | W4+5 통합 |

### Week 6: 특징점 매칭 (W6_feature_matching/)
| 날 | 파일명 | 주제 | 함수 |
|----|--------|------|------|
| D1 | W6D1_feature_extract.ipynb | 특징점 추출 | ORB_create, detectAndCompute |
| D2 | W6D2_matching.ipynb | 매칭 | BFMatcher, knnMatch, drawMatches |
| D3 | W6D3_homography.ipynb | homography 정렬 | findHomography, warpPerspective |
| D4 | W6D4_diff_detect.ipynb | 차이 기반 검출 | absdiff + W3 파이프라인 |
| D5 | W6D5_template.ipynb | template matching | matchTemplate, minMaxLoc |
| Sat | **W6_mini_project_2.ipynb** | **미니 프로젝트 2** | 참조 비교 검사 시스템 |

### Week 7: 비디오 처리 (W7_video_processing/)
| 날 | 파일명 | 주제 | 함수 |
|----|--------|------|------|
| D1 | W7D1_video_io.ipynb | 비디오 읽기·쓰기 | VideoCapture, read, VideoWriter |
| D2 | W7D2_frame_process.ipynb | 프레임별 처리 | 반복문 + W3 함수 |
| D3 | W7D3_motion_detect.ipynb | 움직임 감지 | absdiff + 프레임 비교 |
| D4 | W7D4_realtime_sim.ipynb | 실시간 검사 시뮬레이션 | waitKey, 루프, 판정 로직 |
| D5 | W7D5_connected.ipynb | 연결 요소 분석 | connectedComponents, connectedComponentsWithStats |
| Sat | **W7_summary.ipynb** | **포트폴리오 3** | 실시간 결함 판정 시뮬레이션 |

### Week 8: 최종 프로젝트 (W8_final_project/)
| 날 | 파일명 | 할 것 |
|----|--------|------|
| D1 | W8D1_design.md | 전체 파이프라인 구조도 |
| D2 | W8D2_implement.ipynb | NEU 6종 자동 검출+판정 구현 |
| D3 | W8D3_tuning.ipynb | 파라미터 튜닝 + 검출률 계산 |
| D4 | W8D4_analysis.md | 결과 분석 + 개선 방향 |
| D5 | W8D5_document.md | 프로젝트 문서화 |
| Sat | W8_final.ipynb | Kaggle 공개용 노트북 |

## 전체 함수 목록 (약 60개)
imread, imwrite, cvtColor, resize, flip, calcHist, equalizeHist, createCLAHE,
GaussianBlur, medianBlur, bilateralFilter, filter2D,
threshold, adaptiveThreshold,
erode, dilate, morphologyEx, getStructuringElement,
Canny, Sobel, Scharr, Laplacian,
findContours, drawContours, contourArea, arcLength, moments, boundingRect, minAreaRect, minEnclosingCircle, approxPolyDP,
connectedComponents, connectedComponentsWithStats,
warpAffine, warpPerspective, getRotationMatrix2D, getPerspectiveTransform,
ORB_create, detectAndCompute, drawKeypoints, BFMatcher, knnMatch, drawMatches, findHomography,
matchTemplate, minMaxLoc,
absdiff, addWeighted, bitwise_and, bitwise_or, bitwise_not,
rectangle, circle, line, putText,
VideoCapture, read, VideoWriter, waitKey,
inRange, split, merge, HoughLines, HoughCircles
