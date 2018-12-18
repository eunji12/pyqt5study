# PyQt5 배포하기
``` memo
2018.12.17 22:00 ~
매일 조금씩 하는 pyqt5 학습
실행파일 생성하기
```

[pyQt5 tutorial]([PyQt5 tutorial 2018: Create a GUI with Python and Qt](https://build-system.fman.io/pyqt5-tutorial))

- 간단한 위젯을 하나 띄운 후 이 앱을 아무대서나 열 수 있도록 실행 파일로 만든다
``` shell
1 pip install fbs PyInstaller==3.4
2 fbs startproject
3 fbs run
4 fbs freeze
```

— 1 : fbs설치  
— 2 : 컴파일용 프로젝트 생성(source/아래 main.py 생성 )  
— 3 : 앱 실행  
— 4 : 독립형 실행파일 생성  


- 내일은 위젯 생성 후 Signals / slots 실습하기
