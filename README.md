# 🧩 Mini Project

PyTorch로 학습한 딥러닝 모델을 Streamlit 웹 앱으로 구현한 미니프로젝트입니다.

MNIST 손글씨 이미지 분류와 서울시 자전거 대여량 회귀 예측 앱을 각각 구현했으며, 두 앱을 하나의 Showcase로 통합했습니다.

## 📌 프로젝트 구성

| 프로젝트 | 유형 | 모델 | 실행 파일 |
|---|---|---|---|
| MNIST 손글씨 분류 | 분류 | CNN | `과제_Streamlit_앱_분류/app.py` |
| 서울시 자전거 수요 예측 | 회귀 | MLP | `과제_Streamlit_앱_회귀/app_bike.py` |
| 통합 Showcase | 분류 + 회귀 | 두 프로젝트 통합 | `showcase/Home.py` |

## 📁 폴더 구조

```text
Miniproject/
├── app.py
├── mnist_cnn.pt
├── requirements.txt
├── README.md
├── AGENTS.md
├── .gitignore
│
├── 과제_Streamlit_앱_분류/
│   ├── app.py
│   ├── mnist_cnn.pt
│   ├── requirements.txt
│   └── .gitignore
│
├── 과제_Streamlit_앱_회귀/
│   ├── app_bike.py
│   ├── bike_reg.pt
│   ├── requirements.txt
│   └── .gitignore
│
└── showcase/
    ├── Home.py
    ├── profile.py
    ├── README.md
    ├── __init__.py
    ├── core/
    │   ├── loader.py
    │   ├── theme.py
    │   └── __init__.py
    └── pages/
        ├── 1_분류_MNIST.py
        └── 2_회귀_자전거.py
```

`__init__.py` 파일은 Python 패키지로 인식시키기 위한 파일이며, 별도 코드가 없어 빈 파일로 유지합니다.

## 🖼️ MNIST 손글씨 분류

손글씨 이미지를 입력하면 CNN 모델이 숫자 0부터 9까지 중 하나를 예측합니다.

- 이미지 입력 및 미리보기
- 28×28 크기 변환
- 숫자 분류 결과 출력
- 클래스별 예측 확률 확인

관련 파일:

```text
과제_Streamlit_앱_분류/app.py
과제_Streamlit_앱_분류/mnist_cnn.pt
```

## 🚲 서울시 자전거 수요 예측

시간과 날씨 데이터를 입력하면 MLP 모델이 시간당 자전거 대여량을 예측합니다.

- 시간 및 날씨 데이터 입력
- 입력 데이터 표준화
- 시간당 대여량 예측
- 입력값에 따른 예측 결과 확인

관련 파일:

```text
과제_Streamlit_앱_회귀/app_bike.py
과제_Streamlit_앱_회귀/bike_reg.pt
```

## 🧪 통합 Showcase

`showcase/Home.py`를 실행하면 두 프로젝트를 하나의 Streamlit 앱에서 확인할 수 있습니다.

Showcase는 기존 분류 앱과 회귀 앱을 복사하지 않고 그대로 불러와 재사용합니다.

- `showcase/Home.py`: 첫 화면 및 프로젝트 소개
- `showcase/pages/1_분류_MNIST.py`: MNIST 분류 페이지
- `showcase/pages/2_회귀_자전거.py`: 자전거 수요 회귀 페이지
- `showcase/profile.py`: 첫 화면에 표시할 개인 설명
- `showcase/core/`: 앱 로딩 및 공통 테마 관리

자세한 Showcase 설명은 [`showcase/README.md`](./showcase/README.md)에서 확인할 수 있습니다.

## ⚙️ 설치

프로젝트 최상위 폴더에서 실행합니다.

```bash
pip install -r requirements.txt
```

## 🚀 실행 방법

### 통합 Showcase

```bash
streamlit run showcase/Home.py
```

### MNIST 분류 앱

```bash
streamlit run 과제_Streamlit_앱_분류/app.py
```

### 자전거 수요 회귀 앱

```bash
streamlit run 과제_Streamlit_앱_회귀/app_bike.py
```

### 루트 분류 앱

```bash
streamlit run app.py
```

## 🛠️ 사용 기술

- Python
- PyTorch
- CNN
- MLP
- Streamlit
- NumPy
- Pillow
- Git / GitHub

## 💡 학습 내용

- 분류와 회귀 문제의 차이
- CNN을 활용한 이미지 분류
- MLP를 활용한 수치 예측
- 데이터 전처리와 표준화
- PyTorch 모델 저장 및 불러오기
- Streamlit 웹 앱 구현
- 여러 프로젝트를 하나의 Showcase로 통합

## 👤 Developer

**하주성**

GitHub: [leeony2636](https://github.com/leeony2636)