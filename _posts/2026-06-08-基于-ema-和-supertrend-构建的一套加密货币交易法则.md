---
layout: post
title: 基于 EMA 和 SuperTrend 构建的一套加密货币交易法则
lang: zh-CN
category: Essays
tags:
- trading
- cryptocurrency
math: true
date: 2026-06-08 14:54 +0800
---
经过了与 AI 的讨论，以及根据我自己的经验，终于搭建了一套基于 EMA 和 SuperTrend 指标的加密货币交易法则：

1. **趋势识别**（周线）
   - EMA60 向上，且价格在 EMA60 之上，为牛市，只做多。
   - EMA60 向下，且价格在 EMA60 之下，为熊市，只做空。
2. **开仓**（日线）
   - 在牛市中，当 SuperTrend 由红翻绿时，以市价开仓。
   - 在熊市中，当 SuperTrend 由绿翻红时，以市价开仓。
3. **加仓**
   - 如果趋势仍在，当价格回踩 EMA20 或 EMA60 后又重新站稳时，可以市价加仓。
   - 最多三次加仓。
4. **止损**
   - 采用移动止损，将止损点设为 SuperTrend 的上轨或者下轨。
5. **仓位管理**
   - 基本原则是使得每笔交易的亏损不超过总资金的 2%。设总资产为 $A$，交易保证金是 $D$，交易价格是 $P_T$，止损价格是 $P_S$，杠杆倍数是 $L$，则应有如下关系：

     $$
     D \cdot \frac{|P_T - P_S|}{P_T} \cdot L = A \cdot 0.02
     $$

     最终算出交易数量 $DL$ 是

     $$
     D L = 0.02 A \frac{P_T}{|P_T-P_S|}
     $$
6. **止盈**
   - 计算当前价格对 EMA20 的偏离率，超过 20% 则止盈 20% 仓位。
   - 在牛市中，当 SuperTrend 由绿翻红时，以市价清仓。
   - 在熊市中，当 SuperTrend 由红翻绿时，以市价清仓。
