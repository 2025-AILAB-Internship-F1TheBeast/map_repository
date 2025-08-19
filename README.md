아래와 같이 map_repository 폴더의 구조와 용도, 각 파일의 의미를 설명하는 README 예시를 작성할 수 있습니다.

---

# map_repository

F1TENTH 및 자율주행 경진대회용 다양한 트랙 맵과 최적화 레이싱 라인 데이터를 관리하는 저장소입니다.

## 폴더 구조

각 트랙별로 하나의 폴더가 존재하며, 폴더 내부에는 다음과 같은 파일들이 포함됩니다:

```
map_repository/
├── BrandsHatch/
│   ├── BrandsHatch_map.png         # 트랙 맵 이미지 (occupancy grid)
│   ├── BrandsHatch_map.yaml        # ROS용 맵 메타데이터 (origin, resolution 등)
│   └── BrandsHatch_race.csv        # 최적화된 레이싱 라인 및 속도 프로파일
├── Oschersleben_map/
│   ├── Oschersleben_map.png
│   ├── Oschersleben_map.yaml
│   └── Oscherslegen_map_race.csv
├── icra_2_clean/
│   ├── icra_2_clean.png
│   ├── icra_2_clean.yaml
│   └── icra_2_clean_race.csv
├── soobmap1/
│   ├── slam_map1.png
│   ├── slam_map1.yaml
│   └── slam_map1_race.csv
├── soobmap2/
│   ├── slam_map2.png
│   ├── slam_map2.yaml
│   ├── slam_map2_race.csv
│   └── slam_map2_mid.csv
```

## 파일 설명

- **\*_map.png**: 트랙의 occupancy grid 맵 이미지 (ROS navigation, SLAM 등에서 사용)
- **\*_map.yaml**: 맵 이미지의 메타데이터 (해상도, origin, threshold 등)
- **\*_race.csv**: [s, x, y, v, width_left, width_right] 형식의 최적화된 레이싱 라인 및 속도 프로파일
- **\*_mid.csv**: (선택) 중간 결과 또는 추가 경로 정보

## 활용 예시

- ROS navigation, SLAM, 경로 추종(pure pursuit) 등에서 맵 및 레이싱 라인 데이터로 활용
- 시뮬레이터 및 실제 차량 실험에서 동일한 맵/경로 재현 가능

## 기여 방법

1. 새로운 트랙을 추가할 때는 동일한 구조로 폴더를 생성하고, png/yaml/csv 파일을 추가해주세요.
2. 파일명은 트랙명과 일치시키는 것을 권장합니다.

---
