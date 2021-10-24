# FingerTexter

如何优雅的解锁一个台式机

![FingerTexter-1](https://github.com/xusixteen/FingerTexter/blob/main/FingerTexter-1.png)

![FingerTexter-2](https://github.com/xusixteen/FingerTexter/blob/main/FingerTexter-2.jpg)

## 功能
### 设备映射成USB键盘，通过指纹输入台式机登陆密码“asdasdasd”，并且自动按下回车键。
### 灵感基于稚辉君的项目 https://github.com/peng-zhihui/FingerBoard
### 硬件方案基于STM32F103单片机+BM2166指纹模块，整合了正点原子的基本库函数版本的USB键盘驱动,开发环境是Keil4，并没有采用主流的HAL库+CUBE MX的方法。
### 指纹模块驱动兼容AS0608等。
### 结构参考了3D打印素材钢铁侠，截取半身像并添加圆形底座。

![dock](https://github.com/xusixteen/FingerTexter/blob/main/dock.png)

## 现有不足
### STM32 pin33（USB-PWR-DP）需加10K上拉电阻，才可识别为2.0高速从机。
### 原理图中已经做出相应修改，但没有更新到PCB中。所以PCB直接打样会有上述问题。

![pcb-1](https://github.com/xusixteen/FingerTexter/blob/main/pcb-1.png)

![pcb-2](https://github.com/xusixteen/FingerTexter/blob/main/pcb-2.png)

## TODO
### 1、WS2812 全彩LED驱动做状态指示。
### 2、增大Flash存储，识别到特定指纹输入后进入U盘模式。将U盘制作为PE启动盘，进而可以解锁更多未知密码的设备。
