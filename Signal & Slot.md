# Signal & Slot
``` memo
2018.12.18 23:30 ~
매일 조금씩 하는 pyqt5 학습
Signal & Slot 이해하기
```

[pyQt5 tutorial]([PyQt5 tutorial 2018: Create a GUI with Python and Qt](https://build-system.fman.io/pyqt5-tutorial))

- 버튼 생성 후 click이벤트 발생시 액션 취하기
- button.clicked : 이벤트 발생 Signal
- connect 를 통해  Slot 연결
- Python에서는 모든 함수가 슬롯이다

```python
*"""*
*    Slot & signal 학습*
*    1. 버튼 생성*
*    2. 버튼 클릭시 메시지 창을 띄우는 함수 만들기*
*    3. 이벤트 연결*
*    4. 실행*
*"""*
from PyQt5.QtWidgets import *

app = QApplication([])
button = QPushButton('Click!') -- 버튼 생성


def on_button_click(): -- 이벤트 발생시 실행시킬 함수
    alert = QMessageBox()
    alert.setText('clicked')
    alert.exec_()


button.clicked.connect(on_button_click) 
-- clicked.connect를 통해 이벤트 연결
button.show()
app.exec_()

````


- 튜토리얼 원문
``` textile
Signals / slots
Qt uses a mechanism called signals to let you react to events such as the user clicking a button. The following example illustrates this. It contains a button that, when clicked, shows a message box:

from PyQt5.QtWidgets import *
app = QApplication([])
button = QPushButton('Click')
def on_button_clicked():
    alert = QMessageBox()
    alert.setText('You clicked the button!')
    alert.exec_()

button.clicked.connect(on_button_clicked)
button.show()
app.exec_()
PyQt QMessageBox saying that a button was clicked
The interesting line is highlighted above: button.clicked is a signal, .connect(...) lets us install a so-called slot on it. This is simply a function that gets called when the signal occurs. In the above example, our slot shows a message box.

The term slot is important when using Qt from C++, because slots must be declared in a special way in C++. In Python however, any function can be a slot – we saw this above. For this reason, the distinction between slots and "normal" functions has little relevance for us.

Signals are ubiquitous in Qt. And of course, you can also define your own. This however is beyond the scope of this tutorial.
```

