# WhatsAppBot

```Python
import pyautogui
import webbrowser as web
from time import sleep
from datetime import datetime

"""
Prueba muy simple de bot

Envia una cadena de texto de un fichero
"""

web.open("https://web.whatsapp.com/send?phone=+34653465545")
sleep(10)

def send_at():
    now = datetime.now()
    if hour(now):
        if min(now):
            pyautogui.typewrite("Ya es la hora")
            pyautogui.press("enter")

def hour(now):
    return now.hour == 10

def min(now):
    return now.minute == 30

with open("prueba.txt", "r") as file:
    for line in file:
        pyautogui.typewrite(line)
        pyautogui.press("enter")
        send_at()
```