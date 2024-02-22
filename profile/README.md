# openctp
CTP开放平台提供A股、港股、美股、期货、期权等全品种接入通道，通过提供中泰证券XTP、华鑫证券奇点、东方证券OST、东方财富证券EMT、盈透证券TWS等各通道的CTPAPI接口，CTP程序可以无缝对接各股票柜台。平台也提供了一套基于TTS交易系统的模拟环境，同样提供了CTPAPI兼容接口，可以替代Simnow，为CTP量化交易开发者提供7x24可用的模拟环境。

# TickTrader
一款支持订单OneClickOrder下单风格的交易客户端，支持CTP、CTP股票期权、openctp、华鑫证券股票及期权、中泰证券等股票、期货、期权柜台。

# MiniTrader
一款支持订单OneClickOrder下单风格的交易客户端，开发中，相当于TickTrader的Mini版。

# ViTrader
ViTrader（原TextTrader），命令行交易终端（股票、期货、期权），绝大部分命令与VI编辑器中相同，支持CTP、openctp、华鑫证券、中泰证券等柜台，支持Windows、Linux、MacOS等操作系统。

# webctp
以websocket+json协议提供CTP交易及行情服务。

# TTS
TTS全称Tick Trading System，是一款支持多通道多账户多交易员的交易系统，以CTPAPI接口对外通讯，openctp的模拟平台就是采用TTS系统提供模拟交易服务。

# openctp-ctp-python
CTPAPI的Python版，使用Swig生成，支持pip install方式。