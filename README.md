

# ASD工具箱（ASD圆你一个黑客梦）

```
https://github.com/huntingsec/asdtools
```

天下武功，无坚不破，唯快不破

![logo](https://github.com/huntingsec/asdtools/logo.png)

为了快速上手，快速打点而生（由此得名：键盘输入asd是最快的[肌肉记忆了]）

本项目，目前只集成了快速打点的GUI工具和一小部分命令行工具（为了不和GUI进行混淆，后面会将所有蓝队应急的命令，攻防的命令以及APT手法等单独集成到工具箱中的一个模块）。

收集于各位大佬们的精选工具，也是日常必备，使用率最高的几个工具。

#### 下载到本地

![image-20240701203637270](https://github.com/huntingsec/asdtools/image-20240701203637270.png)

#### 解压

```
tar xvf asdtools.tar.xz
```

![image-20240701203710142](https://github.com/huntingsec/asdtools/image-20240701203710142.png)

进入目录，添加安装脚本执行权限

```
cd asdtools
chmod +x install.sh
```

![image-20240701203922578](https://github.com/huntingsec/asdtools/image-20240701203922578.png)

以root权限安装

```
sudo ./install.sh
```

![image-20240701204031463](https://github.com/huntingsec/asdtools/image-20240701204031463.png)

这是为了修改用户的执行权限

![image-20240701204153909](https://github.com/huntingsec/asdtools/image-20240701204153909.png)

等待安装完成，输入asd进入菜单

![image-20240701204251185](https://github.com/huntingsec/asdtools/image-20240701204251185.png)

![image-20240701220611993](https://github.com/huntingsec/asdtools/image-20240701220611993.png)

可以用关键字进行选择，也可以鼠标滚轮，还可以双坤

![image-20240701220726971](https://github.com/huntingsec/asdtools/image-20240701220726971.png)

绝大部分是可以直接执行的，仅有一部分是需要交互的

比如设置代理需要先切换到root模式

![image-20240701221016833](https://github.com/huntingsec/asdtools/image-20240701221016833.png)

这里可以选择代理的协议，键入IP和端口

（PS：这里采用删掉最后一行然后再追加一行的方式配置代理，方便快捷，嘎嘎好用，在也不用vi /etc/proxychinas4.conf了）

![image-20240701221102460](https://github.com/huntingsec/asdtools/image-20240701221102460.png)

例子2：

log4j的工具使用

![image-20240701221353945](https://github.com/huntingsec/asdtools/image-20240701221353945.png)

可以输入要执行的命令，譬如ping dnslog.cn

![image-20240701221514766](https://github.com/huntingsec/asdtools/image-20240701221514766.png)

然后输入IP，这样能极大程度减少我们的操作量

![image-20240701221636819](https://github.com/huntingsec/asdtools/image-20240701221636819.png)

另外，在linux上执行二进制的pppscan或者tscanplus的时候会报错找不到libwebkit2gtk-4.0.so.37

这个解决方案我已经在脚本中进行修复了

不过大家也可以自行去解决，命令如下

```
sudo ln -sf /usr/lib/x86_64-linux-gnu/libwebkit2gtk-4.1.so.0 /usr/lib/x86_64-linux-gnu/libwebkit2gtk-4.0.so.37
sudo ln -sf /usr/lib/x86_64-linux-gnu/libjavascriptcoregtk-4.1.so.0 /usr/lib/x86_64-linux-gnu/libjavascriptcoregtk-4.0.so.18
```

其次为了方便系统和cms的定位，实现准确的打点，后面的版本会增加更详细的匹配规则以及bypass的命令，感谢大家的支持。







