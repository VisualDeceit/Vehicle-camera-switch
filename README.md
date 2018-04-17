# Коммутатор видеосигналов для автомобиля 
Данный коммутатор предназначен для коммутации двух видеосигналов в автомобиле в зависимости от состояния сигналов управления.
В качестве сигналов управления выступают: включение заднего хода, кнопка включения передней камеры, скорость автомобиля.
## Алгоритм работы

| Задний ход | Кнопка | Выходной видеосигнал |
|  :---: |  :---: | :--- |
| 1  | 0 | Задняя камера |
| 1  | 1 | Задняя камера |
| 0  | 1 | Передняя камера |
| 1 -> 0 | 0 | Передняя камера на 10 сек  |

## Схема подключения
![Image of Yaktocat](https://github.com/VisualDeceit/Vehicle-camera-switch/blob/master/%D0%A1%D1%82%D1%80%D1%83%D0%BA%D1%82%D1%83%D1%80%D0%BD%D0%B0%D1%8F.JPG)

## Калибровка
Калибровка необходима для того, чтобы задать значение скорости при которой будет происходить автоматическое отключение передней камеры даже если нажата кнопка включения.<br>
При падаче питания устройство находится в режиме ожидания запуска колибровки в течение 5 секунд, при этом светодиод на плате мигает с периодничностью 1 раз в секунду. Для запуска режима калибровки необходимо нажать 3 раза кнопку вкл. передней камеры.
При правильной последовательности действий светодиод на плата начнет мигать 2 раза в секунду, что означает  режим калибровки. Если спустя 5 секунд после подачи питания режим калибровки не запущен, то светодиод начнет гореть постоянно, что соответсвует штатному режиму работы устройства. Для выхода из режима калибровки следует перевести селектор АКПП в положение "R".<br>
