# ASD工具箱（ASD圆你一个黑客梦）

> [!IMPORTANT]
>
> ```
> https://github.com/huntingsec/asdtools
> ```

> [!TIP]
>
> 天下武功，无坚不破，唯快不破

![logo](https://raw.githubusercontent.com/huntingsec/asdtools/main/logo.png)

#### 工具介绍

> [!TIP]
>
> 为了快速上手，快速打点而生（由此得名：键盘输入asd是最快的[肌肉记忆了]）
>
> 本项目，目前只集成了快速打点的GUI工具和一小部分命令行工具（为了不和GUI进行混淆，后面会将所有蓝队应急的命令，攻防的命令以及APT手法等单独集成到工具箱中的一个模块）。
>
> 收集于各位大佬们的精选工具，也是日常必备，使用率最高的几个工具。

#### 工具安装

![image-20240701203637270](https://github.com/huntingsec/asdtools/blob/main/image-20240701203637270.png?raw=true)

> [!TIP]
>
>  解压
>
> ```
> tar xvf asdtools.tar.xz
> ```

![image-20240701203710142](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701203710142.png)

> [!TIP]
>
> 进入目录，添加安装脚本执行权限
>
> ```
> cd asdtools
> chmod +x install.sh
> ```

![image-20240701203922578](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701203922578.png)

> [!TIP]
>
> 以root权限安装
>
> ```
> sudo ./install.sh
> ```

![image-20240701204031463](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701204031463.png)

> [!TIP]
>
> 这是为了修改用户的执行权限

![image-20240701204153909](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701204153909.png)

> [!TIP]
>
> 等待安装完成，输入asd进入菜单

![image-20240701204251185](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701204251185.png)

![image-20240701220611993](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701220611993.png)

> [!TIP]
>
> 可以用关键字进行选择，也可以鼠标滚轮，还可以双坤

![image-20240701220726971](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701220726971.png)

> [!TIP]
>
> 绝大部分是可以直接执行的，仅有一部分是需要交互的
>
> 比如设置代理需要先切换到root模式

![image-20240701221016833](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701221016833.png)

> [!TIP]
>
> 这里可以选择代理的协议，键入IP和端口
>
> （PS：这里采用删掉最后一行然后再追加一行的方式配置代理，方便快捷，嘎嘎好用，在也不用vi /etc/proxychinas4.conf了）

![image-20240701221102460](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701221102460.png)

> [!TIP]
>
> 例子2：
>
> log4j的工具使用

![image-20240701221353945](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701221353945.png)

> [!TIP]
>
> 可以输入要执行的命令，譬如ping dnslog.cn

![image-20240701221514766](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701221514766.png)

> [!TIP]
>
> 然后输入IP，这样能极大程度减少我们的操作量

![image-20240701221636819](https://raw.githubusercontent.com/huntingsec/asdtools/main/image-20240701221636819.png)

> [!TIP]
>
> 另外，在linux上执行二进制的pppscan或者tscanplus的时候会报错找不到libwebkit2gtk-4.0.so.37
>
> 这个解决方案我已经在脚本中进行修复了
>
> 不过大家也可以自行去解决，命令如下

> [!WARNING]
>
> ```
> sudo ln -sf /usr/lib/x86_64-linux-gnu/libwebkit2gtk-4.1.so.0 /usr/lib/x86_64-linux-gnu/libwebkit2gtk-4.0.so.37
> sudo ln -sf /usr/lib/x86_64-linux-gnu/libjavascriptcoregtk-4.1.so.0 /usr/lib/x86_64-linux-gnu/libjavascriptcoregtk-4.0.so.18
> ```

> [!TIP]
>
> 其次为了方便系统和cms的定位，实现准确的打点，后面的版本会增加更详细的匹配规则以及bypass的命令，感谢大家的支持。

#### 项目清单

| 名称                     | NAME                    | GITHUB                                                       |
| ------------------------ | ----------------------- | ------------------------------------------------------------ |
| 冰蝎                     | Behinder                | https://github.com/rebeyond/Behinder                         |
| 蚁剑                     | AntSword                | https://github.com/AntSwordProject/antSword<br/>https://github.com/AntSwordProject/AntSword-Loader |
| 哥斯拉                   | Z-Godzilla_ekp          | https://github.com/kong030813/Z-Godzilla_ekp                 |
| 哥斯拉suo5插件           | Godzilla-Suo5MemShell   | https://github.com/X1r0z/Godzilla-Suo5MemShell               |
| 天蝎                     | skyscorpion             | https://github.com/shack2/skyscorpion                        |
| Webshell免杀生成器       | Webshell_Generate       | https://github.com/cseroad/Webshell_Generate                 |
| 综合OA漏洞利用工具       | Exp-Tools               | https://github.com/cseroad/Exp-Tools                         |
| OA漏洞利用工具           | I-Wanna-Get-All         | https://github.com/R4gd0ll/I-Wanna-Get-All                   |
| 指纹管理扫描工具         | pppscan                 | https://github.com/zhensuibianwan/pppscan                    |
| 无影综合扫描工具         | TscanPlus               | https://github.com/TideSec/TscanPlus                         |
| DecryptTools综合解密工具 | DecryptTools            | https://github.com/wafinfo/DecryptTools                      |
| 大华定向利用工具         | dahuaExploitGUI         | https://github.com/MInggongK/dahuaExploitGUI                 |
| Nacos定向利用工具        | NacosExploitGUI         | https://github.com/charonlight/NacosExploitGUI               |
| Thinkphp定向利用工具     | ThinkphpGUI             | https://github.com/nex121/ThinkphpGUI                        |
| 若依定向利用工具         | ruoyiVuln               | https://mp.weixin.qq.com/s/HU1OqZ7YFGjfc4HE3M8tPA            |
| Shiro定向利用工具        | ShiroAttack2            | https://github.com/SummerSec/ShiroAttack2                    |
| Strusts2定向利用工具     | Struts2VulsScanTools    | https://github.com/abc123info/Struts2VulsScanTools           |
| Weblogic定向利用工具     | WeblogicTool            | https://github.com/KimJun1010/WeblogicTool                   |
| SmartBI定向利用工具      | SmartBIAttackTool       | https://github.com/yggo/SmartBIAttackTool                    |
| Spring定向利用工具       | SpringExploitGUI        | https://github.com/charonlight/SpringExploitGUI              |
| 帆软定向利用工具         | FrchannelPlus           | https://github.com/BambiZombie/FrchannelPlus                 |
| 用友NC定向利用工具       | NCTOOls                 | https://github.com/wafinfo/NCTOOls                           |
| Dockerapi未授权利用工具  | DockerApi-Rce           | https://mp.weixin.qq.com/s/gjD7SVFqjkusmLjhxJ_tDQ            |
| Jenkins定向利用工具      | JenkinsExploit-GUI      | https://github.com/TheBeastofwar/JenkinsExploit-GUI          |
| 蓝队分析工具箱           | BlueTeamTools           | https://github.com/abc123info/BlueTeamTools                  |
| Java 内存马生成工具      | java-memshell-generator | https://github.com/pen4uin/java-memshell-generator           |
| HeapDump敏感信息提取工具 | JDumpSpider             | https://github.com/whwlsfb/JDumpSpider                       |
| JNDI注入漏洞利用工具     | JNDI-Injection-Exploit  | https://github.com/welk1n/JNDI-Injection-Exploit             |
| JNDI注入漏洞利用工具2    | JNDIExploit-1           | https://github.com/Jeromeyoung/JNDIExploit-1                 |
| Suo5-GUI正向代理工具     | suo5                    | https://github.com/zema1/suo5                                |

### 功能模块列表

> [!NOTE]
>
> GUI工具(侧重常用GUI图形化)✔️
>
> 攻防模式(侧重常用攻防命令集)❌
>
> 内网模式(侧重内网横向及bypass)❌
>
> APT模式(侧重痕迹隐藏及后门)❌

> [!CAUTION]
>
> 大家有什么意见或者建议可以添加好友进群反馈（PS：如果有大佬想深入交流或者合作，可以进群添加群主私聊）
>
> ![team](https://raw.githubusercontent.com/huntingsec/ARL-Limited-Edition/main/link.jpg)



## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=huntingsec/asdtools&type=Date)](https://star-history.com/#huntingsec/asdtools&Date)





