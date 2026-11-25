# 超市销售数据可视化分析（Sample Superstore）

数据挖掘课程设计项目。基于经典零售数据集 Sample Superstore，使用 Pandas 做数据清洗、Matplotlib + Seaborn 做多维度可视化分析。

## 项目信息

| 项目 | 内容 |
|---|---|
| 课程 | 数据挖掘课程设计 |
| 数据集 | Sample Superstore（美国零售订单，2014—2017） |
| 数据规模 | 9,994 条记录、21 个特征 |
| 核心指标 | Sales（销售额）、Quantity（数量）、Discount（折扣）、Profit（利润） |
| 技术栈 | Python、Pandas、NumPy、Matplotlib、Seaborn |

## 文件说明

| 文件 | 说明 |
|---|---|
| `supermarket_sales_visualization.html` | Jupyter Notebook 导出的完整分析报告（含代码 + 7 张真实图表 + 分析结论） |
| `charts/chart_1.png` ~ `chart_7.png` | 从报告中分离出的 7 张真实图表 |
| `README.md` | 项目说明 |

> 命名规范：原文件 `王琪-超市销售数据可视化分析.html` 改名为英文 `supermarket_sales_visualization.html`；代码中的数据集引用同步由 `Sample - Superstore.csv` 改为 `superstore.csv`（运行前需将数据集文件按此名放置）。

## 分析流程

1. **数据读取与清洗**：`pd.read_csv('superstore.csv', encoding='windows-1252')`，处理特殊字符编码；将 Order Date / Ship Date 转为 datetime，提取 Year / Month 时间维度。缺失值统计为 0。
2. **七种可视化图表**（课程要求）：
   - 折线图 — 2014—2017 各季度销售额趋势
   - 散点图 — 销售额与利润的关系
   - 堆叠柱状图 — 各区域不同产品类别的销售额
   - 带核密度曲线的直方图 — 利润分布
   - 饼图 — 各产品类别销售额占比
   - 箱线图 — 不同产品类别的利润分布差异
   - 闭合雷达图 — 各区域综合表现（归一化后）

## 分析结论

- **销售趋势**：整体呈波动上升，下半年普遍高于上半年，尤其 Q4 突出。
- **利润问题**：存在大量「高销售、低利润甚至亏损」订单，部分产品过度打折；Furniture 类别利润离散度大、出现明显负利润。
- **品类与区域**：Technology 类利润表现更稳健；West 区域在总销售额和总数量上领先。

## 收获

掌握了 Pandas 数据清洗（编码问题处理、时间维度提取）及 Matplotlib + Seaborn 联合绘图，实现从原始数据到可视化洞察的完整分析流程。
