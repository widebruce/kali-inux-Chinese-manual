# <font color= #C70036>Kali Linux 中文技术手册</font>

## 零章· 序言

- 阅读这本手册是一种很好的探索 Linux 的方式。本手册以快速上手，实用为主。不过多的赘述理论，除非它必须被提起。你可以在 GitHub上 获取它的原始文档。推荐把它当成一个索引，尝试去修改完善当中的内容。使它成为你知识的扩展。

- 如何学习：持之以恒，积少成多。上手操作，熟能生巧。

- 本文档以 FAQ 的形式展开，问答之间，环环相扣。

## 章一· 跑起来

- <font color= #C70036 >什么是 Linux？</font>

    - 计算机操作系统的一种，如大家熟悉的 Windows，Mac OS 等都是。

    - 严格意义上说，Linux 只是一个内核，是处于硬件与应用程序之间的核心软件。“Linux 发行版”是一个完整的操作系统；它通常包括 Linux 内核，安装程序，最重要的是，包含将计算机变成真正有用的工具所需的应用程序和其他软件。

    - 通常我们习惯把 Linux 系统，称呼为 Linux。

- <font color= #C70036> Linux 与 Windows 的区别？</font>

    - 易用性：Windows 中大部分软件的安装和使用都在图形界面中完成。而 Linux 及运行在其之上的软件只有部分支持图形界面，但情况正在逐渐改善。

    - 软件支持：大多数 Windows 中运行的软件都在 Linux 中也有对应的版本。但是还有部分软件以及游戏厂商只提供了 Windows 版本的应用。而在 Linux 中，也有部分专业软件是在 Windows 中所不支持的。虽然有方式使不同系统之间的程序互通，但都会以牺牲性能为代价。

    - 应用场景：Windows 在个人电脑中广泛使用，Linux 在服务器中大量使用。

    - 开源与非开源：Linux 源代码开放，任何人都可以出于任何目的贡献，修改，增强和分发代码。更自由，可在网上免费下载和使用。Windows 需要购买许可证，无法修改其源代码。

- <font color= #C70036>为什么要学习Linux？</font>

    - 在学习 Linux 的过程中可以更深入理解计算机的操作系统，组成原理，网络基础等。

- <font color= #C70036>如何选择Linux版本？</font>

    - Windows 有 Windows xp，Windows 7，Windows 10 等版本，各个版本中又分为家庭版，专业版，企业版等。也有运行在服务器上的版本，如 Windows serve 2008，Windows serve 2012等。

    - Linux 也有许多的版本，它主要分为 Redhat，和 Debian 两个阵营。Redhat 技术支持可靠、更新及时。Debian 精简稳定。还有基于这两个版本的其他发行版。比较知名的有基于 Redhat 的 Cent OS，以及基于 Debian 的 Ubuntu。还有渐渐被人熟知的 Kali。Cent OS 完美了的继承了 Redhat 的优点。Ubuntu 为个人 PC 做了优化，有着丰富的资源库和领先的图形界面设计。而 Kali 面向各种信息安全任务，如渗透测试、安全研究、计算机取证和逆向工程等。

    - Linux 有着很高的自由度，甚至可以定制专属于你的 Linux。

    - 本手册中使用 Kali Linux ，虽然 Linux 有众多发行版，但本质上它们都是 Linux，只要学习一种，对于其它的发行版都触类旁通。

- <font color= #C70036>如何开始？</font>

    - 第一步，需要准备一台电脑，真实的物理机。然后需要再电脑中安装一个虚拟机软件。

    - <font color= #C83C32>什么是虚拟机软件？</font>

        - 虚拟机(英文全称：Virtual Machine)是指通过软件模拟的具有完整硬件系统功能的、运行在一个完全隔离环境中的完整计算机系统。目前主流的有 VMware Workstation，VirtualBox 等。

    - <font color= #C83C32>为什么不直接在物理机直接安装 Kali？</font>

        - 使用习惯：Windows 在个人 PC 市场上流行，也许你的 PC 上运行的就是 ，突然切换到新的操作系统，会让你产生困惑。图形界面的差异化，软件的安装方式与操作方法的区别，会让你浅尝辄止。

        - 安装过程：多数电脑在你获取得时都预装了 Windows。而 Linux 需要你自己动手去安装配置。在 Linux 的安装过程中提供的选项，需要足够了解它们才能做出适合你设备的选择。Kali Linux 在其下载网址上提供了对应的适用于虚拟机的版本，只要需要下载，打开，就可以使用，省去了繁琐的安装过程。

        - Windows 中，系统管理员的权限是有限的，当你尝试修改或删除一个系统文件时，会弹出拒绝操作提示框。Linux 系统中的管理员，拥有无限权力，可以，读、写和删除系统上的任何文件。初次接触 Linux，可能会因误操作导致系统出错，使其无法正常运行。在虚拟机中可以很好规避这些问题（借助我们马上讲到的虚拟机的快照功能）。

    - <font color= #C83C32>如何获取虚拟机程序？</font>

        - VMware Workstation，功能丰富，性能优秀，需要收费，VirtualBox 体积小反应快，开源且免费，但支持和功能不如VMware。本手册以 VMware Workstation 为实例。前往 [VMware Workstation Pro 下载页面](https://www.vmware.com/cn/products/workstation-pro/workstation-pro-evaluation.html) 。

        - 选中 Workstation 16 Pro for Windows 点击立即下载。

        - 下载后双击 exe 文件进行安装。

        - 在安装向导中点击下一步开始安装

        - 选择《我接受许可协议中的条款》，点击下一步。

        - 确定安装位置，点击下一步。

        - 用户体验设置，这里取消勾选《加入VMware客户体验提升计划》，并点击下一步。

        - 选择需要创建快捷方式的位置，点击下一步。

        - 点击安装开始安装。

        - 关于许可证可从 Workstation 官网购买获取，或通过互联网等其他方式取得。

        - 点击完成完成安装。

    - <font color= #C83C32>如何获取 Kali 并在虚拟机中打开？</font>
        - 前往 [kali 下载页面](https://www.kali.org/get-kali/)。

        - 选择 Virtual Machines 虚拟技术（Virtual Machines）。

        - 选择 VM 版本，这里我们选择 64-bit VMware，点击左侧下载按钮进行下载。
     
        - 选中下载文件，解压缩。

        - kali 系统运行环境准备完毕。

    - 如何操作虚拟机？

        - 打开 kali 系统文件，首先打开 VMware Workstation 软件，在主页中，点击打开虚拟机。选中解压后的虚拟机文件，点击打开。这时会在左侧库中与右侧选项卡中显示 kali 虚拟系统。

        - 生成快照，方便在系统运行异常时快速恢复之前备份的状态，系统快照可生成多个节点。并且推荐对计算机进行不确定实验性功能改动时进行快照操作。在顶部菜单栏中选择虚拟机(M)->快照(N)->拍摄快照。输入快照名称，因为初次打开 kali 虚拟机文件，并未对系统做出任何改变，这里设置快照名称为《初始》。最后点击拍摄快照(T)。

        - 恢复快照，选择顶部菜单栏中的虚拟机(M)->快照(N)->恢复到快照(R):初始。或者打开快照管理器(Ctrl+ M)进行快照操作。

        - 启动 kali 时，点击右侧打开的 kali linux 选项卡中的，开启此虚拟机。

        - 将鼠标点入打开的虚拟机窗口，进入 kali linux 系统。 

- <font color= #C70036>如何登陆？</font>

    - 系统启动后，会显示一个图形的登陆界面。在  Kali 的 VM 版本中，默认用户名和密码都是kali，在登陆栏中输入后即可登录。使用 Tab 键（跳格键）可以在用户名和密码之间移动，也可以使用鼠标主要键点击。输入完成后点击 Log In 或者按下回车键，进入该用户的图形界面。

- <font color= #C70036>什么是图形界面？</font>

    - 图形用户界面（Graphical User Interface，简称 GUI，又称图形用户接口）是指采用图形方式显示的计算机操作用户界面。Kali 默认安装了GUN环境。

    - 与 Windows 不同的是 Kali Linux 的菜单栏和任务栏都集中到了图形界面的上方。这点与 Mac OS 类似。

- <font color= #C70036>什么是命令行界面？</font>

    - 命令行界面（command-line interface，简称 CLI）”，它是一种字符界面交互环境，通过输入对应的命令对计算机进行相应的操作。
    
    - 系统启动之后，能够用 Ctrl-Alt-F1-F6 进入基于字符的登录提示符，同时你能通过 Ctrl-Alt-F7 回到图形环境。
    
    - 启动命令行环境后，会显示一个字符登陆提示符。输入用户名密码按回车登陆，登陆后进入一个 shell 提示符（命令提示符）。

- <font color= #C70036>什么是 shell 提示符？</font>

    - Shell 提示符是对计算机下达各种指令，操作计算机的一个字符窗口。

    - 要在图形环境下获得 shell 提示符，必须在登陆系统后启动一个 x 终端模拟器程序，菜单栏上的第三个，或者右击桌面屏幕在弹出的菜单中选择Open Terminal Here。

    - 要在命令行环境下获得 shell 提示符，需在登录提示符下，输入你的用户名，例如 kali，然后按回车键，再输入你的密码并再次按回车键。登陆到普通用户 kali 的 shell 提示符。

- <font color= #C70036>什么是普通用户？</font>

    - 普通用户，有限的权利，默认情况下只能够在自己的主目录内进行增删改查等操作。一个文件的权限可能会导致非 root 用户无法使用或访问它。

- <font color= #C70036>什么是root账户？</font>

    - root 账户也被称作超级用户或特权用户。用这个账户，你能够履行系统管理任务。读、写和删除系统上的任何文件，不顾它们的文件权限。设置系统上任何文件的所有者和权限。设置系统上任何非特权用户的密码。免用户密码登录任何帐户。

    - 无限权力的 root 账户，要求你慎重和负责任的使用。千万不要和其他人共享 root 密码。

- <font color= #C70036>普通用户如何拥有特权用户的权利？</font>

    - 对于典型的单用户工作站，例如运行在笔记本电脑上的桌面 kali 系统，通常简单地配置 sudo来使为非特权用户（例如用户 kali）只需输入用户密码而非 root 密码就能获得管理员权限。kali Linux 中的 kali 用户默认情况下已配置。

    - 在多用户工作站中不要建立这样的普通用户账户，因为它会导致非常严重的系统安全问题。（ 为了对受限的设备和文件提供访问权限，你应该考虑使用组来提供受限访问，而不是通过sudo来使用 root 权限。）上述例子中，用户 kali 的密码及账号要有和 root 账号密码同样多的保护。管理员权限应该被赋予那些有权有能力对工作站进行系统管理任务的人。

    - 随着越来越细致周密的配置，sudo 可以授予一个共享系统上的其它用户有限的管理权限而不共享 root 密码。这可以帮助对有多个管理员的主机进行责任追究，你可以了解到是谁做什么。另一方面，你可能不想任何人有这样的权限。


- <font color= #C70036>如何进入 root shell 提示符？</font>

    - 在字符界面的登录提示符，键入 root 作为用户名密码登录。

    - 在任意用户的 shell 提示符下输入“su”。这会保存当前用户的一些环境设定。

    - 在任意用户的 shell 提示符下输入“su -l”。这不会保存当前用户的环境设定。

    - 在任意用户的 shell 提示符下输入“sudo -i”

- <font color= #C70036>如何为文件管理器获取 root 权限？</font>

    - 打开终端输入 `sudo thunar` 打开获取root权限的文件管理器。

- <font color= #C70036>如何安装软件？</font>

    - Windows 软件的安装，在互联网上下载对应的后缀名为 exe 的安装包，双击打开安装。而 kali Linux 是基于 Debian 的，所以需要下载支持 Debian 系统的安装包。其后缀名为 deb ，然后使用 dpkg 进行安装。

    - “ dpkg ” 是“ Debian Packager ” 的简写。是 “ Debian ” 专门开发的套件管理系统，方便软件的安装、更新及移除。需要在终端中进行。

        - 安装：`dpkg -i <package.deb>`
        - 卸载：`dpkg -r <package>`
        - 查询：`dpkg -l | grep 'package'` # 查看已安装的包
        - 配置：使用 `dpkg-reconfigure package` 来对已安装的软件进行配置。# 本地化语言设置 `dpkg-reconfigure locales`; # 设置时区 `dpkg-reconfigure tzdata`;
    
    - <font color= #C83C32>如何设置系统语言环境为中文？</font>
        - 官网提供的 VM 版本的 Kali 系统，默认语言环境为英文，只需要简单的几步操作，就可以将其修改为中文。

        - 打开终端模拟器，输入 `sudo dpkg-reconfigure locales`;

        - 下翻找到 zh_CN.UTF-8 UTF-8 单击空格键选择，使用 Tab 键切换选项，选择Ok，按回车确定。重启后生效。

        - 启动后，包括登陆界面，都以中文的形式展现，登陆后会询问，将标准文件夹更新到标准语言吗？建议选择保留旧的名称，旧的英文名称并勾选，不要再次询问我。在我们学习Linux 命令时方便切换目录时直接输入对应的单词，而不用再切换中文输入法。

    - <font color= #C83C32>如何下载安装 edge 浏览器。</font>

        - Microsoft Edge 基于 Chromium，并进行了优化，使其发挥最佳性能。有着丰富的附加组件，以及对中国用户有着良好的支持。

        - 前往 edge 浏览器[官网下载页面](https://www.microsoft.com/zh-cn/edge?form=MA13FJ#evergreen)，点击下载，选择保存文件（Save File）。

        - 打开下载目录，单点鼠标右键，选择在这里打开终端。然后在shell提示符中输入 `sudo dekg -i microsoft-edge-stable_107.0.1418.35-1_amd64.deb`; 再输入用户 kali 的密码进行安装。

        - 这里有个小技巧，在输入命令和文件目录名称时可以使用 Tab 键补全，这里 edge 的文件名称很长，你只需要在输入文件名时输入前几个字母，然后按下 Tab 键，文件名就会自动补全。

    - <font color= #C83C32>如何下载安装 wps 办公软件。</font>

        - 前往 [wps for linux](https://www.wps.cn/product/wpslinux#) 下载页面，点击立即下载，选中 For X64 开始下载。

        - 打开下载目录，单点鼠标右键，选择在这里打开终端。然后在shell提示符中输入 `sudo dekg -i wps-office_11.1.0.11664_amd64.deb`; 再输入用户 kali 的密码进行安装。

        - 打开 wps 可能会提示缺少系统字体，你可以在互联网上下载这些字体文件，把它们复制到 usr->share->fonts->truetype->wps-office目录下。需要获取root权限的文件管理器才可以执行该操作。打开终端输入`sudo thunar`;

    - <font color= #C83C32>如何下载安装 xmind 思维导图软件。</font>

        - 前往 [xmind for linux](https://xmind.cn/download/) 下载页面，找到 Linux ，选择 deb 64位下载。

        - 打开下载目录，单点鼠标右键，选择在这里打开终端。然后在shell提示符中输入 `sudo dpkg -i Xmind-for-Linux-amd64bit-22.10.0632.deb`; 再输入用户 kali 的密码进行安装。

    - <font color= #C83C32>如何使用另外一种安装方式 apt。</font>

        - 通过APT，软件包可以从系统中添加或移除，命令分别为：apt install 软件包（安装） apt remove 软件包（删除） apt purge 软件包（不保留配置删除）

        - 在软件包中的文件发生移除或更改时，系统有时候可能会受损。恢复这些文件最简单的方法是重新安装受影响的软件包。不幸的是，包管理系统会认为后者已安装而拒绝重新安装；为了避免此情况，使用和命令的选项。如下命令会重新安装postfix，即使它已存在：`sudo apt --reinstall install postfix`; 

    - <font color= #C83C32>如何安装中文输入法</font>

        - 打开终端输入 `apt install fcitx fcitx-googlepinyin -y`; 

        - 使用 ctrl + space 切换输入法。

    - <font color= #C83C32>如何在 Linux 上安装 Windows 上常用的软件。</font>

        - 打开终端输入 `sudo wget -O- https://deepin-wine.i-m.dev/setup.sh | sh`; 按下回车。

        - 现在可以试试安装更新deepin-wine软件了，如：
        <br>微信：`sudo apt install com.qq.weixin.deepin`   <br>QQ：`sudo apt install com.qq.im.deepin`
        <br>TIM `sudo apt install com.qq.office.deepin`
        <br>钉钉：`sudo apt install com.dingtalk.deepin`
        <br>完整列表见 https://deepin-wine.i-m.dev/    

        - 安装微信：打开终端输入 `sudo apt install com.qq.weixin.deepin`；

        - 添加微信程序这些文件到应用程序目录(应用程序默认安装在/opt/apps下)执行
        <br>打开文件管理器，选择左边栏的文件系统。前往 opt->apps->com.qq.weixin.deepin->entries->applications 右键打开终端输入 `sudo thunar` 新建一个取得 root 权限的文件管理器，点击右键选择复制，进入 usr->share->applications 目录下 右击粘贴;

        - 添加桌面快捷方式
        <br> 点击应用程序图标，搜索微信，右键选择编辑应用程序，点击图标，选择上侧的，从此次选择图标，在弹出的选项卡中选择图片文件，找到安装目录，去到 entries/icons/hicolor/64x64/apps 选择图片文件点击确定并保存。在次打开应用程序图标，搜索微信，右键选择发送到桌面。

