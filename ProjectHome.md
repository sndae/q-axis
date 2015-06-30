The reasons of making this project is to interest Taiwanese people in open source projects, like this MultiWii. If we get enough people to put their hand on this, one day we should be able to contribute our effort to the open source community.
So, Beside the current doc in Eng, I will start to write note in Chinese.

V2 board to come...

https://lh4.googleusercontent.com/-LFeWxJCEMes/TvgkXHajOpI/AAAAAAAAAr8/fUvN8GM94YQ/w339-h263-k/Qaxis.JPG

currently V1 board

![https://lh6.googleusercontent.com/-W0_7BYbuX6w/TvBPHhWjH7I/AAAAAAAAAr8/7KTiz8MUWoc/w568-h341-k/2011-12-19%2B21.05.29.jpg](https://lh6.googleusercontent.com/-W0_7BYbuX6w/TvBPHhWjH7I/AAAAAAAAAr8/7KTiz8MUWoc/w568-h341-k/2011-12-19%2B21.05.29.jpg)

**Q-axis** is made to fit with MultiWii quad fly control projects. The on board sensors are all supported by MultiWii since V1.9.(we also made a adaptation with V1.8 as well)
Read more about MultiWii http://www.multiwii.com/

**Q-axis contains:**

**3 axis gyro: L3G4200D**

**3 axis Acc and magnetic sensors: LSM303**

**processor: Mega328 at 16Mhz.**

The board can run at 5V and 3.3V, with modification of multiWii 1.9, it can also drive brushed motor.


The board has pin out fit with FTDI basic, down load is tested under Arduino 022.

Picture of the FTDI baisc we are using.

![https://lh5.googleusercontent.com/-Ccwq9y2BywE/TvBPO3bJRoI/AAAAAAAAApo/QMECS_Fs55U/w383-h230-k/FTDI.jpg](https://lh5.googleusercontent.com/-Ccwq9y2BywE/TvBPO3bJRoI/AAAAAAAAApo/QMECS_Fs55U/w383-h230-k/FTDI.jpg)

The board is currently testing on a small quad, it fly nice with default PID in MultiWiiV1.9

![https://lh4.googleusercontent.com/-tbU9vEkD3e8/TvBPHDcXRCI/AAAAAAAAApU/Vi5o9r6iGpQ/w383-h230-k/2011-12-19%2B22.26.52.jpg](https://lh4.googleusercontent.com/-tbU9vEkD3e8/TvBPHDcXRCI/AAAAAAAAApU/Vi5o9r6iGpQ/w383-h230-k/2011-12-19%2B22.26.52.jpg)

first test fly with brushless small quad
http://www.youtube.com/embed/DG1uagyJ8sA

2nd test fly in bedroom...
http://youtu.be/Hbz6OpgRNNM

# Making a Brushed multiWii #

It's so simple, once you understand, but you will need a MOSFET to drive brushed motor
[BrushedMotors](BrushedMotors.md)

# 實作分享 #

下面這些說明是用中文寫的,是把我實做上的經驗分享給大家, 也喜有一天, 台灣人也可以為open source貢獻一點創意...

組好你的multiWii後, 第一件要做的事情是確認版子可以跟MultiWiiConfig溝通,再來就要確認遙控器的細節

設定的方法請參考Wiki裏的[SetUpController](SetUpController.md)