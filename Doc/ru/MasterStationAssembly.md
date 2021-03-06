Компоненты станции сопряжения

![](https://raw.githubusercontent.com/alexandervolikov/sportiduino/master/Images/w01.jpg)

1.	RFID-модуль RC522. Довольно распространён. 

2.	Arduino nano. Можно подключать напрямую к компьютеру. Есть вариации на каком чипе происходит реализация Serial-USB порта, более дорогой FT232RL и более дешевый CHG340, для подключения второго нужно установить драйвера на компьютер. Я использовал более дешевый вариант

3.	Плата для спайки. Я заказывал через сервис EasyEDA, остался доволен. Стоимость зависит от партии, минимальное число 5. Целесообразно заказывать платы для станции сопряжения одновременно с платами для станций отметки. 

4.	Штырьки, светодиод и пищалка. Впрочем, пищалку можно поискать и получше. У дешевых довольно сильно гуляют характеристики, в итоге станции пищат с разной громкостью и немного в разной тональности.

5.	Корпус Gainta 1020BF. Хороший корпус из ABS пластика, неплохо поддается допиливанию под свои цели. Покупал в России 

6.	USB-шнурок. Зависит от используемого порта в Arduino Nano/ У меня micro-usb.
	
Сначала нужно спаять ардуино нано, хотя можно заказать с уже спаянными ножками. Промазываем ножки и отверстия флюсом, паяем. ISP (2*3 разъём) можно не паять, но с его помощью можно прошивать станции и обойтись без дополнительного программатора в виде Arduino Uno. 

![](https://raw.githubusercontent.com/alexandervolikov/sportiduino/master/Images/w02.jpg )

Далее впаиваем в основную плату. Также в основную плату впаиваем разъём 1*8, согнутый углом светодиод, пищалку и резисторы 0805 на 47 ом (к пищалке) и 150 ом к светодиоду

![](https://raw.githubusercontent.com/alexandervolikov/sportiduino/master/Images/w03.jpg)
 

Затем припаиваем модуль RFID. Подключаем через провод USB к компьютеру.
 
![](https://raw.githubusercontent.com/alexandervolikov/sportiduino/master/Images/w04.jpg)


Открываем программу Arduino на компьютере, в настройках указываем тип платы (Arduino Nano), выбираем нужный COM порт и заливаем прошивку RFID_ReadSet на плату.

Примеряем корпус. Плата у меня получилась немножко неудачная, кабель еле влазит, хорошо бы немного сместить ардуино нано и поставить её под углом. Но втиснуть можно. Для провода вырезается небольшая канавка в корпусе. Светодиод промазывается эпоксидкой.
 
![](https://raw.githubusercontent.com/alexandervolikov/sportiduino/master/Images/w05.jpg)

После чего корпус закручивается и готов к использованию.

![](https://raw.githubusercontent.com/alexandervolikov/sportiduino/master/Images/w06.jpg)