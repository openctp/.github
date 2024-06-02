# openctp的产品与服务
[openctp](https://github.com/openctp/openctp)是一个以CTP生态为基础的技术服务平台，通过将中泰XTP、华鑫奇点等股票柜台的接口封装成[CTPAPI](https://github.com/openctp/openctp)，使得CTP程序只需将CTP动态库如"thosttraderapi_se.dll"替换成各柜台的同版本CTPAPI动态库即可接入相应柜台，可以帮助开发者节省大量的接口对接成本。

[openctp](https://github.com/openctp/openctp)提供了一套与上期技术SimNow类似的模拟环境，支持CTPAPI接口，不仅提供国内各期货交易所的期货与期权品种模拟交易，还提供了A股的股票、基金、债券以及股票期权模拟交易，也支持港股、美股等市场模拟交易。

openctp还提供了[CTPAPI的Python接口](https://github.com/openctp/openctp-ctp-python)以及[CTP股票期权API的Python接口](https://github.com/openctp/openctp-ctpopt-python)，开发了CTP交易客户端[ViTrader](https://github.com/openctp/ViTrader)并开放了源码，还开发了图形界面的交易客户端[TickTrader](http://www.openctp.cn/download.html),都支持openctp、CTP、CTP股票期权、中泰XTP、华鑫奇点股票与股票期权等柜台，还做了一款TickTrader的简版[MiniTrader](https://github.com/openctp/MiniTrader)，采用openctp的CTPAPI兼容接口技术支持了CTP、TTS、华鑫证券股票与股票期权等柜台，无需自己再替换dll。

openctp还做了一套websocket接口的CTP服务，[webctp](https://github.com/openctp/webctp)，将CTP的接口以websocket+json形式对外提供服务，也开放了源码。

openctp还提供了CTP、华鑫奇点、中泰XTP等柜台接口开发的咨询服务以及策略交易框架开发、柜台系统开发等培训服务。

![openctp全景图](https://user-images.githubusercontent.com/83346523/148639077-6c328032-b75a-4979-be8d-157de60cf3b4.jpg)

# openctp模拟环境
openctp模拟环境采用与CTP完全兼容的SDK接口，提供期货、期权以及股票（A股股票、基金、债券及股票期权）等全市场全品种模拟交易。

openctp模拟环境的使用方法及账号注册等见[股票、期货、期权等模拟环境](https://zhuanlan.zhihu.com/p/685170963)。

TTS柜台CTPAPI的github仓库：[TTS柜台CTPAPI](https://github.com/openctp/openctp/tree/master/ctp2TTS)。

# [CTPAPI](https://github.com/openctp/openctp)
openctp提供了华鑫证券、中泰证券、东方财富等股票柜台的CTPAPI接口，使得CTP程序无需修改即可接入股票柜台。

## [CTPAPI-Python](https://github.com/openctp/openctp-ctp-python)
CTPAPI的Python接口，openctp官方开发，使用Swig技术制作，提供两种方式使用Python版的CTPAPI，一种是下载我们做好的Python库，一种是用pip install一键安装。

## [CTP股票期权API-Python](https://github.com/openctp/openctp-ctpopt-python)
CTP股票期权API的Python接口，openctp官方开发，使用Swig技术制作，提供两种方式使用Python版的CTP股票期权API，一种是下载我们做好的Python库，一种是用pip install一键安装。

## openctp开发的demo与工具
### CTP、XTP、TORA等柜台接口demo
虽然ctp等官方都给出了一些demo，但是都过于粗糙了，甚至有误导作用，可以看看我们是怎么写demo的，地址：[CTP、XTP等柜台接口demo](https://github.com/openctp/openctp/tree/master/demo/print)
### 行情显示工具prices
一个命令行模式的CTP行情显示工具，采用curses技术开发，地址：[行情显示工具prices](https://github.com/openctp/openctp/tree/master/demo/prices)

# [TickTrader](http://www.openctp.cn/download.html)
一款支持点价下单风格的交易客户端，支持CTP、CTP股票期权、TTS、华鑫证券股票及股票期权、中泰证券等股票、期货以及期权柜台，下载地址：[TickTrader下载](http://www.openctp.cn/download.html)。

# [MiniTrader](https://github.com/openctp/MiniTrader)
一款支持点价下单风格的交易客户端，采用openctp的CTPAPI兼容接口技术支持了CTP、TTS、华鑫证券股票与股票期权等柜台，无需自己再替换dll，下载地址：[MiniTrader下载](http://www.openctp.cn/download.html)。

# [ViTrader](https://github.com/openctp/ViTrader)
ViTrader（原TextTrader），命令行交易终端（股票、期货、期权），绝大部分命令与VI编辑器中相同，支持CTP、openctp、华鑫证券、中泰证券等柜台，支持Windows、Linux、MacOS等操作系统，下载地址：[ViTrader下载](http://www.openctp.cn/download.html)

# [webctp](https://github.com/openctp/webctp)
以websocket+json协议提供CTP交易及行情服务，适合web类产品开发。

# TTS
TTS全称Tick Trading System，是openctp开发的一款支持多通道多账户多交易员的交易系统，以CTPAPI接口对外通讯，openctp的模拟平台就是采用TTS系统提供模拟交易服务。

# TickTradingFramework策略交易框架
CTP接口的坑非常多，专业性很强，持仓与资金的实时计算也很难处理，各种持仓与资金字段的冻结、计算等，openctp给出了一套轻量级的基于Tick的CTP策略交易框架源码，保持了原汁原味的CTP数据结构，代码很漂亮，不到5000行，简洁易懂，二次开发很容易。第二期培训中免费赠送了一套简版的Python交易框架。付费版有更完善更专业的持仓与资金计算，以及更多专业的处理，更多介绍见：[CTP策略交易框架](https://mp.weixin.qq.com/s?__biz=Mzk0ODI0NDE2Ng==&mid=2247485118&idx=1&sn=6ad0fe9db64e15f0ef481aac6cdbaa4e&chksm=c36bdd17f41c5401a823513fc82b28f42616b63faece2e6dc96db07b5a70ca419ccdbfecc835&token=246256733&lang=zh_CN#rd)。
- CTP策略交易框架Python-Lite版源码（培训版，不带手续费及保证金等计算），3000元。
- CTP策略交易框架Python版源码，10000元。只支持单账户，实时计算持仓及资金。
- CTP策略交易框架Python多账户版源码，30000元。支持多账户，可以通过openctp的CTPAPI兼容接口方式接入华鑫证券、中泰证券等柜台。
- CTP策略交易框架Python多柜台版源码，50000元。支持多账户，支持华鑫证券、中泰证券、易盛等跨柜台策略交易，支持华鑫证券、中泰证券、易盛等多数据源，且支持数据源之间负载均衡。
- CTP策略交易框架C++版源码，30000元。只支持单账户，实时计算持仓及资金。
- CTP策略交易框架C++多账户版源码，50000元。支持多账户，可以通过openctp的CTPAPI兼容接口方式接入华鑫证券、中泰证券等柜台。
- CTP策略交易框架C++多柜台版源码，80000元。支持多账户，支持华鑫证券、中泰证券、易盛等跨柜台策略交易，支持华鑫证券、中泰证券、易盛等多数据源，且支持数据源之间负载均衡。

# openctp技术服务
## 期货交易佣金及保证金参考表
openctp提供了一个实盘环境的手续费及保证金等资金计算参考表，每天同步实盘。网址：[openctp期货交易佣金及保证金参考表](http://www.openctp.cn/fees.html)
## 模拟环境监控平台
openctp提供了一个集中监控SimNow、华鑫N视界、中泰XTP、东财EMT等模拟环境的监控平台，当然也包括openctp自己的模拟环境，有几个环境，有没开着，一眼就知道了。网址：[CTP接口模拟环境监控](http://www.openctp.cn)。
## 实盘环境监控平台
openctp提供了一个监控各大期货公司CTP柜台实盘系统运行情况的监控平台，并且还标出了支持上期所免费5档行情的期货公司，网址：[CTP柜台实盘环境监控](http://www.openctp.cn/env.html)。
## CTP、中泰XTP、华鑫TORA等柜台接口、文档及相关软件下载
SimNow网站经常上不了是吧，可以在openctp下载，网址：[CTPAPI接口与文档下载](http://www.openctp.cn/download.html)。

# openctp培训服务
openctp提供证券期货交易开发方面的技术培训，也提供行业无关的基础技术培训，openctp的培训偏向于就业方向，比如想去私募或者科技公司从事量化或者柜台系统开发的比较适合，当然如果想自己学习一些技术帮助自己更好地做交易也是可以的。openctp的培训是迭代式的，会不断更新，补充更多的内容，同学可在相应课程的群内永久交流。所有课程的每节课在B站上都有试看视频，报培训只需要在openctp的公众号回复培训两个字即可获取联系方式。

openctp不定期组织同学进行技术交流，为大家创造一个好的学习氛围。

## 课程介绍
- 第一期：[C/C++高级编程](https://www.bilibili.com/video/BV1mV4y1V7HM)，3000元，以krenx开发的C语言跨平台开发框架[Think库](https://github.com/krenx1983/think)为基准进行讲解，含socket网络编程、IPC进程通讯等，有众多实用的工具，可立即应用到工作中。另外还有boost.asio异步网络通讯框架等开发技术的讲解，也提供相应的实例源码。
- 第二期：[CTP、XTP等柜台接口开发技术](https://www.bilibili.com/video/BV1JP411N78s)，5000元，以openctp相关技术为基准进行讲解，含CTPAPI底层逻辑、CTPAPI各种注意事项、开源CTP客户端TextTrader源码讲解等。送高质量轻量级Tick级多策略交易框架源码（约三五千行），保持原汁原味的CTP数据结构，实时计算持仓、资金。
- 第三期：[交易系统开发](https://www.bilibili.com/video/BV1F3411f7Q9)，5000元，以TTS交易系统为基准进行讲解，含交易系统结构、架构技术、业务表结构设计、关键业务处理等。送一套完整的交易撮合系统源码，含下单、仓位与资金计算、委托回报、成交回报、撮合成交、行情推送等完整功能，正在开发中，开发完成后也将免费发给前面已报名的同学。
- 第四期：[金融交易业务与产品设计](https://www.bilibili.com/video/BV1sd4y1a7Kk)，3000元，通讲全球股票、期货、期权交易发展历程、交易规则、计算公式、风险控制及产品设计，提供一份CTP全部常用字段的详细说明。
- 第五期：[内存数据库架构交易系统总线开发技术](https://www.bilibili.com/video/BV1Bx4y1K7t7)，8000元，通过TTS的总线架构技术讲解CTP那样的总线开发技术，包括重演、热备、负载均衡、最短路由、分布式计算等技术，内存计算架构在各行业的高性能通讯方面都可以应用，远不止金融交易领域。

## openctp公开课
openctp做了一些免费的0基础学习课程，帮助更多朋友进入到软件编程与证券期货交易行业。
- [C语言公开课](https://www.bilibili.com/video/BV1CK411o743)：以生动有趣的方式讲C语言基础性编程技术，重在兴趣培养和信心建立。
- C++语言公开课：以生动有趣的方式讲C++语言基础性编程技术，课程在准备中。
- [Linux环境编程公开课](https://www.bilibili.com/video/BV1Jw411E7sF)：介绍Unix&Linux的前世今世，讲Shell、VI编辑器等使用，讲netstat、traceroute、ifconfig、lsof等网络工具的使用，讲正则表达式等等，0基础，谁都能听得懂。

# 实盘交易
openctp有合作的券商和期货公司，不仅交易费用低并且还可以得到免费的技术支持服务（CTP、XTP等接口与应用开发培训等），具体请关注openctp公众号，回复“咨询”两个字。

# 技术交流
QQ群：127235179

# openctp官网
[www.openctp.cn](http://www.openctp.cn/)

# openctp公众号
<img src="https://user-images.githubusercontent.com/83346523/225707613-59293970-0f04-4056-8ea4-dd4596a4efec.png" alt="微信公众号" width="300" height="350" />
