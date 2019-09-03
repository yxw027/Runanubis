# Runanubis

## 软件用途
* G-nut Anubis 是一款非常成熟的数据质量分析软件，但是其成功编译和使用却有一定的困难。 在使用方面，G-nut Anubis只能一次性支持分析在同一段时间内的不同观测站的数据，同时，我们需要在config文件中准确的输入观测文件的观测起始时间和结束时间才能使程序正常运行。而这些信息其实都包括在了观测文件里面。本软件的用途就是从观测文件中提取这种没有必要自己录入的信息将其注入到config文件里面。同时，本软件还会通过启示观测时间的不同自动分类观测文件，然后分别运行G-nut Anubis。最后本软件会将输出的xtr文件通过 “anubisplot” 画出卫星的skyplot。

## 软件用法

* 1. 环境配置

     * 为了运行 "anubisplot.py"，我们需要安装python2(我安装的是python 2.7.16) 和其需要的库 "matplotlib"(我安装的是1.4.0版本) 以及 "numpy"(我安装的是1.10.4版本)，这里我没有选择安装官方文档中要求的更老版本的原因是只有我装的版本才能够不通过编译源码快速的在windows 环境下成功安装。

  2. 软件准备

     * 如filedemo文件夹下一样，将编译完成的 "Runanubisplot.exe" 与 "Anubis.exe" (编译完成的G-nut Anubis，可直接使用)， "anubisplot.py" (用于绘制skyplot的python脚本，可在官网找到）， 观测文件和配置文件放在同一目录下。在配置文件的<rec>节点下中输入所有观测站的四字简称。

  3. 运行软件

     * 打开cmd到刚才配置的文件夹目录，输入

       "Runanubisandplot.exe  [配置文件的名字] [G-nut Anubis 可执行文件的名字] [画图程序的名字]"

       而后理论上讲就可以成功将起始，终止时间注入config文件然后分别运行Anubis，最后运行画skyplot的程序了。