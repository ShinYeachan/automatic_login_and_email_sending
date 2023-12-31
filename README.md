## 네이버 아이디로 로그인 후, 엑셀에서 메일 정보를 가져와 메일을 보내는 자동화 스크립트

### 개요

이 스크립트는 새로운 네이버 아이디로 로그인하여, 주어진 엑셀 파일(`email_list.xlsx`)에서 메일 주소, 제목, 내용을 추출한 후, 해당 내용으로 메일을 자동으로 보내는 작업을 수행합니다.

## **시작하기 전에**

## ** 설치 및 환경 설정**

### 사용된 라이브러리

- **Selenium**: 웹 브라우저 자동화
```
pip install selenium
```
- **PyAutoGUI**: GUI 자동화
```
pip install PyAutoGUI
```
- **Pyperclip**: 클립보드 사용
```
pip install pyperclip
```
- **Openpyxl**: Excel 파일 작업
```
pip install openpyxl
```

### ** 기타 필요한 파이썬 패키지들 설치**

    
    pip install -r requirements.txt
    

<details>

| 라이브러리               | 설명                                                                            |
|---------------------|-------------------------------------------------------------------------------|
| chromedrivermanager | 도구로써, 웹 브라우저를 자동화하기 위해 필요한 ChromeDriver의 설치와 관리를 담당합니다.                       |
| ipython             | 대화형 Python 쉘로써, 코드 실행, 디버깅, 테스팅에 용이합니다. Jupyter notebook에서의 커널로도 사용됩니다.       |
| PyAutoGUI           | 그래픽 사용자 인터페이스(GUI) 자동화를 위한 Python 모듈로, 마우스와 키보드 명령을 프로그래밍 방식으로 제어할 수 있게 해줍니다. |
| setuptools          | Python 패키지의 빌드, 배포를 도와주는 도구입니다. `pip`를 통해 패키지를 설치할 때 기본적으로 사용됩니다.             |
| wheel               | Python 배포 패키지를 위한 바이너리 패키지 형식입니다. `pip`를 통해 패키지를 빠르게 설치할 수 있게 도와줍니다.          |
| jupyter             | 웹 기반의 대화형 계산 환경을 제공하는 프로젝트로, Jupyter notebook, JupyterLab 등의 애플리케이션을 포함합니다.   |

</details>

### 코드 구조 설명

1. **네이버 로그인**:
    - 브라우저를 최대화하고 네이버 로그인 페이지로 이동
    - 아이디와 비밀번호를 입력 후 로그인 버튼 클릭

2. **엑셀 파일에서 메일 정보 읽기**:
    - `sample_email_list.xlsx`에서 메일 주소, 제목, 내용을 순차적으로 추출

3. **메일 보내기**:
    - 메일 작성 페이지로 이동
    - 메일 주소, 제목, 내용을 입력
    - 메일 보내기

- **네이버 로그인**:버튼 클릭
    - 봇 탐지를 피하기 위한 20초의 대기 시간

### 사용법

1. **주피터 노트북 설치**:
    - 아래 영상을 참고해서 Visual Studio Code에 Jypyter Notebook을 설치해줍니다.
    - https://www.youtube.com/watch?v=1tKPqQmXM98&t=78s 

2. **네이버 아이디 설정**:
    - 21번째, 28번째 줄에 있는 pyperclip.copy("sample_id"), pyperclip.copy("sample_pw")에서
        sample_id, sample_pw를 사용할 네이버 아이디로 변경합니다

3. **엑셀 파일에서 샘플 이메일들을 변경**:
    - `sample_email_list.xlsx`에서 첫번째 컬럼에 있는 샘플 이메일들을 원하는 이메일로 변경합니다.

# 에러 해결 방법: 화면이 갑자기 꺼지거나 네이버 캡챠때문에 더 진행이 안 될 경우

## 해결 방법:

### 1. 주피터 노트북 설치 후 코드 실행

### 2. 새로운 네이버 아이디를 만든 후 코드 실행


