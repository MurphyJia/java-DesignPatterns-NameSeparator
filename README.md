# learning-java
* 做了一个姓名分离器，通过规定格式输入姓名可以将姓与名分离再进行输出。主要算法参考中国电力出版社的《Java设计模式》（James W. Cooper著）中第三章《工厂模式》，UI界面是自己设计的。
* 本人是一名大二学生，计算机专业，第一次在这里记录下自己平时写的代码。技术不足，请多多包涵，欢迎指点批评。
* Hi, you can call me Vera. I'm a sophomore, majoring in computer science. If the technical level is not high, please forgive me. This is the first time I recorded my usual code practice in GitHub. The main algorithm of this small code refers to “Java design pattern” (by James W. Cooper) published by China Electric Power Publishing House. The UI design interface is written by myself. The level of UI interface design is not high, and I have just been self-taught.
## Introduction of my programme 程序介绍
* 假设要建立一个登记表，允许按照规定的格式，例如：“名 姓”或者“姓，名”来录入姓名。简而言之，这个程序的功能就是通过姓和名之间是否有逗号来确定姓名的顺序。步骤如下：
1. 首先要定义一个简单的基类，代码中对应的是Name类，它的主要功能是为两个子类提供继承和扩展
2. 子类一，代码中的FistName类，在它的构造函数中要把姓名划分为姓和名两个部分。在这个类中，假设最后一个空格前的所有字符都属于名都组成部分
3. 子类二，代码中的LastName类，假设逗号（英文状态下）是姓与名之间的分隔符。以上的两个类都提供了错误的恢复机制，防止不存在空格或者逗号的情况发生。
4. 构建简单工厂，代码中的NameFactory类，只要检测是否存在逗号并返回其中的某个子类实例即可。
* 在确定完模式后，我构造了一个水平不高的简单Java用户界面，可以按照不同的顺序输入姓名，并能够分别显示出姓和名两个部分。如果输入姓名并按下Compute键，两个文本框就会显示出划分之后的姓和名。这个程序的关键在于如何提取文本、获得Name类的一个实例以及如何显示结果
* 对于简单工厂方法，首先是要创建一个提取方法，它能够在多个可能的类中决定返回哪一个类的实例，并将其返回。然后就可以调用该类实例的方法了，而不必了解实际使用的是哪一个子类。这种防护可以使数据依赖性问题与类的可用方法分离。

* Suppose you want to create a registration form that allows names to be entered in a prescribed format, such as "first name, last name" or "last name,first name.". In short, the function of this program is to determine the order of names by whether there is a comma between the last name and the first name. The steps are as follows:
1. First, a simple base class should be defined. The code corresponds to the name class. Its main function is to provide inheritance and extension for the two subclasses
2. Subclass 1, the fistname class in the code. In its constructor, the name should be divided into two parts: first name and last name. In this class, assume that all characters before the last space are part of the name
3. Subclass 2, LastName class in the code, assuming that comma (in English state) is the separator between last name and first name. Both classes provide error recovery mechanisms to prevent the absence of spaces or commas.
4. Build a simple factory. For the namefactory class in the code, you only need to detect whether there is a comma and return an instance of one of its subclasses.
* After determining the mode, I constructed a simple java user interface with low level, which can input names in different order, and display the last name and first name parts respectively. If you enter a name and press the compute key, two text boxes will display the first and last names after division. The key to this program is how to extract text, get an instance of the name class, and how to display the results
* For a simple factory method, the first step is to create an extraction method that can decide which instance of a class to return from multiple possible classes and return it. You can then call the method of the class instance without knowing which subclass is actually used. This protection separates data dependency issues from the available methods of the class.
