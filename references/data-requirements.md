# 数据需求与校验清单

## 1. 整店分析优先数据

### 必需优先项

1. **店铺利润总表 / 经营总表**
   - 日期区间
   - 总销售额
   - 广告销售额
   - 广告花费
   - 毛利润 / 最终利润
   - 毛利率 / 净利率定义
   - 若有退款、coupon、折扣、其他费用，最好单列

2. **campaign report / 广告活动汇总**
   - campaign name
   - impressions
   - clicks
   - spend
   - sales
   - orders
   - cpc
   - ctr
   - cvr 或可反推字段
   - bid / budget（若有）

3. **placement report**
   - campaign
   - placement type
   - impressions
   - clicks
   - spend
   - sales
   - orders
   - 便于判断首页、其余搜索、商品页的差异

4. **search term report**
   - customer search term
   - campaign / ad group
   - match type / targeting type
   - impressions
   - clicks
   - spend
   - sales
   - orders
   - sku / asin（若有）

### 强烈建议补充

5. **sku 与 parent asin 对照表 / top 产品表 / 广告商品表**
   - sku
   - child asin
   - parent asin
   - style / color / size
   - 便于判断 hero child 和变体引流

6. **targeting report / advertised product report**
   - 用于更精确看 keyword、product target、asin target 级别效果

7. **价格 / coupon / rating / review 快照**
   - 用于解释 CTR、CVR 和竞争力变化

## 2. 单品分析优先数据

1. SKU / child 与 parent 的映射
2. 该商品涉及的 campaign report
3. placement report
4. search term report
5. 如果要算承受边界：
   - 售价
   - 折扣 / coupon
   - referral fee
   - fba fee
   - 头程 / prep / 包装
   - 退款率或退款准备金
   - 若没有完整单品成本，也要至少说明“当前使用整店口径近似”

## 3. 校验动作

开始分析前，逐项检查：

### 日期与口径
- 文件日期区间是否一致
- 同一文件是否混有不同时间区间
- 归因窗口是否一致
- 是 gross sales 还是 net sales
- TACoS 分母用总销售还是净销售

### 结构与内容
- 是否有总计行、空行、重复表头
- 金额列是否仍是文本
- 百分比列是否可计算
- campaign / term 是否重复
- 是否有多个 marketplace 混在一起

### 常见冲突
- 广告销售额大于总销售额
- 有花费但没有点击
- 有订单但点击极少且明显异常
- 一张表用美元，一张表用人民币
- 利润表已含广告费，但用户又把广告费再减一次

## 4. 当数据不足时怎么处理

### 可以先分析的情况
- 缺少 targeting report，但 campaign / placement / search term 都在
- 缺少完整单品成本，但用户只想先看结构与相对优先级

### 不能强结论的情况
- 利润定义不清
- 日期范围差很多
- 没有 sku-parent 映射却要求做单品 parent 级判断
- 只有 search term report，却要求做全店利润承受边界

## 5. 与用户沟通的方式

指出问题时要具体：
- 哪个文件
- 哪个 sheet
- 哪列缺失或冲突
- 会影响哪一步分析
- 用户最小需要补什么

示例：
- “利润表里没有说明 23.8% 是广告前还是广告后利润率，这会直接影响 break-even ACoS 的判断。当前我只能先按广告后最终利润率理解，并把广告放量结论降为暂定结论。”
- “search term report 是 180 天，但 placement report 是 30 天，不能直接把两者混在一起判断同一轮加价测试，只能分别作为历史样本和近期位置结构参考。”
