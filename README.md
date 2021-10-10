## Welcome to last run

You can use the [editor on GitHub](https://github.com/wjqbugkiller/wjqbugkiller.github.com/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.


### 基础介绍

> #### What is Arduino
> - Arduino is an open source electronic platform that includes hardware and software.
> - The hardware part is an Arduino board that can be used for circuit connection, and the software part is Arduino IDE which is a program in the computer that used for development.
> - Software（Arduino IDE）can be downloaded from [Arduino](https://www.arduino.cc/en/software/)

![图片](/docs/arduino基础介绍图片裁剪完毕/image1.jpeg)![图片](/docs/arduino基础介绍图片裁剪完毕/image2.jpg)
<center class="half">
    <img src="/docs/arduino基础介绍图片裁剪完毕/image1.jpeg" width="200"/><img src="/docs/arduino基础介绍图片裁剪完毕/image2.jpg" width="200"/>
</center>

> #### The function of Arduino
>> Output device
>> - Arduino can use existing electronic components, such as switches, drives or many other sensors to make an interactive device. It can be used to make hardware equipment such as electronic production or creative design prototypes.

>> Art interactive works
>> - Arduino can also build art interactive works though integrating ideas and sensors in a simple or unified way. Using sensors to sense and affect the environment by controlling lights, motors and other devices. This kind of work can be an original object, a wall, or combined with other objects in life.

>> Interactive software
>> - Arduino can be used with many software, such as processing, brain-link, etc. Their cooperation can create many interesting visually interactive software or pages. Interaction with the computer is no longer limited to the mouse and keyboard. Sound, infrared, touch, pressure human motion catcher and many other facts can become the input source of the computer.

> #### The choice for Arduino
>> - The official Arduino team adopted the Creative Commons license. Anyone is allowed to produce and sell copies of the Arduino development board. Therefore, there are two kinds of development boards.Therefore, there are two kinds of development boards, one is the official board, and the other is the clone board of other manufacturers. 
>> 
>> - Both official boards and clone boards are legal products.
>> 
>> - The production process of the official board will be more excellent and more expensive.
>> 
>> - There are many types of Arduino development board, which can be roughly divided into five categories: Entry Level, Enhanced Features, Internet of Things, Education, and Retired.
>> 
>> - You can view all of them from the official website:[Arduino.Products](https://www.arduino.cc/en/Main/Products)
>> 
>> - There are not much options for us, we got only Arduino UNO. We have two pieces in our hands. One is turquoise and the other is black. They are both made in China. We can easily buy them in a cheap price.

> #### Connection with computer
>> Wire
>> 
>> - Two types of wires in our group
>> 
>> Development board and port selection
>> - ‘Arduino on comX’ is in the lower right corner of the Arduino IDE. X stands for number.
>> 
>> - Click the ‘工具 – 开发板’ at the toolbar and choose the Arduino type. 
>> 
>> - Then select the comX in the ‘工具-端口’.

> ### Web
>> Circuit drawing at: [Thinkercad](https://www.tinkercad.com/dashboard)
>> 
>> Recommendations for Color-Ring-Resistance calculation: [Elecfans](http://www.elecfans.com/tools/)

### 小组作业介绍

> ### Case 1: LED light with a button

>> - We tried this case in the class to learn about the basic digital I/O in Arduino. In this case, we can control the LED light with a button. When the button is pressed,  the LED light is off; otherwise the light is on.
Here is the circuit of this case.

>> - Here is the code and the video of this case.
```c
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
```

![视频]（/docs/小组作业图片素材/视频1.mp4）

### 模型
这是一个测试链接[模型](https://github.com/wjqbugkiller/wjqbugkiller.github.com/blob/main/docs/%E6%A8%A1%E5%9E%8B.pptx)

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/wjqbugkiller/wjqbugkiller.github.com/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
