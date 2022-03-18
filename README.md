# python-program

# 마우스의 좌표를 출력하는 코드 만들기
```
-라이브러리 설치
pip install pyautogui
pip install pyperclip
pip install schedule

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

# python
```
schedule
- 명령어가 직관적으로 알아볼 수 있어서 사용에 용이
- 설정이 복잡해질 경우 사용여부를 고려

apscheduler
- Cron 방식 - Cron 표현식으로 수행
- Date 방식 - 특정 날짜에 수행
- Interval 방식 - 일정 주기로 수행
```
# 웹페이지 자동화 
``` PYTHON
import pyautogui
import time
import pyperclip

pyautogui.moveTo(1110, 50,0,2)
pyautogui.click()
time.sleep(0.5)

pyperclip.copy("roblox.com")
pyautogui.hotkey("ctrl", "v")
time.sleep(0.5)

pyautogui.write(["enter"])
time.sleep(1)
```
# 자동 캡쳐 후 저장
``` PYTHON
import pyautogui
import time
import pyperclip

pyautogui.moveTo(1241, 206, 0, 2)
pyautogui.click()
time.sleep(0.5)

pyperclip.copy("인천 날씨")
pyautogui.hotkey("ctrl", "v")
time.sleep(0.5)

pyautogui.write(["enter"])
time.sleep(1)

start_x = 992
start_y = 220
end_x = 1656
end_y = 635

pyautogui.screenshot('인천날씨.png', region=(start_x, start_y, end_x-start_x, end_y-start_y))
```

## 로블록스 앱 들어가는 방법
``` PYTHON
import pyautogui
import time
import pyperclip

pyautogui.hotkey("alt", "tab")

pyautogui.moveTo(1110, 50, 0, 2)
pyautogui.click()
time.sleep(0.5)

pyautogui.write("roblox.com")
time.sleep(0.5)

pyautogui.write(["enter"])
time.sleep(1)

pyautogui.moveTo(1755, 112)
time.sleep(5)
pyautogui.click()

pyautogui.moveTo(1314, 281)
time.sleep(1)
pyautogui.click()
pyautogui.write("triger1225")
time.sleep(0.3)
pyautogui.write(["enter"])

pyautogui.moveTo(1297, 336)
pyautogui.click()
time.sleep(5)
pyautogui.write("qkrtlgn@1225")
time.sleep(1)
pyautogui.write(["enter"])

pyautogui.moveTo(1689, 96)
pyautogui.click()
time.sleep(5)
pyautogui.click()
***** 완벽아님 주의 *****
```

## 자동화 날씨 프로그램
``` PYTHON
import pyautogui 
import time 
import pyperclip 

날씨 = [" 인천 날씨 ", "울산 날씨", "일산 날씨", " 부산 날씨", " 제주도 날씨"]

pyautogui.hotkey("alt", "tab")
addr_x = 1145
addr_y = 53
start_x = 992
start_y = 220
end_x = 1656
end_y = 635

for 지역날씨 in 날씨:
    pyautogui.moveTo(addr_x, addr_y, 1)
    time.sleep(0.5)
    pyautogui.click()
    time.sleep(0.5)
    pyautogui.write(" www.naver.com", interval=0.1)
    pyautogui.write(["enter"])
    time.sleep(1)

    pyperclip.copy(지역날씨)
    pyautogui.hotkey("ctrl", "v")
    time.sleep(0.5)
    pyautogui.write(["enter"])
    time.sleep(1)
    save = 지역날씨 + '.png'
    pyautogui.screenshot(save, region=(start_x, start_y, end_x-start_x, end_y-start_y))

* save = "weather\\" + 지역날씨 + '.png'
weather이라는 파일을 만들면 거기로 사진을 저장한다.
```

## 사진의 좌표를 알려주는 코드
``` PYTHON
import pyautogui

picPosition = pyautogui.locateOnScreen("testtest\picture.png")
print(picPosition)

if picPosition is None:
    picPosition = pyautogui.locateOnScreen("testtest\picture1.png")
    print(picPosition)

if picPosition is None:
    picPosition = pyautogui.locateOnScreen("testtest\picture2.png")
    print(picPosition)
```

## youtube검색 및 사진 캡쳐후 저장
``` PYTHON

