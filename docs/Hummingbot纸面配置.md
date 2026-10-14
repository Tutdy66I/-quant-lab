# Hummingbot 纸面交易配置说明
# Paper Trading Setup for quant-lab
#
# 模式: Hummingbot 自带模拟模式 (paper_trade_enabled)
# 不连接任何真实交易所,所有成交均为模拟撮合。
#
# 启动步骤 (在 hb_env 虚拟环境中):
#   1. source hb_env/bin/activate
#   2. hummingbot  (首次启动会引导配置)
#   3. 在 hummingbot 命令行中:
#        paper_trade  -> 开启纸面交易模式
#        create       -> 选择策略 pure_market_making
#        使用以下参数:
#
# 策略: pure_market_making (做市策略,逻辑简单可解释)
# 交易对: BTC-USDT (纸面)
# 参数:
#   bid_spread: 1.0        # 买单离中间价 1%
#   ask_spread: 1.0        # 卖单离中间价 1%
#   order_amount: 0.001    # 每笔 0.001 BTC
#   order_refresh_time: 60 # 每 60 秒刷新一次挂单
#
# 日志位置: hummingbot/logs/
# 模拟交易记录会写入 logs,可用 `history` 命令查看。
#
# 注意: 纸面模式用的是模拟订单簿,不是真实市场深度,
# 它的意义是熟悉"策略 -> 信号 -> 模拟成交 -> 记录"的完整链路,
# 不是预测收益。
