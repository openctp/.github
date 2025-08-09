# openctp的产品与服务
[openctp](https://github.com/openctp/openctp)是一个以CTP生态为基础的技术服务平台，通过将中泰XTP、华鑫奇点等股票柜台的接口封装成[CTPAPI](https://github.com/openctp/openctp)，使得CTP程序只需将CTP动态库如"thosttraderapi_se.dll"替换成各柜台的同版本CTPAPI动态库即可接入相应柜台，可以帮助开发者节省大量的接口对接成本。

[openctp](https://github.com/openctp/openctp)提供了一套与上期技术SimNow类似的模拟环境，支持CTPAPI接口，不仅提供国内各期货交易所的期货与期权品种模拟交易，还提供了A股的股票、基金、债券以及股票期权模拟交易，也支持港股、美股等市场模拟交易。

openctp还提供了[CTPAPI的Python接口](https://github.com/openctp/openctp-ctp-python)以及[CTP股票期权API的Python接口](https://github.com/openctp/openctp-ctpopt-python)，开发了CTP交易客户端[ViTrader](https://github.com/openctp/openctp/tree/master/widgets/ViTrader)并开放了源码，还开发了图形界面的交易客户端[TickTrader](http://openctp.cn/TickTrader.html),都支持openctp、CTP、CTP股票期权、中泰XTP、华鑫奇点股票与股票期权等柜台，还做了一款TickTrader的简版[TickTraderMini](http://openctp.cn/TickTrader.html)，采用openctp的CTPAPI兼容接口技术支持了CTP、TTS、华鑫证券股票与股票期权等柜台，无需自己再替换dll。

openctp还提供了CTP、华鑫奇点、中泰XTP等柜台接口开发的咨询服务以及策略交易框架开发、柜台系统开发等培训服务。

![openctp全景图](https://user-images.githubusercontent.com/83346523/148639077-6c328032-b75a-4979-be8d-157de60cf3b4.jpg)

# openctp模拟环境
openctp模拟环境采用与CTP完全兼容的SDK接口，提供期货、期权以及股票（A股股票、基金、债券及股票期权）等全市场全品种模拟交易。

openctp模拟环境的使用方法及账号注册等见[股票、期货、期权等模拟环境](http://openctp.cn/Trading.html)。

TTS柜台CTPAPI的github仓库：[TTS柜台CTPAPI](https://github.com/openctp/openctp/tree/master/TTS-CTPAPI)。

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

# TickTrader
一款支持点价下单风格的交易客户端，支持CTP、CTP股票期权、TTS、华鑫证券股票及股票期权、中泰证券等股票、期货以及期权柜台，下载地址：[TickTrader下载](http://www.openctp.cn/TickTrader.html)。

# TickTraderMini
一款支持点价下单风格的交易客户端，采用openctp的CTPAPI兼容接口技术支持了CTP、TTS、华鑫证券股票与股票期权等柜台，无需自己再替换dll，下载地址：[TickTraderMini下载](http://www.openctp.cn/TickTrader.html)。

# [ViTrader](https://github.com/openctp/openctp/tree/master/widgets/ViTrader)
命令行交易终端（股票、期货、期权），绝大部分命令与VI编辑器中相同，支持CTP、openctp、华鑫证券、中泰证券等柜台，支持Windows、Linux、MacOS等操作系统，下载地址：[ViTrader下载](http://www.openctp.cn/Widgets.html)

# TTS
TTS全称Tick Trading System，是openctp开发的一款支持多通道多账户多交易员的交易系统，以CTPAPI接口对外通讯，openctp的模拟平台就是采用TTS系统提供模拟交易服务。

# CTPAPI策略交易框架
CTPAPI接口的坑非常多，专业性很强，持仓与资金的实时计算也很难处理，各种持仓与资金字段的冻结、计算等，openctp给出了一套轻量级的基于Tick的CTPAPI策略交易框架源码，保持了原汁原味的CTP数据结构，代码很漂亮，不到5000行，简洁易懂，二次开发很容易，更多介绍见：[CTPAPI策略交易框架](http://openctp.cn/TTF.html)。

# openctp技术服务
## 期货交易佣金及保证金参考表
openctp提供了一个实盘环境的手续费及保证金等资金计算参考表，每天同步实盘。网址：[期货交易佣金及保证金参考表](http://www.openctp.cn/fees.html)
## 模拟环境监控平台
openctp提供了一个集中监控SimNow、华鑫N视界、中泰XTP、东财EMT等模拟环境的监控平台，当然也包括openctp自己的模拟环境，有几个环境，有没开着，一眼就知道了。网址：[CTP接口模拟环境监控](http://www.openctp.cn/simenv.html)。
## 实盘环境监控平台
openctp提供了一个监控各大期货公司CTP柜台实盘系统运行情况的监控平台，并且还标出了支持上期所免费5档行情的期货公司，网址：[CTP柜台实盘环境监控](http://www.openctp.cn/env.html)。
## CTP、中泰XTP、华鑫TORA等柜台接口、文档及相关软件下载
SimNow网站经常上不了是吧，可以在openctp下载，网址：[CTPAPI接口与文档下载](http://www.openctp.cn/CTPAPI.html)。

# openctp培训服务
openctp提供证券期货交易开发方面的技术培训，也提供行业无关的基础技术培训，openctp的培训偏向于就业方向，比如想去私募或者科技公司从事量化或者柜台系统开发的比较适合，当然如果想自己学习一些技术帮助自己更好地做交易也是可以的。openctp的培训是迭代式的，会不断更新，补充更多的内容，同学可在相应课程的群内永久交流。所有课程的每节课在[B站](https://space.bilibili.com/549478063)上都有试看视频，具体请至[openctp官网](http://openctp.cn/Learning.html)了解。

# 实盘交易
openctp与券商和期货公司均有合作，不仅交易费用低，还可得到免费的技术服务，具体请至[openctp官网](http://openctp.cn/)了解。

# 技术交流
- QQ群：564385877
- 微信群+v：openctp_helper

# openctp官网
[www.openctp.cn](http://www.openctp.cn/)

# openctp公众号
<img src="https://user-images.githubusercontent.com/83346523/225707613-59293970-0f04-4056-8ea4-dd4596a4efec.png" alt="微信公众号" width="300" height="350" />
