# 프로젝트 작업 안내

## 프로젝트 소개

이 저장소는 PyTorch로 학습한 모델을 Streamlit 웹 앱으로 구현한 미니프로젝트입니다.

| 프로젝트 | 설명 | 실행 파일 |
| --- | --- | --- |
| MNIST 분류 | 손글씨 이미지를 숫자 0~9로 분류 | `과제_Streamlit_앱_분류/app.py` |
| 자전거 수요 회귀 | 서울시 자전거 대여량을 예측 | `과제_Streamlit_앱_회귀/app_bike.py` |
| 통합 Showcase | 두 프로젝트를 하나의 웹 앱으로 통합 | `showcase/Home.py` |

## 프로젝트 구조

- `과제_Streamlit_앱_분류/`
  - MNIST 이미지 분류 앱
  - `app.py`: Streamlit 앱
  - `mnist_cnn.pt`: 학습된 CNN 모델

- `과제_Streamlit_앱_회귀/`
  - 서울시 자전거 대여량 회귀 앱
  - `app_bike.py`: Streamlit 앱
  - `bike_reg.pt`: 학습된 회귀 모델

- `showcase/`
  - 통합 포트폴리오 앱
  - `Home.py`: 메인 화면
  - `pages/`: 분류·회귀 페이지
  - `core/`: 공통 로더 및 테마
  - `profile.py`: 포트폴리오에 표시할 개인 설명

- `requirements.txt`
  - 프로젝트 실행에 필요한 Python 패키지 목록

- `README.md`
  - 프로젝트 소개 및 실행 방법

## 실행 방법

### 1. 패키지 설치

프로젝트 루트에서 실행합니다.

```bash
pip install -r requirements.txt
```

### 2. 통합 Showcase 실행

두 프로젝트를 하나의 화면에서 실행합니다.

```bash
streamlit run showcase/Home.py
```

### 3. 분류 앱만 실행

```bash
cd 과제_Streamlit_앱_분류
streamlit run app.py
```

### 4. 회귀 앱만 실행

```bash
cd 과제_Streamlit_앱_회귀
streamlit run app_bike.py
```

## 수정 규칙

- 통합 앱의 메인 진입점은 `showcase/Home.py`입니다.
- 분류 기능은 `과제_Streamlit_앱_분류/app.py`에서 수정합니다.
- 회귀 기능은 `과제_Streamlit_앱_회귀/app_bike.py`에서 수정합니다.
- Showcase 페이지는 과제 폴더의 앱을 재사용하므로 동일한 기능을 중복 구현하지 않습니다.
- 기존 폴더 구조와 파일명은 특별한 이유가 없으면 변경하지 않습니다.
- 모델 구조를 수정할 때는 기존 `.pt` 체크포인트와의 호환성을 확인합니다.
- `.pt` 모델 파일은 확인 없이 삭제하거나 덮어쓰지 않습니다.
- 사용하지 않는 중복 파일이나 문서를 정리할 때는 README의 경로도 함께 확인합니다.
- 기능을 추가할 때는 기존 코드 스타일과 변수명을 우선적으로 따릅니다.

## 모델 파일 규칙

모델 파일은 학습된 가중치와 설정을 포함합니다.

- 분류 모델: `과제_Streamlit_앱_분류/mnist_cnn.pt`
- 회귀 모델: `과제_Streamlit_앱_회귀/bike_reg.pt`

모델을 다시 생성하거나 교체할 때는 다음 항목이 일치해야 합니다.

- 모델 구조
- 입력 데이터 형태
- 특성 순서
- 정규화 방식
- 체크포인트 저장 형식

## 문서 관리

- 프로젝트 전체 설명은 루트 `README.md`에서 관리합니다.
- Showcase 설명은 `showcase/README.md`에서 관리합니다.
- 실행 명령어가 변경되면 README의 실행 방법도 함께 수정합니다.
- 삭제한 파일이나 폴더가 README에 남아 있지 않은지 확인합니다.
- 오래된 배포 방법이나 실제 구조와 다른 설명은 수정합니다.

## 보안 및 파일 관리

저장소에 다음 정보를 추가하지 않습니다.

- API 키
- 비밀번호
- 개인 인증 정보
- `.env` 파일
- Streamlit secrets
- 개인적인 임시 파일

모델 파일과 프로젝트에 필요한 소스 파일만 저장소에서 관리합니다.

## 수정 후 확인 사항

변경 후 다음 항목을 확인합니다.

- 분류 앱이 정상적으로 실행되는지 확인합니다.
- 회귀 앱이 정상적으로 실행되는지 확인합니다.
- `showcase/Home.py`가 정상적으로 실행되는지 확인합니다.
- Showcase의 분류 페이지가 열리는지 확인합니다.
- Showcase의 회귀 페이지가 열리는지 확인합니다.
- 모델 파일 경로가 올바른지 확인합니다.
- README의 설명과 실제 프로젝트 구조가 일치하는지 확인합니다.
``` 