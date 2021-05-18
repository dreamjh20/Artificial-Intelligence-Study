```python
import pyautogui as pg
import time
import schedule
```


```python
def check():
    pg.moveTo(1000, 350, 1)
    pg.click(clicks = 2, interval = 0.1)
    pg.moveTo(650, 600, 1)
    pg.click(clicks = 2, interval = 1)
    pg.moveTo(87, 680)
    pg.click(clicks = 1)
    pg.moveTo(87, 820)
    pg.click(clicks = 1)
    pg.moveTo(87, 1010)
    pg.click(clicks = 1)
    pg.scroll(-50)
    pg.click(clicks = 1)
    pg.moveTo(950, 25)
    pg.click(clicks = 1)
```


```python
#if 시간 되면
schedule.every().day.at("08:10:29").do(check)

while True:
    schedule.run_pending()
    time.sleep(1)
```
