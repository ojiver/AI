Google Colab——零成本玩转深度学习<br/>
前言<br/>
最近在学深度学习HyperLPR项目时，由于一直没有比较合适的设备训练深度学习的模型，所以在网上想找到提供模型训练，经过一段时间的搜索，最终发现了一个谷歌的产品--Google Colaboratory。它几乎可以实现零成本玩转深度学习，达到快速训练模型的目的。<br/>

Google Colaboratory是谷歌开放的一款深度学习的研究工具，主要用于深度学习的开发和研究。这款工具现在是可以免费使用，但是暂时还是无法确定是不是永久免费。Google Colab最大的好处是给广大的AI开发者提供了免费的GPU和TPU使用！GPU型号是Tesla K80！你可以在上面轻松地跑例如：Keras、Tensorflow、Pytorch等框架。<br/>

 

Google Colab基本操作<br/>
网站：Google Colab<br/>

进入Google Colab网站-》新建项目<br/>
![image](https://github.com/ojiver/AI/blob/main/1.jpg?raw=true)
新建项目<br/>
创建完项目之后我们就可以进入Colab的主界面了。<br/>
![image](https://github.com/ojiver/AI/blob/main/2.jpg?raw=true)
添加代码块<br/>
 
现在，我们就可以在代码框中输入一些代码。这里注意，如果我们直接输入代码，系统会当作是Python代码执行。例如我们输入：<br/>
![image](https://github.com/ojiver/AI/blob/main/3.jpg?raw=true)

运行之后输出框中会打印出"1"。<br/>
![image](https://github.com/ojiver/AI/blob/main/6.jpg?raw=true)
运行结果<br/>

如果想去执行系统命令，只需要在命令前加感叹号!。例如我们输入：<br/> 
![image](https://github.com/ojiver/AI/blob/main/5.jpg?raw=true)

运行结果如下： <br/>
![image](https://github.com/ojiver/AI/blob/main/4.jpg?raw=true)

运行结果<br/>

执行之后输出框中会显示当前目录下的所有文件夹。这是不是很像Linux下的命令行操作？<br/>

其实在Google Colab中连接的云端的那台虚拟机正是使用的Ubuntu操作系统，我们可以将自己在Google Colab中的一切操作看作是在用命令行控制云端的那台Ubuntu虚拟机。你可以用它来直接跑代码，也可以使用一些系统命令（我们后面要安装第三方软件都需要借助一系列的系统命令）。

 

前期配置<br/>
1. 修改笔记本环境<br/>
每新建一个Colab项目，都需要先对笔记本环境进行配置，运行类型选择是Python2还是Python3，硬件类型选择CPU、GPU或者TPU。（其中Python2是2.7版本，Python3是3.6版本）<br/>
![image](https://github.com/ojiver/AI/blob/main/7.jpg?raw=true)

 修改完后点击保存即可。<br/>

2. 安装必要的包和软件<br/>
在代码段中输入以下代码：<br/>

 ![image](https://github.com/ojiver/AI/blob/main/8.jpg?raw=true)

运行代码，运行中会提示输入验证码，点击程序给出的网址进行验证即可。<br/>

3. 挂载Google Drive<br/>
其实完成前面的操作我们就可以在Google Colab中敲写代码或者输入一些系统命令了，但是我们现在连接的虚拟机是和Google Drive脱离的，也就是说我们跑的程序无法使用谷歌云盘里的文件，这就非常受限制了。所以我们一般需要将谷歌云盘看作是虚拟机中的一个硬盘挂载，这样我们就可以使用虚拟机轻松访问谷歌云盘。<br/>
挂载Google Drive代码：<br/>

![image](https://github.com/ojiver/AI/blob/main/9.jpg?raw=true)

运行挂载Google Drive代码会出现应认证的链接<br/>

![image](https://github.com/ojiver/AI/blob/main/10.jpg?raw=true)

装载Google Drive<br/>
 点击链接获得应用认证码<br/>
 
![image](https://github.com/ojiver/AI/blob/main/11.jpg?raw=true)

 应用认证码<br/>
 将应用认证码复制输入到下面的文本框中，点击回车键即可
![image](https://github.com/ojiver/AI/blob/main/12.jpg?raw=true)

![image](https://github.com/ojiver/AI/blob/main/13.jpg?raw=true)

加载成功

 挂载完后在虚拟机中会多出一个文件夹"drive"，我们可以用<br/>
 

 命令查看。<br/>

 更改工作目录<br/>
在Colab中cd命令是无效的，切换工作目录使用chdir函数。<br/>



执行以上代码，当前工作目录会进入到drive文件夹下。我们再使用!ls命令会发现系统输出的是drive文件夹下的目录。<br/>

回到上级目录：<br/>
![image](https://github.com/ojiver/AI/blob/main/14.jpg?raw=true)

![image](https://github.com/ojiver/AI/blob/main/15.jpg?raw=true)

运行自己的代码<br/>
好了，各种准备工作都做好了，我们如何在Colab上直接运行自己写好的代码呢？其实很简单，就跟在自己电脑上一样，使用命令<br/>

![image](https://github.com/ojiver/AI/blob/main/16.jpg?raw=true)


就可以了！详细步骤如下：<br/>

1. 将.py文件和其它必要的文件上传到Google Drive<br/>
上传速度很快，不用担心网速问题~<br/>
2. 将工作目录切换到.py文件所在目录<br/>

![image](https://github.com/ojiver/AI/blob/main/17.jpg?raw=true)


如果不放心的话切换完之后用!ls命令看一下是不是到了指定目录下。<br/>

3. 运行代码<br/>

![image](https://github.com/ojiver/AI/blob/main/18.jpg?raw=true)

4. 注意事项<br/>
Linux系统下文件路径使用'/'而不是'\'<br/>


总结<br/>
1.可以把Google Colab看成是一台带有GPU或者TPU的Ubuntu虚拟机，只不过我们只能用命令行的方式操作它。你可以选择执行系统命令，也可以直接编写运行python代码。<br/>

2.挂载完Google Drive，会在虚拟机里生成一个drive文件夹，直接将Google Drive当成是一块硬盘即可。访问drive文件夹里的文件，就是在访问你的Google Drive里的文件。<br/>

3.Colab最多连续使用12小时，超过时间系统会强制掐断正在运行的程序并收回占用的虚拟机。（好像再次连接到虚拟机后，虚拟机是被清空的状态，需要重新配置和安装库等等）<br/>

4.请使用科学-上网方式。<br/>

好了，Google Colab的使用方法就先介绍到这里了，笔者也是刚接触不久，写下了这篇使用总结的文章与大家分享。文中若有问题之处，还请大家多多包涵，可以在评论区指出我的错误，互相学习。<br/>
