[toc]

## windows 常用快捷键

- `Ctrl+R`：打开运行窗口
- `Alt+Tab`：切换窗口
- `Win+X`：打开 Windows 移动中心（可开关无线网络、调节音量、显示器亮度等）
- `Win+D`：回到桌面
- 进入目录，按住 `Shift` 键，再鼠标右键 --> 「在此处打开命令窗口」
- `Win+E`：打开「计算机」
- `Ctrl+W`：关闭窗口（浏览器下也可用。浏览器下新开窗口：`Ctrl+T`）
- `Ctrl+P`：关于与投影仪的连接（断开、复制、扩展、仅投影仪）
- `Win+L`：锁屏

### Win10

- `Win+Tab`：打开任务视图。



### 惠普笔记本锁定和取消 Fn 键：`Shift+fn`

### ThinkPad 系列电脑Fn、Ctrl切换及F1~F12等功能键切换方法

联想 ThinkPad 系列的笔记本电脑不知道从什么时候开始把键盘最上面一行的功能键设置为默认功能，而其上面的 F1~F12 功能需要通过 Fn+F1~F12 来实现，这对于用一些软件的快捷功能非常不方便。如果需要改为直接按 F1~F12 即实现相应的功能，而其它调节音量、屏幕亮度等则通过按 Fn+ 相应的功能键来实现，可采用如下方法：

**一、通过进入BIOS来实现**

1、开机出现Thinkpad的LOGO字样时，按下F1键，进入BIOS；

2、找到CONFIG-->Keyboard/Mouse-->Change to "f1-f12 keys”,按回车更改为Legacy；

3、然后保存退出（按F10或Fn+F10）。

**二、直接在键盘上切换**

1、按键盘上的Fn+Esc来锁定Fn功能，此时Fn上的指示灯亮。这时F1~F12为F键功能，若想用调节音量、屏幕亮度的功能，则需要按Fn+相应的功能键；

2、再次按键盘上的Fn+Esc来解锁Fn功能，此时Fn上的指示灯熄灭。这时要调节音频、屏幕亮度等功能，直接按相应的键；若要用F1~F12，则需要通过按Fn+F1~F12来实现。

这种方法更好一些，方便切换，无需重启系统。

**三、Fn和Ctrl键切换**

键盘上的Fn键设置在左下角，Ctrl在Fn的右边，这对于经常使用Ctrl+c和Ctrl+v非常不方便，容易按错。若需要切换两键的位置，可以在BIOS里进行设置，方法如下：

1、开机出现Thinkpad的LOGO字样时，按下F1键，进入BIOS；

2、找到找到CONFIG-->Keyboard/Mouse--> Fn and Ctrl Key Swap，按回车更改为”Enabled“；

3、然后保存退出（按F10或Fn+F10，根据是否锁定Fn功能）。

——from：[ThinkPad系列电脑Fn、Ctrl切换及F1~F12等功能键切换方法](<http://blog.sina.com.cn/s/blog_47569d460102w8r1.html>)



## windows cmd 命令

- `regedit`：打开注册表
- `netstat -ano`：列出所有端口的情况。
  - 若端口占用，可以先在列表中我们观察被占用的端口
- `mstsc`：打开远程桌面连接
- `calc`：打开计算器
- `cls`：清除窗口信息
- `systeminfo`：查看系统的详细状态，除了基本系统信息，还可以查看系统补丁及网络信息和 CPU 主板等信息
- `shutdown -s -t 30`：电脑倒计时，将会在 30 秒后关机
- `msconfig`：是 Microsoft System Configuration 的缩写。在开始菜单里运行中输入然后确认就可以找到程序开启或者禁用，可以帮助电脑禁止不需要运行的程序，这样可以加快你的电脑运行。
- 



## windows 使用技巧

### Windows 常见设置？

(1) 在 Windows 文件管理器中，输入`%APPDATA%`,回车，进入电脑`...\AppData\Roaming`目录。

(2) 设置 Windows 软件开机自启：
1. 打开路径`C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup`，即打开`程序——>启动`，或者 CMD 下运行：`shell:startup`打开；
2. 将需要开机自动启动的软件的快捷方式粘贴到“系统启动文件夹”里。

(3) Win7 怎么关闭自动锁屏？

1. 控件面板--网络和INTERNET--网络和共享中心--更改适配器设置--本地连接（右击）--属性--配置--电源管理
   把关闭此电源已节约电的勾去掉，这样就可以解除锁定计算机，避免出现锁定后断网的现象。
2. 开始 –> 控制面板 –> 电源选项  –> 更改计划设置 –> 使计算机进入睡眠状态，设成从不 –> 保存修改 
3. 右击桌面 –> 个性化 –> 屏幕保护程序 –> 设置等待时间长一点或者屏幕保护程序为无就行了
4. 不行的话，屏幕保护程序下面那里有一个更改电源设置。打开之后按照以下的设置。单击更改计算机的睡眠时间，关闭显示器和使计算机进入睡眠状态都设置为从不。

### Win7图标丢失和不正常显示的修复方法

根据参考文章 [1] 来修复桌面白图标方法是打开记事本，复制以下内容：

``` markdown
@echo off
taskkill /f /im explorer.exe
CD /d %userprofile%\AppData\Local
DEL IconCache.db /a
start explorer.exe
cho 执行完成
```

保存为后缀 `.bat` 格式文件，然后运行该 bat 文件即可。若运行完成之后出现黑屏，这种正常情况，部分会因重启 `explorer.exe` 失败而不显示内容，所以黑屏，只要在任务管理器中重新加载 `explorer.exe` 即可，或者直接重启电脑即可，不影响解决问题及系统安全。

根据参考文章 [2] 方法步骤如下：

1. 打开任务管理器（任务栏右键，启动任务管理器），结束正在运行的 `explorer.exe` 进程（explorer 是桌面进程，关闭后，你会发现你的桌面没有了，不要紧，解决问题需要）

2. 点击新任务，在打开空格内输入“CMD”，依次执行以下命令：

   ``` markdown
   CD /d %userprofile%\AppData\Local（回车）
   DEL IconCache.db /a（回车）
   exit（回车）
   ```

   然后重新运行 `explorer.exe`（点击任务管理器的“文件” –> 新建任务“运行”，输入explorer 即可）。

   原理：`IconCache.db` 文件为图标属性文件，由于某种操作，导致文件损坏，删除后，系统会自动重建。然后图标就会恢复正常了。

参考文章：

- \[1] [修复桌面白图标方法，图标有白色的方块怎么办_百度经验](https://jingyan.baidu.com/article/c85b7a64568aac003bac952d.html)
- \[2] [关于Win7图标丢失、不正常显示的修复方法](https://www.cnblogs.com/luckly-hf/p/5135516.html)

### 两台电脑如何连接？

#### 1. windows 访问远程共享(包括连接其他电脑的共享打印机)

Windows 下，`Ctrl+R`，输入 `\\192.168.x.x` 即可访问局域网的远程共享文件，包括局域网其他电脑的共享打印机。

- 连接局域网其他电脑共享的打印机设置：[如何连接其他电脑共享的打印机_百度经验](<https://jingyan.baidu.com/article/f54ae2fcd41fb41e92b849f9.html>)

其他命令：

- `net use`：可看到当前所有的远程访问记录
- `net use * /d`：删除所有访问记录，提示是否删除时，输入y

#### 2. windows “远程桌面 mstsc” 连接局域网其他电脑

`Ctrl+R` 或 `Win` 键，输入`mstsc` 打开“远程桌面”，输入 ip 地址连接即可，前提被连接电脑已设置允许连接。

#### 3. 使用软件远程连接，如 Teamviewer

### 如何正确的修改administrator用户名？

在“运行”里面输入“gpedit.msc”就打开了组策略 -> 计算机配置 -> Windows 设置 -> 安全设置 -> 本地策略 -> 安全选项 -> 账户：重命名系统管理员账户

参考来源：[如何正确的修改administrator用户名-百度经验](https://jingyan.baidu.com/article/4dc408488b2187c8d946f1b2.html)



### 如何查看局域网ip被占用？

windows键＋R键，打开cmd

输入：`arp -a`，回车（“arp”与“-a”之间有空格）

显示如下：

![](https://img-1256179949.cos.ap-shanghai.myqcloud.com/20190622162929.png)

——from：[查看公司内网 IP 占用情况](https://blog.csdn.net/Snow_loveLife/article/details/79290752)



### 如何更改电脑自动获取的局域网IP地址？

打开“运行”，打开 CMD 窗口，输入 ipconfig，查看本地 ip 地址、子网掩码、默认网关信息。

![](https://img-1256179949.cos.ap-shanghai.myqcloud.com/20190622163303.png)

然后进入 IPV4 协议修改为填写的即可。

![](https://img-1256179949.cos.ap-shanghai.myqcloud.com/20190622163401.png)

参考来源：https://www.pc841.com/Win10/201509-54222_all.html

### DNS 服务器地址 8.8.8.8 和 8.8.4.4 是？

8.8.8.8 是一个 IP 地址，是 Google 提供的免费 DNS 服务器的 IP 地址，Google 提供的另外一个免费 DNS 服务器的 IP 地址是：8.8.4.4 。用户可以使用 Google 提供的 DNS 服务器上网。 

2009 年 12 月 04 日 Google 给了我们一个惊喜，并沉重的打击了 OpenDNS。他们宣布向所有的互联网用户提供一组快速，安全并且完全免费的 DNS 解析服务器，地址分别是：主 8.8.8.8，备 8.8.4.4。

——from：[8.8.8.8_百度百科](https://baike.baidu.com/item/8.8.8.8)

### 外接显示屏，显示“输入信号超出范围”，如何解决？

Win10 下的解决，参考：[WIN10强制去除“输入信号超出范围”](<https://blog.csdn.net/w_j_r/article/details/81142929>)

> 注意：要点击到你想要更改的显示屏。

Win7 下的解决，参考：[强制去除'输入信号超出范围 调整为1600*900@60HZ'](<https://blog.csdn.net/Wbiokr/article/details/60479642>)



### 端口被占用 1080

每次电脑开机都提示 ShadowsocksR 端口 1080 被占用，查了下，被有道词典占用了端口。解决办法：

1、杀掉有道词典进程

1. 打开 cmd，输入：

   ``` xml
   netstat -aon|findstr "1080"
   ```

   找出被占用的进程。其中，最后一列就是 PID，比如 4568，记住该 PID。

   若要想知道此 PID 对应什么程序，可以继续输入：

   ``` xml
   tasklist|findstr "4568"
   ```

   可以看到程序名称。

2. 打开任务管理器，根据 PID 或者进程名称找到该程序，右键选择“结束进程”。

2、修改其中某个程序的端口

右键 ShadowsocksR --> 选项设置 --> 本地端口，修改为其他端口，如 1081。

3、修改注册表

关于端口占用这个问题，还可能碰到一种情况，比如系统 80 端口被 System 占用。解决办法：

> 安装了 Windows10 系统后，如果装 Apache 是启动不了的，遇到这个 Apache 启动不了的时候，首先是查看 80 端口是不是被占用。
>
> 运行 `netstat -aon | findstr :80` ，发现 pid 是 4 的进程占用着 80 端口，这还是一个系统进程，kill 不掉。所以只能另想办法：
>
> 1、打开注册表：regedit
>
> 2、找到：HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\services\HTTP
>
> 3、在右边找到 Start 这一项，将其改为 0
>
> 4、重启系统，System 进程不会占用 80 端口
>
> 重启之后，再启动 Apache 就可以了。
>
> ——from：<https://blog.csdn.net/heshi_yao/article/details/50755886>



---

---



## Win10 安装新版终端

开源地址：<https://github.com/microsoft/terminal>

Win 10 上安装教程：[Windows Terminal微软新版终端工具安装教程（附配置文件）](https://baiyue.one/archives/484.html)  |  视频：[第45期 Windows Terminal微软新版终端工具安装教程](<https://www.bilibili.com/video/av51726432/>) （实际：我在使用win10最新版专业版系统上不能成功安装。）

[win10超级终端在哪怎么用，附Windows Terminal下载](http://pc.poppur.com/taishiji/9095.html)

> 自微软发布Win95操作系统，它就打算用视窗界面来取代Dos状态下繁琐的命令行操作，让电脑（结合操作系统）更容易被普通用户上手和使用。然而当时有很大一部分电脑用户（从业者）是从MS DOS升级上来的，为了避免他们的不适应，微软还是于Windows里内置了一款终端（命令行执行软件）。之后windows又进化了好多个版本，对于第一版就使用Win7的90后来说，有多少平常使用windows的用户会使用生涩难懂的命令行操作呢，于是在win7之后，微软取消了内置在windows里的超级终端（命令行执行）程序。
>
> 对于普通电脑用家来说，这一点问题都没有，可对于程序员或者网站运维来说，这就非常不方便了，他们很多人只能无奈地安装putty或者是SecureCRT这样的远程终端软件。为什么那么多搞设计和程序开发的人会购买苹果电脑，就是因为MacOS是基于Linux系统，天生基因与命令行代码相近，同时MacOS自 Terminal（终端程序，命令行执行界面），打开这软件后就感觉是在Linux上直接操作，这就使得程序员在生产环境中非常倾向于使用苹果电脑。而先有鸡，还是先有蛋的问题微软在苹果App Store发展到如火如荼的今天也是终于意识到了，自他们收购了程序员大本营GitHub后，Windows也向程序员们抛出了橄榄枝，发布了由微软官方打造的win10超级终端程序 - Windows Terminal。

截止到 2019-06-25，可以到 win10 应用商店可以下载到该终端，名称为：`Windows Terminal(Preview)`。

### Win10 PowerShell简介？

参考：[强大到没朋友，Win10 PowerShell简介](<https://www.ithome.com/html/win10/315277.htm>)



## Win10 操作

### 1. win10系统怎么关闭自动更新

键盘的 win+R ，输入：`services.msc`，在弹出来的服务中，找到“Windows Update”，找到后双击，在启动类型处·选择“禁用”然后点击应用。

最后自动更新已关闭，可以去自动更新那看看，路径如图所示，点击更新后是不会更新的。

——from：https://jingyan.baidu.com/article/5225f26b620438e6fa09080c.html

### 2. win10如何打开控制面板？如何卸载软件？

**如何打开Win10控制面板？**

1，方法一：使用 Win + X 快捷键，或者鼠标放在开始菜单，点击右键，就可以看到一个菜单窗口，而后选择“控制面板”即可。

2，方法二：点击任务栏的搜索图标，或者在开始菜单中的搜索框中输入“控制面板”，即可看到“控制面板”程序，点击即可。

3，方法三：通过“运行”功能找到控制面板；点击 Ctrl + R，调出“运行”对话框，输入”Control”，点击确定，即可打开控制面板。

**如何卸载软件？**

方法一：如上方法打开控制面板，然后选择程序下的“卸载程序”。

方法二：键盘的 win+R ，输入：`appwiz.cpl` 打开卸载程序列表。



### 3. 设置 Win10 语言栏停靠在系统托盘最左边

**解决方法：**

1. WIN键+x > 控制面板 > 时钟、语言和区域 > 语言 > 高级设置

2. 选中“使用桌面语言栏”，在后面的“选项”中，把语言栏移到系统盘左侧，选择“停靠于任务栏”

——from：<https://zww.me/win10-language-bar-problem.z-turn>



### 4. win10 快速启动原理以及如何关闭

以往如 Windows 7 关机的时候会将用户会话和系统内核会话同时关闭掉，但在 Windows 8 开始的操作系统中新增加了一个“混合启动”（Hybrid Boot）新功能，其原理是**关机的时候只关闭用户会话，而系统内核会话则转入休眠状态（保存到一个文件中，下次开机时直接从这个文件中写回内存），从而提高系统启动速度，而微软更是把这个“混合启动”功能默认替代了关机功能。**

**“睡眠”模式**

系统会将正在处理的数据保存到内存中，除内存以外的所有设备都停止供电，可以通过鼠标键盘等唤醒电脑，唤醒后的运行状态和睡眠之前一模一样，睡眠期间不可断电，断电的话内存上的所有数据全部丢失，只能重新开机。

**“休眠”模式**

内存中的所有数据都会存储到硬盘的特定空间内，按开机键开机电脑就会将硬盘里临时存储的内存数据恢复到内存里，恢复后的运行状态和休眠之前一模一样。休眠期间可以完全断电。

”**快速启动**“模式

相当于注销后休眠，只休眠内核，不会保存用户当前的数据。

快速启动的弊端：

1、更新补丁后，关机并不会重启内核，所以二者间有了冲突，导致现在更新动不动就自动重启，就是为了补丁生效（不自动重启的情况下，可能会造成某次重启时间过长，我碰到过3小时重启时间的。）

2、毕竟数据会写入硬盘，对于固态硬盘寿命来说有影响

3、对于部分程序来说，可能会出现运行异常的情况

正常情况下快速启动的优势并不明显，固态硬盘的话，相差在10秒内；机械硬盘可能会多点，相差也不超过30秒的。所以快速启动并不实用。

补充，——from：<http://www.aichunjing.com/xtjc/2018-10-24/9841.html>

> win10 快速启动的弊端一：一些应用程序可能在快速启动时会出bug……（这些一般是内核有驱动结果开发者可能忘记注册之类的，但现在除非已经停止维护的一些上古应用外最新版基本都修复了这些问题）
>
> win10 快速启动的弊端二：快速启动会在一定程度上消耗你的硬盘寿命，因为每次关机后都会往硬盘里写入大量数据。所以小编建议，如果你是固态硬盘的话，可以考虑关闭快速启动这个选项，毕竟固态硬盘有擦写次数限制，机械硬盘的话则可以考虑打开快速启动。

#### win10 关闭快速启动

Windows打开“任务管理器”，点开“性能”选项卡看运行时间，这个时间一般情况下只有在重启的时候才会重新计时。也就是说没有真正意义上的关过机。

**方法一、控制面板**

1、桌面左下角 windows 标志鼠标右击，然后打开“控制面板”

2、打开“硬件和声音” ，点击“更改电源按钮的功能”

3、点击“更改当前不可用的设置”（管理员权限），去掉“启用快速启动（推荐）”的勾，“保存修改”后就生效了。

**方法二、CMD命令**

1、使用管理员权限打开 CMD（开始菜单搜索 CMD，“命令提示符”右击，点击“以管理员身份运行”）

2、输入 `powercfg /h off` 关闭快速启动（`powercfg /h on` 开启快速启动）

▼▼▼关闭后看不到启用快速启动和休眠的复选框

这里有个小技巧：

> 点击关机按钮时按住 shift，此次关机就不使用快速启动，这是我很久以前从哪里看来的，不过现在找不到了。我实际检测了一下，的确如此，运行时间清零了。——注：个人已测试，没有用，2019.07.01。

参考：

- [Windows10快速启动原理和如何关闭 - 软件教程](<http://www.myxzy.com/post-211.html>)
- [Windows10 快速启动 - 知乎](<https://zhuanlan.zhihu.com/p/45590515>)

**怎么启动个干净的系统？**

有些用户担忧，每次都是休眠启动，如果系统出问题，我想要个一干二净的登陆环境怎么办？ 办法由两个：

A． 关机不要直接用关机选项，而是开启命令行窗口，输入 `shutdown /s /full / t 0`。

B． 不要关机，而是选择重启。重启不会用快速启动。

**如何缩小休眠文件 hiberfil.sys？**

休眠文件 hiberfil.sys 随着你的内存大小而设定，通常是你安装内存的 75% 大小。土豪用户引以为傲的大内存带来了大休眠文件，对寸土寸金的 SSD 来说就肉痛了。如果你仅仅想用快速启动而对休眠不感兴趣的话，用这个命令：`powercfg /h /type reduced`，可以节省大约一半的空间。

——from：[Windows快速启动背后的功臣：休眠 - 知乎](<https://zhuanlan.zhihu.com/p/28639474>)

### 5. win10 如何关闭触摸板？

Win+X -> 打开“设置” -> 打开“设备” -> 打开“触摸板”，选择关闭即可。

另外，如何设置插入鼠标禁用触控板，请参考：<https://blog.csdn.net/qq459080123/article/details/79036179>



### 6. win10 如何方便所在文件夹的cmd或powershell？

方法一：shift+右键，可以打开在该目录下的 powershell。

方法二：直接在所在文件夹最上面的路径处，输入 `cmd` 即可打开在该目录下的 cmd。



## This beta version of Typora is expired, please download and install a newer version. 解决方案

修改 Typora 相应注册表的权限：

1. 打开注册表：按Windows+R打开运行窗口，输入 regedit。
2. 进入路径计算机\HKEY_CURRENT_USER\SOFTWARE\Typora。
3. 在右键菜单选择权限，把各个用户的权限全部设置为 拒绝。
   



# 一些问题

## windows10怎样把edge浏览器放到桌面上？

桌面右键新建快捷方式，输入`%windir%\explorer.exe shell:::{4234d49b-0245-4df3-b780-3893943456e1}`，点击下一步完成，之后你会发现桌面出现一个名字为“explorer.exe”的文件夹图标，打开该文件夹，选中Microsoft Edge浏览器图标。鼠标右键点击图标出现菜单，选择创建快捷方式。之后就可以在桌面上找到Microsoft Edge浏览器的快捷方式。

参考：[windows10怎样把edge浏览器放到桌面上_百度知道](https://zhidao.baidu.com/question/1240050229741517299.html)



## Win7、Win10 以命令方式开启无线 wifi？

**自动以管理员身份运行 bat 文件：**

在 bat 文件最开始前输入如下：
``` 
@echo off
>nul 2>&1 "%SYSTEMROOT%\system32\cacls.exe" "%SYSTEMROOT%\system32\config\system"
if '%errorlevel%' NEQ '0' (
goto UACPrompt
) else ( goto gotAdmin )
:UACPrompt
echo Set UAC = CreateObject^("Shell.Application"^) > "%temp%\getadmin.vbs"
echo UAC.ShellExecute "%~s0", "", "", "runas", 1 >> "%temp%\getadmin.vbs"
"%temp%\getadmin.vbs"
exit /B
:gotAdmin
if exist "%temp%\getadmin.vbs" ( del "%temp%\getadmin.vbs" )
pushd "%CD%"
CD /D "%~dp0"
```
接下来接你写的批处理。参考：https://www.zhihu.com/question/34541107/answer/91159429

---

批处理文件 bat，如下方法试试：

- [Win7系统建立并开启Wifi热点的bat批处理](https://blog.csdn.net/u010487568/article/details/33729901)
- [不通过第三方软件，笔记本如何创建WIFI热点？-知乎](https://www.zhihu.com/question/48029520/answer/185470770)

但我在 win10 采用如上方法开启 wiif 却都是没成功，有看到提示“无法启动承载网络”。后使用 [猎豹免费wifi](http://wifi.liebao.cn/) 却可以成功开启。



---

*update：2019-07-15* 

