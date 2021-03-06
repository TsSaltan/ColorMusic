# Управление светомузыкой c консоли
## Установка
В скетче изменить значение константы REMOTE_TYPE на 4
```c
#define REMOTE_TYPE 4 
```

## Команды для управления с консоли
* **mode {mode_№}** - изменение режима (от 1 до 9, как на пульте)
* **submode** - изменение подрежима
* **calibrate** - калибровка шума
* **power** - вкл/выкл ленты
* **bright+** - увеличение яркости горящих диодов
* **bright-** - уменьшение яркости горящих диодов
* **bright {bright_level}** - изменение уровня яркости горящих диодов
* **backlight+** - увеличение яркости негорящих светодиодов
* **backlight-** - уменьшение яркости негорящих светодиодов
* **backlight {bright_level}** - изменение яркости негорящих светодиодов
* **lightmode {mode_№}** - изменение подрежима у режима №7 (постоянная подсветка)
* **up** - настройка режима, кнопка вверх
* **down** - настройка режима, кнопка вниз
* **left** - настройка режима, кнопка влево
* **right** - настройка режима, кнопка вправо
* **handshake** - "рукопожатие", устройство должно вернуть своё название, чтоб программа с ПК смогла найти "своё" Arduino для управления

## Программа для управления с ПК
![Powershell RC Form](https://github.com/TsSaltan/ColorMusic/blob/master/PCRemoteControl/screenshot.jpg)
1. Если в диспетчере устройство Arduino определяется как **CH340**, то ничего менять не надо, запускаем файл **launcher.vbs**
2. Если же название у микросхемы другое, в файле **RCForm.ps1** меняем **CH340** на своё значение.