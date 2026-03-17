# Class 14 - Review

Original edit：2026-05-04

Last update：

Markdown type：Study markdown

Resources：BEHI_5011_14.assets 

Update log： 

---

Class 1：不同模型面对的检测图像都是属于什么检测方式

Class 3：最基础定义（什么是ML、DL），评判标准，什么是它们拥有的基础，如何构建一个ML、DL

Class 4：Loss，定义，如何判断

Class 5：如何评估，有什么Loss



Class 6：pipeline，如何选、如何

Class 7：为什么label-efficient出现，有哪些类型，什么是nomarlly

Class 9：Attention的组成，transformor是属于哪种attention，不同的之间的区别是什么，如何区分Q....





Class 10：fully explainability？

Class 11：为什么会有domain adaption learning：有data没有label

Class 12：优势，定义

Class 13：定义，适用范围（best？），如何做

---



# Top-down and bottom-up proteomics

自上而下与自下而上蛋白质组学

------

## 核心流程对比（图中部分）

### 1. Top-down proteomics（自上而下蛋白质组学）

- 流程

  ：

  1. 直接对**完整蛋白质混合物（Protein mix）\**进行\**电喷雾电离（Electrospray ionization）**
  2. 不经过酶解，直接对完整蛋白质分子进行 **LC-MS/MS（液相色谱 - 串联质谱）** 分析
  3. 数据分析可区分不同**蛋白质异构体（Proteoform）**，并匹配到对应的唯一数据库编号（Unique accessions）

  

- 关键特点：保留了完整蛋白质上的 ** 翻译后修饰（PTM）** 信息（如绿色的乙酰化 Acetylation、粉色的磷酸化 Phosphorylation）

------

### 2. Bottom-up proteomics（自下而上蛋白质组学）

- 流程

  ：

  1. 先对蛋白质混合物进行**溶液内酶解（In-solution digestion）**，将完整蛋白质切成短肽段
  2. 对肽段进行电喷雾电离，再通过 LC-MS/MS 分析
  3. 数据分析通过肽段序列匹配，反向推断出原始蛋白质的身份（Unique accessions）

  

- 关键特点：只能通过肽段间接推断蛋白质，无法直接保留完整的 PTM 组合信息

------

## 右侧文字翻译（Top-down 部分）

- **Top-down proteomics: the whole protein molecule is injected and sequenced.**

  自上而下蛋白质组学：直接对完整的蛋白质分子进行进样和测序。

  

- **Advantages: Measure proteoforms directly. Can detect relationships between far-away modifications (analogous to “phasing” in genomics).**

  优势：可直接测量蛋白质异构体；能够检测蛋白质上相距较远的修饰位点之间的关联（类似于基因组学中的 “定相 / 单体型分析”）。

  

- **Disadvantages: Poor ionization and fragmentation (incomplete ion ladders). Need a lot of relatively pure proteins.**

  劣势：电离效率和碎片化效果较差（易产生不完整的离子阶梯）；需要大量相对纯度较高的蛋白质样品。
