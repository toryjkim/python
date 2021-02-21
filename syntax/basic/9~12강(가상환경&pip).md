# 가상환경
가상환경이 필요한 이유: 수행하는 프로젝트마다 필요한 Python의 버전과 패키지가 다르다. 따라서
필요한 Python 버전과 패키지만을 고유의 공간에 설치하면 효율적으로 프로젝트를 관리할 수 있는데
이런 역할을 제공하는 것이 가상환경이다.

## 명령어 (윈도우: sciprts, 맥: bin)
python -m venv 경로 : 경로에 가상환경을 설치한다.
scripts\activate.bin : 가상환경을 실행한다.
scripts\deactivate.bin : 가상환경을 해제한다.


# pip (pip install packages) - 패키지 관리자
## 주요 명령어
1. pip install 패키지 : 패키지를 설치한다.
2. pip list : 설치된 패키지 목록을 조회한다.
3. pip search 패키지 : 현재 pip 버전에 설치하고자 하는 패키지가 존재하는지 확인한다.
4. pip install --upgrade 패키지  : 설치된 패키지를 업데이트한다.
5. pip show 패키지 : 패키지에 대한 정보를 보여준다.
6. pip uninstall 패키지 : 패키지를 삭제한다.
