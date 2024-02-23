# [openctp产品与服务](https://github.com/openctp/openctp)
openctp是一个以CTP生态为基础的平台，既提供了华鑫证券奇点、中泰证券XTP、东方财富EMT、东方证券OST等柜台的[CTPAPI](https://github.com/openctp/openctp)兼容接口，也提供了一套与上期技术SimNow模拟环境类似的模拟环境，也支持CTPAPI接口，不仅提供国内各期货交易所的期货与期权品种模拟交易，还提供了A股的股票、基金、债券以及股票期权模拟交易，也支持港股、美股等市场模拟交易。

openctp还提供了CTPAPI的Python接口，开发了CTP交易客户端[ViTrader](https://github.com/openctp/ViTrader)并开放了源码，还开发了图形界面的交易客户端[TickTrader](https://github.com/openctp/TickTrader),都支持openctp、CTP、CTP股票期权、中泰XTP、华鑫奇点股票与股票期权等柜台。

openctp还做了一套websocket接口的CTP服务，[webctp](https://github.com/openctp/webctp)，将CTP的服务以websocket+json形式对外提供服务，也开放了源码。

openctp还提供了CTP、华鑫奇点、中泰XTP等柜台接口的开发咨询和培训以及柜台系统等的开发培训服务。

openctp还有更多的产品和服务在研发中。。。

![openctp全景图](https://user-images.githubusercontent.com/83346523/148639077-6c328032-b75a-4979-be8d-157de60cf3b4.jpg)

# openctp模拟环境
openctp模拟环境与上期技术SimNow模拟环境类似，均为CTPAPI接口的测试与仿真平台，CTP是上期开发的，SimNow用的也是CTP柜台，所以SimNow是CTPAPI接口的官方测试平台，openctp是自己开发了兼容CTPAPI接口的柜台系统，由于CTP柜台业务非常多，我们openctp只是从一般投资者角度考虑，只实现了一般交易过程中需要使用的接口，完整版还需要到SimNow测试，其实SimNow也没多完整，毕竟是个模拟环境，很多业务也不支持，所以有些功能还是需要在实盘环境中测试的。

openctp模拟环境有三套，一套7x24环境，不间断循环播放最新交易日的一段行情，一套为仿真环境，交易时段与实盘一致，可以用来长期验证策略的运行效果，除期货外还支持A股的股票交易。第三套也是仿真环境，不过带宽较高，提供的品种也全，除期货、期权外还提供了A股的股票、基金、债券以及股票期权的仿真交易，收费也很便宜，只要300块一年，关注openctp公众号并回复注册vip即可。

## openctp模拟环境账号注册
关注openctp公众号，回复相应信息即可注册模拟账号，即时生效，初始资金1000万。
- 7x24环境账号注册，回复注册24，每回复一次就多注册一个7x24账号，一个微信最多注册3个号。
- 仿真环境账号注册，回复注册仿真，每回复一次就多注册一个仿真账号，一个微信最多注册3个号。
- vip环境账号注册，回复注册vip，每回复一次就多注册一个vip账号，一个微信最多注册10个号。

## BrokerID、AppID、AuthCode
openctp模拟环境不检查这几个字段，3项均可不填。

## 7x24模拟环境
- 交易前置 - tcp://121.37.80.177:20002
- 行情前置 - tcp://121.37.80.177:20004
## 仿真环境
- 交易前置 - tcp://121.37.90.193:20002
- 行情前置 - 无（订阅行情需要直连相应行情通道）
## 仿真环境
- 交易前置 - tcp://42.192.226.242:20002
- 行情前置 - 无（订阅行情需要直连相应行情通道）
## openctp环境监控平台
openctp提供了一个集中监控SimNow、华鑫N视界、中泰XTP、东财EMT等模拟环境的监控平台，当然也包括openctp自己的模拟环境，有几个环境，有没开着，一眼就知道了。

监控页面：[openctp模拟环境监控](http://121.37.80.177:50080/index.html)

# [CTPAPI](https://github.com/openctp/openctp)
openctp提供了华鑫证券、中泰证券、东方财富等股票柜台的CTPAPI接口，使得CTP程序无需修改接入股票柜台。

openctp还提供了Python版的CTPAPI的pip install支持，为Python开发者提供了极大的便利。其它语言的CTPAPI我们也做了收集，均为github作者实现。
## [CTPAPI-Python](https://github.com/openctp/openctp-ctp-python)
提供两种方式使用Python版的CTPAPI，一种是下载我们做好的Python库，一种是用pip install一键安装。

[openctp官方开发的Python语言版CTPAPI](https://github.com/openctp/openctp-ctp-python)
## CTPAPI-Java
[openctp收集的Java语言版CTPAPI](https://github.com/openctp/openctp/tree/master/ctpapi-java)
## CTPAPI-Go
[openctp收集的Go语言版CTPAPI](https://github.com/openctp/openctp/tree/master/ctpapi-go)
## 华鑫证券奇点股票柜台CTPAPI
[华鑫证券奇点股票柜台CTPAPI](https://github.com/openctp/openctp/tree/master/ctp2华鑫证券STP)
## 华鑫证券奇点股票期权柜台CTPAPI
[华鑫证券奇点股票期权柜台CTPAPI](https://github.com/openctp/openctp/tree/master/ctp2STPOPT)
## 中泰证券XTP柜台CTPAPI
[中泰证券XTP柜台CTPAPI](https://github.com/openctp/openctp/tree/master/ctp2中泰证券XTP)
## 东方财富EMT柜台CTPAPI
[东方财富EMT柜台CTPAPI](https://github.com/openctp/openctp/tree/master/ctp2EMT东方财富)

# [TickTrader](https://github.com/openctp/TickTrader)
一款支持订单OneClickOrder下单风格的交易客户端，支持CTP、CTP股票期权、openctp、华鑫证券股票及股票期权、中泰证券等股票、期货以及期权柜台。
[TickTrader下载](http://121.37.80.177:50080/download.html)
# MiniTrader
一款支持订单OneClickOrder下单风格的交易客户端，开发中，相当于TickTrader的Mini版，开发中，即将发布。

# [ViTrader](https://github.com/openctp/ViTrader)
ViTrader（原TextTrader），命令行交易终端（股票、期货、期权），绝大部分命令与VI编辑器中相同，支持CTP、openctp、华鑫证券、中泰证券等柜台，支持Windows、Linux、MacOS等操作系统。
[ViTrader下载](http://121.37.80.177:50080/download.html)

# [webctp](https://github.com/openctp/webctp)
以websocket+json协议提供CTP交易及行情服务。

# TTS
TTS全称Tick Trading System，是openctp开发的一款支持多通道多账户多交易员的交易系统，以CTPAPI接口对外通讯，openctp的模拟平台就是采用TTS系统提供模拟交易服务。

# openctp咨询服务
基于openctp积累的深厚的技术，我们为CTP、华鑫奇点、中泰XTP等柜台接入与开发提供咨询服务，有接口及实盘交易问题均可咨询，只需1000元，永久服务。

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

# openctp公众号
<img src="https://user-images.githubusercontent.com/83346523/225707613-59293970-0f04-4056-8ea4-dd4596a4efec.png" alt="微信公众号" width="300" height="350" />
