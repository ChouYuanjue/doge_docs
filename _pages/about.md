---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>
请持续关注本文档，一切指令以文档为准。

现在使用的QQ号：**2701384861**

# 简介
豆子 Doge依托于mirai框架， 采用协议为ANDROID_PHONE以及ANDROID_WATCH。

功能主要分成两大部分，依托于mirai-console (JVM)的新功能以及依托于mirai-native的由旧版移植的旧功能。目前二者数量基本持平。

初版豆子诞生于2020年3月30日，依托于CQP. 此后四个月内断断续续地进行更新，在此过程中作者收到了许多人善意的帮助和支持，顶峰时期豆子有百余名好友，加入30多个群聊。2020年8月2日，经历腾讯第二次qbot大屠杀，元气大伤，CQP框架倒闭。随后尝试转移至mirai，效果极不理想，作者当即删库跑路，初版豆子就此结束了短暂的一生。

时隔两年，作者在数学吧闲聊时发现还有人记得豆子，大为感动，恰巧那时刚与丽琪的作者fyr进行过关于tex功能的交流，于是重新萌生了写bot的想法。2022年7月25日，作者开始重新写bot，发现两年的时间给qbot的生态造成了极大的变化，花了相当的时间适应。作者目前使用的是mirai-console-2.12.0，仍然存在部分问题。7.27日出现大崩溃事件，7.28重新配置完毕并进行大更新，豆子正式重生。

感谢所有曾提供帮助的人，同样感谢所有时隔两年仍然记得当初那个问题百出的豆子的人。特别感谢fyr和他的丽琪，没有他们两版豆子都不会出现。

友情链接：

mirai主仓库：[mamoe/mirai](https://github.com/mamoe/mirai)

丽琪使用说明：[使用说明](http://liqisese.top:800/help/)

# 更新日志
2022-07-30 增加`/poem`功能块，增加`/ask`功能，重写`/run`功能块（但仍然不能用）

2022-07-29 第二次大崩溃事件（tx风控）

2022-07-28 恢复大部分旧版功能

2022-07-27 第一次大崩溃事件

2022-07-26 增添部分新功能

2022-07-25 开始配置bot。增添部分新功能

# 开发者

欢迎参与豆子的开发。请阅读mirai的开发文档：[mirai docs](https://docs.mirai.mamoe.net/). 豆子鼓励使用JVM或者mirai-api-http开发的功能，但不太建议使用mirai-native. 目前豆子之所以采用双协议就是为了防止mirai-native崩溃而导致整个bot的停运。

豆子的所有指令原则上都使用`/`开头，后面应该跟着功能的英文或缩写，如果有开发意愿请注意这点。

所有插件请尽量不要夹带私货并且在mcl2里在至少一个bot上成功运行，如果可以的话请连同源码、README和打包好的jar(JVM)或exe(api-http)一并发送给作者。以上是请求而不是要求，但仍然希望有意者自觉遵守。如果不方便调试，日后作者或许会再开一个mcl专门用来测试这类插件（mirai-api-http不必担心此问题）。

关于功能方面，我们不介意大小，倒不如说比起大功能我们更青睐小功能（当然是因为作者的服务器实在是太差啦）。任何一个你觉得有趣或有用的功能都可以pr。当然如果太小的话可以直接联系作者让作者写，但作者不能保证会完成你的请愿。

出于某些原因，作者可能一到两周才能调试一次bot，很可能不能及时回复或者干脆摆烂，非常抱歉。

如果看了以上这些不客气的要求仍然想参与开发，欢迎联系作者询问更多。让我们一起把豆子变得更好

# 什么？你不会用？
```
/docs
```
查看使用说明。你的几乎所有问题都可以在这里解决。请认真且严格地遵照指令，不要再问什么诸如为什么`/tex`不能用的问题（因为指令是`/tex render`）。
```
/ask <问题内容>
```
如果你发现本文档无法解决你的问题，请通过该指令提问。问题会被提交给作者并在本文档末的FAQ中解答。

# 加群/加好友
目前是自动通过所有申请，欢迎对bot进行推广。如果有不通过的请与作者联系，这可能是腾讯拦截导致的。

# 聊天
新版豆子目前没有智能聊天的功能。初版豆子的智能聊天词库来自图灵机器人api，现在已需要收费。由于聊天者不多所以暂时没有使用的打算。

# 运行代码 『/run』
已通过调用curl重写，但是由于作者不知道curl for Windows竟然这么难用（和Linux完全不是一个感觉），所以现在处于**基本不能用**的状态（只要带空格就不行）。以后会再次重写。

使用说明：
```
/run <语言> <程序内容>
```
例子：
```
/run python3 print ('Hello,World!')
```
# 科学计算 『/wa』
此功能使用的是WolframAlpha api，一个月调用额度是2000，如果发现数次发送该指令都无回应很可能是额度已用完。

使用说明：
```
/wa <表达式>
```
例子：
```
/wa integrate x^2 sin^3 x dx
```
# LaTeX渲染 『/tex』
支持tikz,tikz-cd,xy-pic,mhchem宏,不支持tcolorbox,physics,calc,unicode宏；
支持`\def`,`\newcommand`,`\renewcommand`进行定义，不支持`\raise`,`\kern`进行微调

使用说明：

*渲染公式*
```
/tex render
<TeX代码>
```
例子：
```
/tex render
A_{m,n} = \begin{pmatrix} a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\ a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\ \vdots  & \vdots  & \ddots & \vdots  \\ a_{m,1} & a_{m,2} & \cdots & a_{m,n} \end{pmatrix}
```
但是目前有可能出现错误（主要是画交换图），如果渲染结果不正常且经检查确认没有使用不支持的宏，请采用以下解决方案：

*渲染URL编码公式*
```
/tex urender
<经URL编码后的TeX代码<>
```
例子：
```
/tex urender
%5Cxymatrix%7B%0A%20%20A%20%5Car%5Br%5D%5Ef%20%5Car%5Bd%5D_g%20&%0A%20%20B%20%5Car%5Bd%5D%5E%7Bg'%7D%20%5C%5C%0A%20%20D%20%5Car%5Br%5D_%7Bf'%7D%20&%0A%20%20C%0A%7D
```
**注意**：对空格符的编码请编成%0A，不要编成+号。可使用该网站上的工具：https://www.matools.com/code-convert

*随机TeX公式图片*
```
/tex random
```
公式是从arXiv上爬取保存在本地的，数据库大约有十万张，可能会导致反应稍慢。这是把某次失败的机器学习的残留物拿来废物利用，不会对此功能进行变动。图片只能在电脑端正常查看。

# 奇怪的表情包 『/rua』
mirai特色表情生成。一度成为mirai bot最常见的功能（雾

使用说明：
```
/rua [Key] <@某人>
```
也可以使用图片：
```
/rua [Key] <图片>
```
其中[Key]可不填，若不填则会随机生成。[Key]可填以下几项：

```
anyasuki ( 阿尼亚 喜欢 )
bite ( 啃 咬 )
breast ( 胸 凶 )
cast ( 丢 )
center_symmetry ( 中心对称 左上对称 )
coupon ( 陪睡 )
cover_face ( 挡 )
crawl ( 爬 )
decent_kiss ( 抱歉 )
distracted ( 注意力 )
dont_touch ( 不要靠近 )
down_symmetry ( 对称 下对称 上下对称 )
eat ( 吃 )
fencing ( 击剑  )
garbage ( 垃圾桶 垃圾 探头 )
hammer ( 锤 )
interview ( 采访 )
jiujiu ( 么么 )
keep_away ( 远离 )
kiss ( 亲 热吻 )
knock ( 敲 打 )
left_down_symmetry ( 中心对称 左下对称 )
leg ( 蹭 )
like ( 永远喜欢 )
loading ( 加载 加载中 )
make_friend ( 加好友 )
marry ( 结婚 )
nano ( 纳米科技 )
need ( 需要 )
osu
painter ( 画 )
pat ( 拍 )
perfect ( 完美 )
petpet ( 摸 摸头 )
play ( 玩 顶 )
police ( 警察 )
pound ( 捣 )
pr ( 舔屏 )
punch ( 打拳 )
record ( 唱片 )
right_down_symmetry ( 中心对称 右下对称 )
right_symmetry ( 对称 右对称 左右对称 )
right_up_symmetry ( 中心对称 右上对称 )
roll ( 滚 推 )
rub ( 舔 prpr )
safe_sense ( 安全感 )
suck ( 吸 )
support ( 精神支柱 )
symmetry ( 对称 左对称 左右对称 )
tear ( 撕 )
thinkwhat ( 想 )
throw ( 扔 )
thump ( 锤 )
tightly ( 黏 )
twist ( 抱 )
up_symmetry ( 对称 上对称 上下对称 )
wallpaper ( 壁纸 )
worship ( 膜拜 )
yoasobi ( 群青 )
```

例子：
```
/rua twist @豆子 Doge
```
戳一戳将有30%概率触发该功能。

# 零乱的娱乐功能 『/amuse』
使用说明：

*夸我/夸某人*
```
/amuse chp <me|@某人>
```
彩虹屁功能

*骂我/骂某人*
```
/amuse zuan <me|@某人>
```
对着指定的人口吐芬芳（也可用于抖M）

*毒我/毒某人*
```
/amuse du <me|@某人>
```
输出毒鸡汤

*随机生成乱码*
```
/amuse gar
```
实际上并不是完全随机。

*舔我/舔某人*
```
/amuse tian <me|@某人>
```
调用舔狗日记的接口，内容一定程度上引起不适

# 网络工具 『/netool』
使用说明：

*ping测试*
```
/ping <目标名称> [ping次数] [超时时间/ms]
```
例子：
```
/ping 127.0.0.1 10
```

*网页测试*
```
/web <URL链接> [编码]
```
例子：
```
/web https://baidu.com
```

*端口扫描*
```
/nmap <目标名称> [端口]
```
例子：
```
/nmap 127.0.0.1 8080
```

*查墙*
```
/gc <目标名称>
```

# 游戏功能 『/game』
一些游戏功能。目前只有24点，且需要作者授权使用。如需要请与作者联系。

使用说明：

*24点*
```
/game 24p
```
发送指令查看规则
允许四则运算 `+, -, *, /` 和位运算 `>>`(右移)，`<<`(左移)，`&`(与)，`^`(异或)，`|`(或)
**注意**：这里的`^`不是乘方运算！！！

关于如何计算位运算，可以使用即将提及的功能
```
/math calc <表达式>
```
关于什么是位运算，参见本文档末的FAQ.

# 数学相关 『/math』
使用说明：

*逻辑判断*
```
/math logic <逻辑表达式>
```
若逻辑正确返回真，否则返回假。
支持符号：
“或”/“||”, “且”/“&&”, “+”, “-”, “*”, “\”, “/”, “%”,“(”,“)”
“=”(值等), “==”(全等), “!=”, “!==”, “>”, “<”, “>=”, “<=”
“in”(包含), “!in”(不包含), “reg”(正则匹配), “!reg”(正则不包含)
例子：
```
/math logic 1!=3+4-5+2||3>4
```

*计算结果*
```
/math calc <表达式>
```
支持四则运算：加 +   减 -   乘 * ×   除 / ÷   括号 ()

支持其他数值运算：  求余 %   求整 \   求次方 ^   如：4%3=1  4\3=1 4^3=64

支持分布运算：符号,  如：4+3,×5,-7 相当于 ((4+3)×5)-7

支持四舍五入：符号@  x@y  表示：将x四舍五入到相对于个位的第y位。
y大于0，舍入到小数点后y位；y=0，舍入到整数；y小于0，舍入到小数点前|y|位(需要带上括号)。

支持位运算：  左位移 <<   右位移 >>   位或 or   位与 and   位异或 xor

例子：
```
/math calc 4+5,^3,/3,@2,xor1
```

*MathWorld*
```
/math mw <词条>
```
词条为英文，省略空格和`'`号，除介词和连词外开头大写（请严格按照要求，否则将无法查询到结果）如：Dyck's Theorem -> DycksTheorem, Lie algebra ->LieAlgebra, probability and statistics -> ProbabilityandStatistics

如果不知道是否词条存在可以通过以下命令查询：
```
/web https://mathworld.wolfram.com/search/?query=<词条>
```
例子：
```
/math mw Handle
```

*Encyclopedia of Math*
```
/math em <词条>
```
词条为英文，空格用符号`_`代替

例子：
```
/math em adjoint_module
```

*查询π*
```
/math pi <起点数位> <查询位数>
```
例子：
```
/math pi 0 100
```

# Pixiv功能 『/px』
使用说明：

*ID查询*
```
/ px  id <图片id>
```
如果是多张图片，查看第n张，请在id后加-n。不支持r18图片。

*作者查询*
```
/px user <用户id>[-页数]
```
例子：
```
/px user 54259522-2
```

*以图搜图*
```
/px tst <图片>
```
**注意**：一定要加上空格，否则无法识别。

*以图搜番*
```
/px tsf <图片>
```
旧版豆子最受欢迎的功能。接的是SauceNAO接口。使用限制是一天100次，30内不超过4次，请慎用。

*СЭОТУ功能*
```
/px setu
```
大家喜闻乐见的功能（但是我是不会让你们用der!）。只有授权才可以使用，请与作者联系。

# Jeff笑话生成 『/jeffjoke』
关于什么是Jeff笑话，参加本文档末FAQ.,

使用说明：

*生成关于自己的笑话*
```
/jeffjoke <mj|myjoke> [条数]
```
条数可不填，默认一条

*生成关于别人的笑话*
```
/jeffjoke <dj|diyjoke> <某人>  [条数]
```
例子：
```
/jeffjoke dj 豆子 3
```

# StyleGAN 『/gan』
使用StyleGAN生成图片，如果图片过于诡异请不要恐慌，它们不是真实存在的。关于什么是StyleGAN，参见文档末的FAQ。

使用说明：

*生成猫*
```
/gan cat
```

*生成画作*
```
/gan art
```

*生成马*
```
/gan horse
```

*生成二次元人像*
```
/gan waifu
```
有概率失败，可以多试几次（中间请间隔一段时间）

# 圣训 『/yan』
记录群友的言行。无差别记录，如果需要制造某人的圣训录请与作者联系。作者必须也在要求该功能的群内，且需要征得被记录者的同意。

使用说明：
```
/yan-<QQID> [关键词]
```
理论上是这个指令，但可以要求作者使用其他的指令，比如“XX圣训”，“XX物语”等

*查看本群被记录者语录条数*
```
/yan length <QQID>
```
使用该命令需要作者授权。

*查看本群有哪些人已被记录*
```
/yan stars
```
使用该命令需要作者授权。

# 其他功能
这里是一些零碎的功能，一部分是初版豆子遗留的无法完全恢复的残件。

使用说明：

*发送动漫大图*
```
/anime
```
原`/img`功能块。之前使用的api.computerfreaker.cf接口现在已全部失效。

*今日说法*
```
/law
```
随机发送一条宪法内容。原`/laws`功能块，现在只有宪法能调用。

*生成幻影坦克*
```
/mirage
```
关于什么是幻影坦克，请参见文末FAQ.

*说指定的话*
```
/echo <内容>
```
原`/cmd`功能块。出于安全考量，现在只留下这一个鸡肋的功能。

*查看bot版本*
```
/ver
```

# FAQ
**1.什么是位运算？**

位运算就是直接对整数在内存中的二进制位进行操作的运算。参见[位运算](https://www.runoob.com/w3cnote/bit-operation.html)

**2.什么是Jeff笑话？**

Jeff Dean是谷歌的工程师，大神级别。Jeff笑话是以事实为依据（bushi）来表明Jeff非凡的能力的笑话。参见[JeffDeanFacts](https://github.com/LRitzdorf/TheJeffDeanFacts)

**3.什么是StyleGAN？**

StyleGAN是NVIDIA继ProGAN之后提出的新的生成对抗网络，借鉴风格迁移，通过修改不同层级在不影响其他层级的前提下控制视觉特征。参见[NVlabs/StyleGAN](https://github.com/NVlabs/stylegan)

**4.什么是幻影坦克？**

指一种双层图，这种图片分为内外两层，在未点击的情况下是一张图片，点击打开后又是一张图片。

**5.为什么豆子没有xxx功能？**

你去pr就有了。

**6.豆子的所有功能都是自己写的吗？**

不是。一部分来自github。但可以保证有至少七成以上是自己写的。搬运的功能大多可以自己重写，但这不意味着我会这么做。

**7.为什么`/tex render`功能会出错？**

我也没发现我的代码哪里有错。目前提供`/tex urender`作为解决方案，可以解决一切问题。

**8.为什么不提供涩图？**

初版豆子曾被这样封号过。同样，有话说得好，“一个bot只要有了涩图功能，那它就会变得只有涩图功能”。

**9.作者是计科专业的吗？**

不是。要不然豆子会比现在好得多。

**10.作者是谁？**

好问题，作者是谁

**11.如何帮助豆子？**

欢迎赞助打赏。毕竟豆子的大多数问题都是穷的问题（雾）
![输入图片说明](../images/MJIF(OK)%5B%5D4V$7U8TQJU%601G.jpg)
