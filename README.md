[//]: # (Image References)

[image1]: ./pic/ArduinoPref.png "Preferences view"
[image2]: ./pic/ArduinoTools.png "Tools view"
[image3]: ./pic/TrafficLight.png "Traffic Light"
[image4]: ./pic/LaserGate.jpg "Laser Gate"


# **TrafficLights**
---

Это репозиторий для прошивок светофоров [Makely Traffic Light v2](makely.ru/traffic-light) ![image3] и лазерных ворот [Makely Laser Gate v2](makely.ru/laser-gate). ![image4]


## Структура папок
---
/OTA-Alone - Ардуино прошивка для независимой работы светофора

/OTA-Light - Ардуино прошивка для групповой работы стартовых светофоров и двух светофоров на одном направлении перекрестка

/OTA-Light_inverse - Ардуино прошивка для групповой работы двух светофоров на поперечном направлении перекрестка

/OTA-LaserGates - Ардуино прошивка для лазерных ворот по регламенту Роботраффика в категории "Скорость"

/DesktopServer - Серверные приложения для ПК на Windows/macOS/Linux Python3 для управления светофорами и лазерными воротами в категориях "Город" (city.py) и "Скорость" (speed.py)

## Использование
---
### Программирование светофоров

#### Подготовка

Для программирования возможно понадобится установить драйвера USB-UART интерфейса отсюда: https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers

Arduino IDE должна быть не менее 1.6.4 (лучше скачать последнюю (1.8.5 на данный момент) с официального сайта Arduino). В ней заходите в настройки и прописываете ссылку на репозиторий поддержки дополнительных плат (Additional Board Manager URLs): http://arduino.esp8266.com/stable/package_esp8266com_index.json
Затем заходите в менеджер дополнительных плат, находите там esp8266 и устанавливаете последнюю версию.
![Pref][image1]

Все, теперь выбираете из списка плат "NodeMCU 1.0 (ESP-12E Module)", нужный последовательный порт и проверяете остальные параметры, чтобы были как на следующей картинке.
![Tools][image2]

#### Программирование

Открываете нужную прошивку для светофора из репозитория - файл \*.ino. Откроется среда ArduinoIDE, если все правильно настроили на предыдущем щаге, остается заменить имя и пароль беспроводной среды (переменные **ssid** и **password**) и нажать на кнопку "загрузить скетч".
