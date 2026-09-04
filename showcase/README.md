# 🧪 통합 Showcase

MNIST 손글씨 이미지 분류 앱과 서울시 자전거 대여량 회귀 앱을 하나의 Streamlit 앱으로 통합한 프로젝트입니다.

기존 앱을 복사하지 않고 Showcase에서 그대로 불러와 실행합니다.

## 📁 폴더 구조

```text
showcase/
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

## 🔗 연결 구조

```text
showcase/Home.py
├── pages/1_분류_MNIST.py
│   └── 과제_Streamlit_앱_분류/app.py
│       └── 과제_Streamlit_앱_분류/mnist_cnn.pt
└── pages/2_회귀_자전거.py
    └── 과제_Streamlit_앱_회귀/app_bike.py
        └── 과제_Streamlit_앱_회귀/bike_reg.pt
```

## 🚀 실행 방법

프로젝트 최상위 폴더에서 실행합니다.

```bash
pip install -r requirements.txt
streamlit run showcase/Home.py
```

## 🖼️ 분류 페이지

MNIST 손글씨 이미지를 입력하면 CNN 모델이 숫자 0부터 9까지 중 하나를 예측합니다.

관련 파일:

```text
과제_Streamlit_앱_분류/app.py
과제_Streamlit_앱_분류/mnist_cnn.pt
```

## 🚲 회귀 페이지

시간과 날씨 데이터를 입력하면 MLP 모델이 서울시 자전거 대여량을 예측합니다.

관련 파일:

```text
과제_Streamlit_앱_회귀/app_bike.py
과제_Streamlit_앱_회귀/bike_reg.pt
```

## ✏️ 프로필 수정

Showcase 첫 화면의 이름과 프로젝트 설명은 다음 파일에서 수정할 수 있습니다.

```text
showcase/profile.py
```

## ☁️ Streamlit 배포

Streamlit Community Cloud에서 다음 파일을 메인 실행 파일로 설정합니다.

```text
showcase/Home.py
```

배포 시 다음 항목이 저장소에 포함되어 있어야 합니다.

```text
requirements.txt
showcase/
과제_Streamlit_앱_분류/
과제_Streamlit_앱_회귀/
```