Google Colab——零成本玩转深度学习
前言
最近在学深度学习HyperLPR项目时，由于一直没有比较合适的设备训练深度学习的模型，所以在网上想找到提供模型训练，经过一段时间的搜索，最终发现了一个谷歌的产品--Google Colaboratory。它几乎可以实现零成本玩转深度学习，达到快速训练模型的目的。

Google Colaboratory是谷歌开放的一款深度学习的研究工具，主要用于深度学习的开发和研究。这款工具现在是可以免费使用，但是暂时还是无法确定是不是永久免费。Google Colab最大的好处是给广大的AI开发者提供了免费的GPU和TPU使用！GPU型号是Tesla K80！你可以在上面轻松地跑例如：Keras、Tensorflow、Pytorch等框架。

 

Google Colab基本操作
网站：Google Colab

进入Google Colab网站-》新建项目
![image](https://github.com/ojiver/AI/blob/main/1.jpg?raw=true)
创建完项目之后我们就可以进入Colab的主界面了。
![image](https://github.com/ojiver/AI/blob/main/2.jpg?raw=true)
现在，我们就可以在代码框中输入一些代码。这里注意，如果我们直接输入代码，系统会当作是Python代码执行。例如我们输入：
![image](https://github.com/ojiver/AI/blob/main/3.jpg?raw=true)
运行之后输出框中会打印出"1"。
![image](https://github.com/ojiver/AI/blob/main/4.jpg?raw=true)
运行结果
如果想去执行系统命令，只需要在命令前加感叹号!。例如我们输入： 
![image](https://github.com/ojiver/AI/blob/main/5.jpg?raw=true)
运行结果如下： 
![image](https://github.com/ojiver/AI/blob/main/6.jpg?raw=true)
运行结果

执行之后输出框中会显示当前目录下的所有文件夹。这是不是很像Linux下的命令行操作？

其实在Google Colab中连接的云端的那台虚拟机正是使用的Ubuntu操作系统，我们可以将自己在Google Colab中的一切操作看作是在用命令行控制云端的那台Ubuntu虚拟机。你可以用它来直接跑代码，也可以使用一些系统命令（我们后面要安装第三方软件都需要借助一系列的系统命令）。

 

前期配置
1. 修改笔记本环境
每新建一个Colab项目，都需要先对笔记本环境进行配置，运行类型选择是Python2还是Python3，硬件类型选择CPU、GPU或者TPU。（其中Python2是2.7版本，Python3是3.6版本）
![image](https://github.com/ojiver/AI/blob/main/7.jpg?raw=true)
