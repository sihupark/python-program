# python-program

# 마우스의 좌표를 출력하는 코드 만들기
```
-라이브러리 설치
pip install pyautogui
pip install pyperclip

import pyautogui
import time

while True:
    print(pyautogui.position())
    time.sleep(0.1)
```
# 오토마우스 라이브러리 기능(pyautogui)
```
pyautogui.position()
마우스의 좌표를 입력 받습니다.

pyautogui.moveTo(x, y)
x, y의 좌표로 이동합니다. 절대 좌표입니다.
pyautogui.moveTo(x, y, 시간)
x, y의 좌표로 지정된 시간동안 이동합니다. 절대 좌표입니다.

pyautogui.moveRell(,x,y)
현재 마우스 위치로부터 x,y 픽셀만큼 이동입니다.

pyautogui.click()
현재 마우스 커서 위치에 마우스를 클릭합니다.

pyautogui.doubleClick()
현재 마우스 커서 위치에 마우스를 더블클릭합니다.

pyautogui.click((50, 50))
50, 50의 위치에 마우스를 클릭합니다.

pyautogui.click(x=50, y=50)
x=50, y=50의 위치에 마우스를 클릭합니다.

pyautogui.rightClick()
현재 마우스 커서 위치에 마우스를 우클릭합니다.

pyautogui.dragTo(x=50, y=50, duration=2)
현재 마우스 위치부터 50, 50 좌표까지 2초 동안 드래그합니다.

pyautogui.typewrite("ABC")
ABC를 입력합니다.한글은 지원되지 않습니다. 한글은 pyperclip 라이브러리를 이용하여 붙여넣기를 통해 입력합니다.

pyautogui.typewrite("ABC", interval=1)
1초 동안 ABC를 입력합니다.

pyautogui.hotkey("ctrl", "v")
hotkey를 이용하여 두 개의 키를 동시에 누를 수 있습니다. [Ctrl + V]를 입력합니다.

pyautogui.screenshot('저장경로', region=(100, 100, 50,50))
screenshot을 이용하여 부분 캡쳐를 할 수 있습니다. region=(x좌표, y좌표, 가로 사이즈, 세로 사이즈)입니다.
```
