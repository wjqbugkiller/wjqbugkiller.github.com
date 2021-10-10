## Welcome to our OUTLAST Zone
This is where a group of exhausted people try to make something valuable. Do not be surprised if you see this place randomly changing sometimes.  It will record the required homework weekly in time if they have not drowned in numerous tasks. If in such luck, they will OUTLAST time and catch up as quickly as possible. Cheer:sunglasses::beers:!!!
🚀
-------------------------

### 基础介绍

> #### What is Arduino
> - Arduino is an open source electronic platform that includes hardware and software.
> - The hardware part is an Arduino board that can be used for circuit connection, and the software part is Arduino IDE which is a program in the computer that used for development.
> - Software（Arduino IDE）can be downloaded from [Arduino](https://www.arduino.cc/en/software/)

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午8.32.47.png">
</center>

> #### The function of Arduino
>> Output device
>> - Arduino can use existing electronic components, such as switches, drives or many other sensors to make an interactive device. It can be used to make hardware equipment such as electronic production or creative design prototypes.

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午8.54.11.png">
</center>

>> Art interactive works
>> - Arduino can also build art interactive works though integrating ideas and sensors in a simple or unified way. Using sensors to sense and affect the environment by controlling lights, motors and other devices. This kind of work can be an original object, a wall, or combined with other objects in life.

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午8.56.54.png">
</center>

>> Interactive software
>> - Arduino can be used with many software, such as processing, brain-link, etc. Their cooperation can create many interesting visually interactive software or pages. Interaction with the computer is no longer limited to the mouse and keyboard. Sound, infrared, touch, pressure human motion catcher and many other facts can become the input source of the computer.

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午9.10.23.png">
</center>

> #### The choice for Arduino
>> - The official Arduino team adopted the Creative Commons license. Anyone is allowed to produce and sell copies of the Arduino development board. Therefore, there are two kinds of development boards.Therefore, there are two kinds of development boards, one is the official board, and the other is the clone board of other manufacturers. 
>> 
>> - Both official boards and clone boards are legal products.
>> 
>> - The production process of the official board will be more excellent and more expensive.

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午9.12.44.png">
</center>

>> - There are many types of Arduino development board, which can be roughly divided into five categories: Entry Level, Enhanced Features, Internet of Things, Education, and Retired.
>> 
>> - You can view all of them from the official website:[Arduino.Products](https://www.arduino.cc/en/Main/Products)
>> 
>> - There are not much options for us, we got only Arduino UNO. We have two pieces in our hands. One is turquoise and the other is black. They are both made in China. We can easily buy them in a cheap price.

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午9.15.21.png">
</center>

> #### Connection with computer
>> Wire
>> 
>> - Two types of wires in our group

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午9.17.38.png">
</center>

>> Development board and port selection
>> - ‘Arduino on comX’ is in the lower right corner of the Arduino IDE. X stands for number.
>> 
>> - Click the ‘工具 – 开发板’ at the toolbar and choose the Arduino type. 
>> 
>> - Then select the comX in the ‘工具-端口’.

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午9.19.44.png">
</center>

> #### Web
>> Circuit drawing at: [Thinkercad](https://www.tinkercad.com/dashboard)
>> 
>> Recommendations for Color-Ring-Resistance calculation: [Elecfans](http://www.elecfans.com/tools/)

-------------------------

### 小组作业介绍

> ### Case 1: LED light with a button

>> - We tried this case in the class to learn about the basic digital I/O in Arduino. In this case, we can control the LED light with a button. When the button is pressed,  the LED light is off; otherwise the light is on.
>> - Here is the circuit of this case:

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午9.30.57.png">
</center>

>> - Here is the code of this case:

~~~c
int ledPin=13;//led连接pin的13脚
int inPin=7;
int val=0;

void setup() {
  // put your setup code here, to run once:
  pinMode(ledPin,OUTPUT);
  pinMode(inPin,INPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
  val=digitalRead(inPin);
  digitalWrite(ledPin,val);

}
~~~

>> - Here is the video:
>>> - [Video:Case 1]()

> #### Case 2: LED light with a button: pro version

>> - When we finished Case 1, we felt a little bit inconvenient in this application for we usually turn on the light with one press and then turn it off with another. In Case 1, however, the light is on immediately when we release the button. So, we did some changes to Case 1 code and made it a pro version.

>> - Here is the code of this case:

~~~c
const int buttonPin = 7;
const int ledPin = 13;

// 按键前一个状态
int oldButtonState = HIGH;
// 按键状态
int buttonState = HIGH;
// led灯状态，false->没亮，true->亮
boolean ledState = false;


void setup() {
  // 使用内置上拉电阻
  pinMode(buttonPin, INPUT_PULLUP);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  // 单次按动开关LED灯
  oldButtonState = buttonState;
  buttonState = digitalRead(buttonPin);
  if(buttonState == LOW && oldButtonState == HIGH) {
    if(ledState == true) {
      digitalWrite(ledPin, LOW);
    } 
    else {
      digitalWrite(ledPin, HIGH);
    }
    ledState = !ledState;
  }
}
~~~

>> - Here is the video:

>>> - [Video:Case 2]()

> #### Case 3: try something new: Speech recognition module & Gesture recognition module
>> - For some of our group members have tried Arduino before, we have some other modules which are not included in the basic Arduino kit. So we used the speech recognition module and the gesture recognition module in our Case 3.

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午9.33.37.png">
</center>

>> - In this case, the user should speak the word “kai shi”（开始）to start and get into the gesture recognition mode, which will turn on the green LED light at the same time to show that you are allowed to do the gesture. When the user move his ore her hand left and right, the red light will be on; but if the hand is moving up and down, the yellow light will be on otherwise. After finishing the gesture recognition, the green light and the indicator light will be off and the device will get into the next loop.

<center class="half">
    <img src="/docs/图片/图片5.png">
</center>

>> - Here is the circuit:

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午10.03.39.png">
</center>

>> - Here is the code:

~~~c
#include <Wire.h>
#include "paj7620.h"
#define I2C_ADDR    0x79
#define ASR_RESULT_ADDR           100
//识别结果存放处，通过不断读取此地址的值判断是否识别到语音，不同的值对应不同的语音，
#define ASR_WORDS_ERASE_ADDR      101//擦除所有词条
#define ASR_MODE_ADDR             102
//识别模式设置，值范围1~3
//1：循环识别模式。状态灯常亮（默认模式）
//2：口令模式，以第一个词条为口令。状态灯常灭，当识别到口令词时常亮，等待识别到新的语音,并且读取识别结果后即灭掉
//3：按键模式，按下开始识别，不按不识别。支持掉电保存。状态灯随按键按下而亮起，不按不亮
#define ASR_ADD_WORDS_ADDR        160//词条添加的地址，支持掉电保存
int i;
unsigned char result; // Read Bank_0_Reg_0x43/0x44 for gesture result.

bool WireWriteByte(uint8_t val)
{
  Wire.beginTransmission(I2C_ADDR);
  Wire.write(val);
  if ( Wire.endTransmission() != 0 ) {
    return false;
  }
  return true;
}

bool WireWriteDataArray(  uint8_t reg, uint8_t *val, unsigned int len)
{
  unsigned int i;

  Wire.beginTransmission(I2C_ADDR);
  Wire.write(reg);
  for (i = 0; i < len; i++) {
    Wire.write(val[i]);
  }
  if ( Wire.endTransmission() != 0 ) {
    return false;
  }
  return true;
}

int WireReadDataArray(   uint8_t reg, uint8_t *val, unsigned int len)
{
  unsigned char i = 0;
  /* Indicate which register we want to read from */
  if (!WireWriteByte(reg)) {
    return -1;
  }
  Wire.requestFrom(I2C_ADDR, len);
  while (Wire.available()) {
    if (i >= len) {
      return -1;
    }
    val[i] = Wire.read();
    i++;
  }
  /* Read block data */
  return i;
}

/*
   添加词条函数，
   idNum：词条对应的识别号，1~255随意设置。识别到该号码对应的词条语音时，
          会将识别号存放到ASR_RESULT_ADDR处，等待主机读取，读取后清0
   words：要识别汉字词条的拼音，汉字之间用空格隔开
   执行该函数，词条是自动往后排队添加的。
*/
bool ASRAddWords(unsigned char idNum, unsigned char *words)
{

  Wire.beginTransmission(I2C_ADDR);
  Wire.write(ASR_ADD_WORDS_ADDR);
  Wire.write(idNum);
  Wire.write(words, strlen(words));
  if ( Wire.endTransmission() != 0 ) {
    delay(10);
    return false;
  }
  delay(10);
  return true;
}


void gesture() {
  uint8_t data = 0;
  paj7620ReadReg(0x43, 1, &data);
  if (data == GES_LEFT_FLAG || data == GES_RIGHT_FLAG) {  //左右移动手，红灯亮
    digitalWrite(48, HIGH);
    digitalWrite(50, LOW);
    Serial.println("red light on");
    delay(1500);
    digitalWrite(48, LOW);
    result = 0;
    digitalWrite(46, LOW);
  }
  else if (data == GES_UP_FLAG || data == GES_DOWN_FLAG) {  //上下移动手，黄灯亮
    digitalWrite(50, HIGH);
    digitalWrite(48, LOW);
    Serial.println("yellow light on");
    delay(1500);
    digitalWrite(50, LOW);
    result = 0;
    digitalWrite(46, LOW);
  }
}

void setup()
{
  paj7620Init();       //初始化手势传感器芯片PAJ7620

  uint8_t ASRMode = 1;//1：循环识别模式    2：口令模式，以第一个词条为口令    3按键模式，按下开始识别
  Wire.begin();
  Serial.begin(9600);

#if 1   //添加的词条和识别模式是可以掉电保存的，第一次设置完成后，可以将此段注释掉，即将1改为0，然后重新下载一次程序
  WireWriteDataArray(ASR_WORDS_ERASE_ADDR, NULL, 0);
  delay(60);//擦除需要一定的时间
  ASRAddWords(1, "kai shi");            //开始
  if (WireWriteDataArray(ASR_MODE_ADDR, &ASRMode, 1))
    Serial.println("ASR Module Initialization complete");
  else
    Serial.println("ASR Module Initialization fail");
#endif
  i = 0;
  Serial.println("Start");
}

void loop() {
  delay(1);
  WireReadDataArray(ASR_RESULT_ADDR, &result, 1);

  if (result) {
    i = 1;
    Serial.print("ASR result is:");
    Serial.println(result);//返回识别结果，即识别到的词条编号
    digitalWrite(46, HIGH);//绿灯亮
    while (result == 1) {
      gesture();
    }
  }
  delay(200);
}
~~~

>> - Here is the video:

>>> - [Video:Case 3]()

-------------------------

### 模型

> #### An Elastic (rubber band) Powered Car
>> - We used Creo to build a simple 3D model of an elastic (rubber band) powered car. The car is driven by rubber bands and can travel a distance in a straight line. Its main components are: body bracket (using lighter carbon fiber tubes to reduce resistance), connection structure , Bevel gears, bearings, screws, rotating modules, tires, wheels.

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午10.15.15.png">
</center>

> #### Three-view Drawing

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午10.17.39.png">
</center>

> #### Exploded Views

<center class="half">
    <img src="/docs/模型图片/动图1.gif">
    <img src="/docs/模型图片/动图3.gif">
    <img src="/docs/模型图片/动图4.gif">
</center>

> #### Components
>> - In the process of creating the model, we used functions such as sketching, extruding, drafting, building threads, rounding, circular bending, drawing space curves, boundary blending, surface merging, solidification, dimensioning, etc. Since Creo has certain limitations when creating curved surfaces, the car shows more straight lines and planes, and it takes more time to create the surface of the racing wheel hub.

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午10.21.04.png">
</center>

> #### The position of the rubber bands

<center class="half">
    <img src="/docs/图片/截屏2021-10-10 下午10.12.03.png">
</center>

------------------------

