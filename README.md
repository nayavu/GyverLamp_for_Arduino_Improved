﻿# GyverLamp for Arduino 

Это оптимизированная версия прошивки Gyver Lamp для Arduino.

Это форк прошивки от ![x-plora](https://github.com/x-plora/GyverLamp_for_Arduino), который в свою очередь является форком прошивки ![Norovl](https://github.com/Norovl/GyverLamp_for_Arduino), которая является форком оригинальной прошивки от ![AlexGyver](https://github.com/AlexGyver/GyverLamp/)

## Краткое описание:

Лампа на адресных светодиодах, позволяющих получить красивые эффекты свечения.

Суммарные отличия от оригинала:
- 	убран будильник;
- 	убрана работа с Wi-Fi (у ардуинки его нет);
-   убран GyverButton в пользу собственной реализации на прерываниях — кнопка теперь работает стабильно!
- 	сохранение яркости всех эффектов, в т.ч. текущего режима в энергонезависимой памяти.
    Производится четырех нажатием кнопки, подтверждением будет выключение и включение лампы;
-   сильно оптимизировано потребление памяти эффектами (Arduino Nano вытягивает матрицу 24x16 светодиодов);
-   отрефакторен код;
-   8 позиций уровня яркости (что значительно удобнее для управления)

Отличия от родительских форков для Arduino:
-   сильно оптимизировано потребление памяти
-   присутствует эффект "Светляки"
-   убран GyverButton в пользу собственной реализации на прерываниях — кнопка теперь работает стабильно!
-   сильно оптимизировано потребление памяти эффектами (Arduino Nano вытягивает матрицу 24x16 светодиодов);
-   отрефакторен код;
-   настроены параметры эффектов (speed & scale) для адекватного отображения

Регулировка уровня яркости/скорости/масштаба реверсивная, т.е. при повторном
регулировании изменения будут производиться в обратную сторону (сначала в бОльшую,
затем в мЕньшую).

Подключение Arduino:
- кнопка - pin 2. Arduino Nano возможно подключить к пинам 2 или 3, для других - смотрите их интеррапты;
- LED - pin 4. Возможно подключить на любой пин.

## Компиляция и загрузка прошивки

`pio run -t upload`
