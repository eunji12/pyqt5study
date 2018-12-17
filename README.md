# PyQt5 시작하기
``` memo
2018.12.16 ~
매일 조금씩 하는 pyqt5
```
[PyQt5 tutorial 2018: Create a GUI with Python and Qt](https://build-system.fman.io/pyqt5-tutorial)

```shell
  535  conda create -n qtstudy2 python=3.5
  537  conda env list
  539  conda activate qtstudy2
  540  ls
  541  python3 --version
  542  pip install PyQt5==5.9.2
```

- conda로 pyQt 실습용 가상환경 생성
- python3.6에서 pyqt5설치 시 지원 버전 등 문제가 있어 python 3.5, pyqt5 5.9.2(기타오류가없는버전;사이트가이드)로 버전 지정하여 설치
- 생성한 가상환경에 PyQt5 설치 후  파이참에 연동하여 소스 작업
- 간단한 위젯 띄우기 실습
```python
from PyQt5.QtWidgets import QApplication, QLabel
app = QApplication([])
label = QLabel('Hello World!')
label.show()
app.exec_()
```
- 응용하여 프로그램 작성 예정
- QApplication([]) : GUI 인스턴스 생성, 필수 요구 사항 
- [] 명령행 매개변수 위치
- label생성 및 show
- app.exec_() 어플리케이션에 실행 권한 위임

* 기타
``` pycharm 단축키
mac os 파이참 단축키
shift+control+R 실행
```
