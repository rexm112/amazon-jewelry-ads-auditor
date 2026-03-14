# 决策规则与日常阈值

## 1. 先建立店铺自己的基准

优先用滚动 30 / 60 / 180 天数据，至少按以下维度分层：

- 价格带：低客单不锈钢 / 中高客单银饰与莫桑钻
- 流量类型：top of search / rest of search / product pages
- campaign 类型：auto / exact / phrase / broad / product targeting
- 产品分层：scale / defend / harvest-clear

建议维护这些基础指标：

- ctr = clicks / impressions
- cvr = orders / clicks
- cpc = spend / clicks
- rpc = sales / clicks
- cpa = spend / orders
- acos = spend / sales
- tacos = spend / total sales

## 2. 当前店铺可用的临时锚点

在没有更完整分层前，可先参考当前对话里形成的临时内部锚点：

- 整体 ctr：约 1%
- 整体 cvr：约 4% 到 5.5%
- 整体平均 cpc：约 0.25 美元
- 整体 acos：约 25% 到 30%
- 整体 tacos：优先按用户确认的同口径数值

这些不是行业 benchmark，只是这个店铺当前状态的起始值。

## 3. 经济边界

### 整体层面

- 如果用户给的是最终利润率，并且有同口径 tacos：
  - 广告前贡献毛利率 ≈ 最终利润率 + tacos
- 若口径不同，不要直接相加。

### 词 / target / 单品层面

- 可接受 cpa = 客单价 × 目标 acos
- 可接受 cpc = rpc × 目标 acos
- 单个商品或词的近似公式：
  - 可接受 cpc = 售价 × cvr × 目标 acos

提醒：bid 提高后，cvr 和 rpc 可能下降，因此操作目标必须低于理论上限。

## 4. 加量判断

一个 campaign、keyword 或 target 可以进入“可加量”池，通常至少满足以下一部分条件：

1. 已经出单，且 acos 低于目标
2. cpc 低于可接受 cpc
3. search term impression share 或 top-of-search share 偏低，但已有成交证明
4. parent 总销量还有放大空间
5. 库存和补货稳定
6. hero child 已基本确定合理

### 加量动作优先级

1. 先从“必须降 / 停”的 campaign 中腾预算
2. 再给“重点放大”组提 bid
3. 最后才考虑提升整体预算或更激进地抢首页

### 加量幅度

- 重点放大：+15% 到 +25%
- 可小提：+5% 到 +10%
- 样本很小但表现漂亮：先 +10%，观察 7 天

不要全店一起抬。

## 5. 否定词与隔离测试规则

## 核心原则

否词不等于永久拉黑。对语义很贴产品、但当前不赚钱的词，优先做“从主 campaign 移出 + 低 bid sandbox 继续验证”。

### 收割词

满足以下多数条件：
- 已出单
- acos 可接受
- 明显优于同主题兄弟词
- 适合进入 exact / phrase 收割层

### 隔离测试词

适用于：
- 语义核心，但当前在 auto / broad / 主 campaign 里不赚钱
- 样本还不完全够，但值得继续验证
- 不想永久放弃

操作：
- 单独建 exact 或 phrase
- very low bid
- 小预算
- 给出明确止损线

### 真正否定词

适用于：
- 已花费超过 2 个可接受 cpa 仍无单
- 或 25 到 30 点击以上仍无单
- 同主题已有更强兄弟词
- 或明显不相关

## 6. 数据量阈值

### 样本不足
- clicks < 10 且 spend < 1 个可接受 cpa

### 观察 / 降级测试
- 0 单，但已花 1 到 2 个可接受 cpa
- 或 10 到 20 点击仍无单

### 从主 campaign 移出
- 0 单且已花 2 个以上可接受 cpa
- 或 25 到 30 点击仍无单
- 对低客单低毛利词，执行更严格

### 收割 / 放量
- 已出单，且 acos 在目标内
- 或即使样本小，但长期 180 天数据反复证明同主题成立

## 7. placement 判断

### top of search
- 不是天然就该抢
- 只有强款、强词、较高利润空间才配抢
- 若 cpc 被显著抬高、acos 失控，不要硬顶

### rest of search
- 很多 generic 词的试金石
- 若持续差，优先降级或拆词

### product pages
- 容易吃到便宜曝光
- 不能因为曝光多就默认好
- 要看是否真的出单、是否拖累整体

### 常见动作
- “保首页、压其余搜索”
- “保商品页、别抢首页”
- “商品页拖累明显，拆出赢 ASIN 单独投”

## 8. daily / weekly / monthly 节奏

### 每天
- 看花费是否失控
- 看重点放大组是否真的吃到更多点击和订单
- 看是否有异常词突然烧钱

### 每周
- 复盘 campaign 分层：必须降、维持、可小提、重点放大
- 更新收割词、隔离测试词、否定词清单
- 复盘 placement 结构是否变化

### 每月
- 按价格带和流量类型重算基准
- 更新目标 acos / tacos / cpc guardrail
- 重新确认 scale / defend / harvest-clear 划分

## 9. 复盘时必须回答的问题

1. 花出去的钱，是买到了更好的流量，还是只是买到了更贵的流量？
2. cpc 上涨后，rpc 和 cvr 是否同步下降？
3. 变体引流逻辑是否真实有效，还是“父体有单”被重复当成理由？
4. 是 hero child 选错，还是 bid 太低？
5. 是否把该停的钱继续烧、把该放大的钱却不敢放？
