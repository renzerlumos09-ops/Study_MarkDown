# Top-down and bottom-up proteomics

自上而下与自下而上蛋白质组学

------

## 核心流程对比（图中部分）

### 1. Top-down proteomics（自上而下蛋白质组学）

- 流程

  1. 直接对**完整蛋白质混合物（Protein mix）\**进行\**电喷雾电离（Electrospray ionization）**
  2. 不经过酶解，直接对完整蛋白质分子进行 **LC-MS/MS（液相色谱 - 串联质谱）** 分析
  3. 数据分析可区分不同**蛋白质异构体（Proteoform）**，并匹配到对应的唯一数据库编号（Unique accessions）

  

- 关键特点：保留了完整蛋白质上的 ** 翻译后修饰（PTM）** 信息（如绿色的乙酰化 Acetylation、粉色的磷酸化 Phosphorylation）

------

### 2. Bottom-up proteomics（自下而上蛋白质组学）

- 流程

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



## 第一张：Proteoforms（蛋白质异构体 / 蛋白质形式）

### 标题

**Proteoforms**：蛋白质异构体（也译作 “蛋白质形式”，指同一基因编码的蛋白质的不同分子形式）

### 要点翻译

1. **Proteoforms are different molecular forms of a protein.**

   蛋白质异构体，是同一种蛋白质的不同分子形式。

   

2. **Different proteoforms of the same “protein” is derived from the same gene but differ in splice variants, sequence variants (e.g. mutations), and post-translational modifications**

   同一 “蛋白质” 的不同异构体，均由同一基因编码产生，但因可变剪接变体、序列变异（如突变）和翻译后修饰的不同而存在差异。

   

------

## 第二张：Shotgun (“bottom up”) proteomics（鸟枪法 / 自下而上蛋白质组学）

### 标题

**Shotgun (“bottom up”) proteomics**：鸟枪法（又称 “自下而上”）蛋白质组学

### 流程图示翻译

1. Cells or tissue → Step 1 Extraction → Proteins

   

   细胞或组织 → 步骤 1 提取 → 蛋白质

2. Proteins → Step 2 Digestion → Peptides

   

   蛋白质 → 步骤 2 酶解 → 肽段

3. Peptides → Step 3 UHPLC → 色谱分离

   

   肽段 → 步骤 3 超高效液相色谱（UHPLC）→ 色谱分离

4. Step 4 ESI → Mass spectrometer

   

   步骤 4 电喷雾电离（ESI）→ 质谱仪

5. **Chromatogram**：色谱图（强度随时间变化的曲线）

6. **MS1 / MS2**：一级质谱 / 二级质谱（分别对应母离子扫描和碎片离子扫描）

### 样本制备（Sample preparation）部分翻译

- Sample preparation

  ：样本制备

  - **Subcellular fractionation**：亚细胞组分分离（如细胞核、细胞质分离）
  - **Protein extraction**：蛋白质提取
  - **Affinity enrichment, depletion, etc.**：亲和富集、高丰度蛋白去除等（用于提高低丰度蛋白的检测率）
  - **Protein fractionation**：蛋白质分级分离
  - **Digestion into peptides**：酶解为肽段
  - **Peptide fractionation**：肽段分级分离
  - **Desalting**：脱盐（去除质谱分析中的盐离子干扰）

  

------

### 补充术语解释

- **Proteoform**：蛋白质异构体，是蛋白质组学的核心概念，强调同一基因产物因剪接、突变、修饰产生的所有分子形式的总和。
- **Shotgun proteomics**：鸟枪法，是自下而上蛋白质组学的主流方法，核心思路是将蛋白质酶解为肽段，通过质谱分析肽段序列再反向推断蛋白质身份。
- **UHPLC**：超高效液相色谱，用于肽段的分离，提高质谱检测的分辨率和通量。
- **ESI**：电喷雾电离，一种软电离技术，能让肽段带上电荷，进入质谱仪分析。



**Matrix-assisted laser desorption ionization**

基质辅助激光解吸电离（简称 MALDI，是质谱分析中常用的软电离技术）

------

### 步骤翻译与说明

1. **Sample is mixed with a matrix. Co-crystallization of the sample occurs to focus the laser (UV range) absorption.**

   样品与基质混合，二者发生共结晶，以此增强对（紫外波段）激光的吸收。

   

2. **The laser is directed to the target region. The matrix heats rapidly and vaporizes. The sample molecules are desorbed alongside the surrounding material.**

   激光照射目标区域，基质迅速受热并气化，样品分子随基质一同被解吸出来。

   

3. **An electrical field is applied to accelerate the charged gaseous sample. Propelling it to the detector.**

   施加电场，使带电的气态样品加速，推动其向检测器运动。

   

4. **m/z measurement is performed by the time of flight (TOF) of the ions.**

   通过离子的飞行时间（TOF）来完成质荷比（m/z）的测定。



**LC-MS**：液相色谱 - 质谱联用技术（Liquid Chromatography-Mass Spectrometry）

------

### 内容翻译

> LC-MS is essentially a two-dimensional separation method for peptides, first based on hydrophobicity (LC), then based on m/z (MS)

**译文：**

LC-MS 本质上是一种针对肽段的二维分离方法：首先基于**疏水性**进行分离（液相色谱，LC），再基于 ** 质荷比（m/z）** 进行分离（质谱，MS）。



**Chromatography**：色谱法（也译作层析法，是一种基于物质在固定相和流动相之间分配 / 吸附差异实现分离的技术）

------

### 第二张：原理说明翻译

> Different dye colors move at different speeds:
>
> 不同颜色的染料移动速度不同，原因如下：

- **The bigger pigments move slower since they are blocked by the pores.**

  分子较大的色素移动更慢，因为它们会被介质中的孔隙阻挡。

  

- **Less soluble dye also move slower since they are not as easily carried by the solvent.**

  溶解度较低的染料移动也更慢，因为它们不容易被溶剂携带。



**Chromatography**：色谱法（也译作层析法，是一种基于物质在固定相和流动相之间分配 / 吸附差异实现分离的技术）

------

### 第二张：原理说明翻译

> Different dye colors move at different speeds:
>
> 不同颜色的染料移动速度不同，原因如下：

- **The bigger pigments move slower since they are blocked by the pores.**

  分子较大的色素移动更慢，因为它们会被介质中的孔隙阻挡。

  

- **Less soluble dye also move slower since they are not as easily carried by the solvent.**

  溶解度较低的染料移动也更慢，因为它们不容易被溶剂携带。



**Ionization**：电离（质谱分析中，使中性分子带电形成离子的过程）

------

### 第二张：两种电离方式对比翻译

#### 左侧：Hard ionization（硬电离）

> A large amount of energy is transferred to the molecule, enough to overcome its bond energy and breaks it into smaller ions or radicals.
>
> 译文：大量能量被传递给分子，足以克服其化学键能，将分子打碎成更小的离子或自由基。

#### 右侧：Soft ionization（软电离）

> A small amount of energy is transferred to the molecule, just enough to impart a charge. Inevitably some smaller ions or radicals will be produced.
>
> 译文：仅向分子传递少量能量，刚好使其带上电荷；过程中不可避免地会产生少量较小的离子或碎片。



**Soft ionization methods – ESI**

软电离方法 —— 电喷雾电离（ESI，即 Electrospray ionization）

------

### 第二张：ESI 原理步骤翻译

#### Electrospray ionization（电喷雾电离）

1. **Samples are dissolved in a solvent and water mixture. The pH of the solution determines the ion charge. (For peptides, the common method is to elute them in acidic conditions so that they are positively charged.)**

   样品溶解在有机溶剂与水的混合溶液中；溶液的 pH 值决定了离子的电荷状态。（对于肽段，通常在酸性条件下洗脱，使其带正电荷。）

   

2. **The solution passes through a capillary needle with a high voltage (kV) applied to it.**

   溶液流经施加了高电压（千伏级）的毛细管针。

   

3. **The solution forms charged droplets. Each droplets possess the same charge, causing the formation of smaller droplets.**

   溶液形成带电液滴；液滴间因带同种电荷相互排斥，进而分裂成更小的液滴。

   

4. **The solvents quickly evaporated due to the heat and vacuum exposure. Leaving behind charged ions of the sample.**

   溶剂在加热和真空环境下快速蒸发，最终留下样品的带电离子。

   

5. **The charged ions are directed towards the mass spectrometer.**

   带电离子被导入质谱仪进行分析。



**Quadrupole mass analyzer**：四极杆质量分析器（质谱仪中用于按质荷比分离离子的核心部件）

------

### 第二张图原理步骤翻译

1. **4 parallel metal rods with currents of electricity running through them. Generating a radial electric field.**

   四根平行的金属杆通有电流，产生径向电场。

   

2. **Each opposing metal rod is connected. One pair will run at a DC voltage while the other will run at a radio frequency voltage.**

   相对的金属杆成对连接：其中一对施加直流电压，另一对施加射频电压。

   

3. **This causes only ions with the targeted m/z to be able to travel axially while other ions will fly off.**

   这种电场组合使得只有目标质荷比（m/z）的离子能沿轴向稳定飞行，其他离子则会因轨迹偏移而撞到杆上被过滤掉。

   

4. **Ions with the correct m/z will pass through the quadrupole and be detected.**

   具有正确质荷比的离子会穿过四极杆，最终到达检测器被检测到。



**Time-of-flight**：飞行时间（TOF，即 Time-of-Flight），是质谱仪中一种常见的质量分析器。

------

### 第二张图原理步骤翻译

#### Time-of-Flight（飞行时间质量分析器）

1. **Ions are accelerated by electric field and fly towards detector in vacuum**

   离子被电场加速，在真空环境中向检测器飞行。

   

2. **The time of flight is proportional to square root of the mass-to-charge ratio**

   离子的飞行时间与其质荷比的平方根成正比。（即：质荷比越大，飞行速度越慢，到达检测器的时间越长）

   

3. **Longer flight path increases resolution**

   更长的飞行路径可以提高质量分辨率。（因此现代 TOF 质谱常通过反射式设计延长有效飞行距离）



**Orbitrap**：轨道阱（也译作静电轨道阱），是一种高分辨率质谱质量分析器。

------

### 第二张图原理步骤翻译

> Based on the Kingdon trap
>
> 基于金顿（Kingdon）离子阱原理

1. **A coaxial inner electrode and an outer-barrel electrode.**

   由同轴的内电极和桶形外电极构成。

   

2. **Charged gaseous molecules are trapped in the electric field and are trapped in an orbit around the inner electrode.**

   带电的气态分子被束缚在电场中，并沿内电极做轨道运动。

   

3. **The motion is harmonic and can be detected by the outer barrel electrode.**

   离子的运动为简谐运动，其信号可被桶形外电极检测到。

   

4. **Signals are analyzed via the Fourier-transform to obtain the mass spectra.**

   信号经傅里叶变换分析，最终得到质谱图。



### 第一张图：Tandem mass spectrometry (MS/MS)

**标题：串联质谱（MS/MS）**

- 可进行 MS/MS 的质谱仪：

  - **离子阱（Ion traps）**：通过**时间维度**实现多级质谱分析（在同一阱内按时间先后完成母离子选择、碎裂、子离子检测）。
  - **三重四极杆（Triple quadrupoles）**：通过**空间维度**实现多级质谱分析；中间的四极杆为碰撞池，用于母离子的碎裂。
  - **混合型质谱仪（Hybrids）**：如四极杆 - 飞行时间（Q-TOF）、四极杆 - 轨道阱（Q-Orbitrap）、离子阱 - 轨道阱（Ion trap-Orbitrap）等。

  

------

### 第二张图：Fragmentation methods

**标题：碎裂方法**

#### 左侧：Collision-induced dissociation (CID) 碰撞诱导解离

- 原理示意图展示了母离子（Precursor ions）进入碰撞池，与碰撞气体（如 He, Ar, N₂）发生碰撞，获得能量后碎裂，生成碎片离子（Fragment ions）和中性丢失（Neutral lost）。

- **高能碰撞解离（HCD）**：与 CID 机制类似，但碰撞能量更高，是轨道阱质谱中常用的碎裂方式。

- 优缺点

  ：

  - 优点：碎裂效率高。
  - 缺点：易断裂不稳定的翻译后修饰（如磷酸化、糖基化），导致修饰位点信息丢失。

  

#### 右侧：Electron transfer dissociation (ETD) 电子转移解离

- 原理示意图展示了带正电的母离子（Precursor cation）与自由基阴离子反应，获得电子形成自由基阳离子（Cation radical），随后发生主链断裂。

- 利用多环芳烃类自由基阴离子，将电子转移给肽段母离子。

- 优缺点

  ：

  - 优点：能保留翻译后修饰（PTMs），便于修饰位点定位；更适合长肽段和高电荷态离子。
  - 缺点：碎裂效率相对较低。



### 图 1：Ion mobility spectrometry（离子淌度质谱）

**标题：离子淌度质谱**

- 这是一个额外的离子分离维度，基于离子的 “淌度”，更准确地说是 ** 碰撞截面（CCS）** 进行分离。淌度与离子和气体分子的碰撞频率直接相关，这种碰撞会阻碍或促进离子向质量分析器的移动。
- 能够分离**质荷比（m/z）相同**但结构不同的离子（如同分异构体、构象异构体）。

------

### 图 2：timsTOF

**标题：timsTOF（捕获式离子淌度飞行时间质谱仪）**

这是一种将 ** 捕获式离子淌度（TIMS）** 与飞行时间（TOF）质量分析器联用的质谱仪。

------

### 图 3：Trapped ion mobility spectrometry - TOF（捕获式离子淌度 - 飞行时间质谱）

1. 惰性气体流推动离子在 tims 仪器中移动，气体对离子的推动力与离子的表面积成正比。
2. 施加电场来减缓离子的运动，从而根据离子的电荷对其进行分离。
3. 流出的离子由四极杆 / TOF 检测器检测；将离子在 tims 中的淌度时间与质荷比（m/z）作图，为数据分析增加了一个全新的维度。



### Acquisition methods

**标题：数据采集方法**

- 尽管现代质谱每秒可进行数百次扫描，但仍无法快到能选择所有可检测的母离子进行碎裂。因此，质谱需要做出决策：**哪些离子需要被隔离并送入 MS/MS 分析**。

------

#### Data-dependent acquisition (DDA)

**数据依赖型采集（DDA）**

- 从 MS1（母离子）扫描中，选择 **N 个丰度最高的离子（最高峰）** 进行碎裂。
- 选择的离子相对单一，可获得更简单、质量更高的 MS/MS 谱图。
- 缺点：会遗漏低丰度离子；实验重复性较差。

------

#### Data-independent acquisition (DIA)

**数据非依赖型采集（DIA）**

- 将质荷比（m/z）范围划分为多个窗口，依次对每个窗口内的所有离子进行碎裂。
- 多个离子同时被碎裂，会产生复杂的 “嵌合” MS/MS 谱图。
- 优势：更适合定量分析，可获得完整的实验记录。

------

#### Selected/parallel reaction monitoring (SRM / PRM)

**选择 / 平行反应监测（SRM/PRM）**

- 预先对质谱进行编程，仅选择目标离子进行碎裂（也可仅检测目标碎片离子）。
- 仅聚焦于测量目标离子，灵敏度和重复性更高。
- 前提：需要预先知道要检测的目标离子信息。



| 对比项               | 数据依赖型采集 (DDA)                                         | 数据非依赖型采集 (DIA)                                       | 选择 / 平行反应监测 (SRM/PRM)                                |
| -------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **MS1 离子选择方式** | 选择丰度最高的 Top N 个离子进行碎裂和 MS2 分析。             | 采集指定 m/z 范围内所有离子的数据，并同时对所有离子进行碎裂。 | 在初步发现阶段后，选择特定的目标离子进行靶向分析。           |
| **偏向性**           | ・偏好高丰度离子・容易遗漏低丰度离子                         | ・几乎无偏向性・特定 m/z 范围内的所有离子都会被选择碎裂      | ・仅关注预先定义的肽段・遗漏所有未被定义的肽段               |
| **优点**             | ・技术成熟、操作简单・对高丰度肽段灵敏度高・所选离子的碎裂数据丰富 | ・对整个样品的覆盖更全面・重复性更好，受技术误差影响小・低丰度肽段不会被主动过滤掉 | ・对目标肽段的特异性和灵敏度极高・能提供最佳的无标记定量数据 |
| **缺点**             | ・容易遗漏低丰度肽段・离子选择的随机性导致重复性问题・偏向生物体系中蛋白质动态范围的高端 | ・数据复杂度大幅提高，需要高级分析工具・单个肽段的灵敏度较低・在非常复杂的样品中信号干扰的可能性很高 | ・仅限于预设的目标物，会遗漏其他所有蛋白质・需要先验知识（通常来自 DDA 或 DIA 实验） |



### 第一张图：Shotgun proteomics – a typical experiment

**标题：鸟枪法蛋白质组学 —— 典型实验流程**

1. 包含数千种蛋白质的复杂样品（如血液样本、细胞培养裂解液等），经酶解处理成肽段混合物。
2. （可选）通过色谱法进行分级分离，降低样品复杂度。
3. 每个分级组分通过 LC-MS（液相色谱 - 质谱联用）进行分析，单次分析时长约 0.5-4 小时。
4. 质谱仪每小时可产生约 100,000 张 MS/MS 二级质谱图。
5. 质谱图通过计算机软件进行鉴定解析。
6. 约 20-60% 的质谱图能被成功鉴定，匹配到对应的肽段序列。
7. 单次实验可鉴定 / 定量 100-5000 种蛋白质。
8. 检测限低至 ** 阿托摩尔（attomole, 10⁻¹⁸ mol）** 级别的进样肽段。

------

### 第二张图：Quantification: overview

**标题：蛋白质组学定量概述**

1. 质谱仪本身只能测量

   相对丰度

   （如对照组 vs 处理组之间的丰度差异）。

   - 若需进行**绝对定量**，需要向样品中加入已知浓度的内标参考品。

   

2. 即使在最佳实验条件下，中丰度蛋白质的定量误差也可能高达 ±20%；实际实验中误差可能更高。

3. 大规模无差别的 “全量” 定量，成本高且准确性、灵敏度较低；而 “有针对性” 的靶向定量方法（如 PRM/assays）灵敏度和准确性更高。

4. 与所有组学技术一样，需要采用先进的统计学方法来控制假阳性率。



### 第一张图：Stable isotope (¹³C, ¹⁵N, ¹⁸O) labeling

**标题：稳定同位素（¹³C, ¹⁵N, ¹⁸O）标记**

- 待定量的分析物化学性质完全相同，但质量不同（形成 “轻 / 重” 同位素对）。
- 假设它们具有完全相同的色谱行为和电离效率。
- 各组样品应**尽早混合**，以减少处理偏差，并一同进样分析。
- 轻 / 重同位素对会在同一保留时间出峰，两者峰面积（AUC）的比值即可反映其相对丰度。
- 合成的重同位素标记肽段可作为内标加入，用于**绝对定量**。

------

### 第二张图：Metabolic labeling

**标题：代谢标记法**

------

### 第三张图：Stable Isotope Labeling with Amino acids in Cell culture (SILAC)

**标题：细胞培养中氨基酸稳定同位素标记法（SILAC）**

- **操作简单**：只需在细胞培养基中加入标记氨基酸即可。
- **成本较高**：同位素标记的氨基酸价格昂贵。
- **处理偏差最小**：样品在细胞裂解前就已混合，减少了后续处理带来的误差。
- **应用局限**：不适用于无法体外培养的细胞 / 组织。
- **全标记**：细胞内所有新合成的蛋白质都会带上同位素标记。



### 图 1：Chemical labeling (MS level)

**标题：化学标记法（MS 水平定量）**

- 同一化学标签的不同同位素版本
- 通常通过共价键连接到半胱氨酸（如 ICAT 技术）或氨基（如二甲基标记）
- 相比代谢标记，更容易引入处理偏差
- 适用于所有类型的样品
- 可通过亲和标签富集标记肽段，降低样品复杂度
- 在一级质谱（MS）水平进行定量

------

### 图 3：Chemical labeling (MS/MS level)

**标题：化学标记法（MS/MS 水平定量）**

------

### 图 4：Isobaric tags for quantification at MS/MS level

**标题：用于 MS/MS 水平定量的等重标签**

- 代表技术：TMT（最高可实现 18 重标记）和 iTRAQ（最高可实现 8 重标记）
- 由于标签是等重的，所有 “通道” 的肽段在一级质谱中表现为同一质量，会被同时碎裂
- 在二级碎裂过程中，质量标签会从肽段上脱落，在 MS/MS 谱图中表现为不同的峰，以此区分不同通道的信号并进行定量

| 方法               | 代表技术         | 定量层级 | 核心优势                           |
| ------------------ | ---------------- | -------- | ---------------------------------- |
| **MS 水平标记**    | ICAT、二甲基标记 | MS1      | 原理简单，在一级谱中区分轻 / 重对  |
| **MS/MS 水平标记** | TMT、iTRAQ       | MS2      | 多重标记能力强，可同时分析多个样品 |

### 图 1：Label-free quantitative proteomics

**标题：无标记定量蛋白质组学**

- 各组样品通过独立的质谱运行进行分析。
- 无需使用稳定同位素标记。
- 容易引入处理偏差和系统误差，因此需要良好的归一化策略。
- 通常需要大量生物学重复、高重现性的色谱分离和高质量精度的质谱仪。

------

### 图 2：两种无标记定量方法

**基于强度的定量（Intensity-based quantification）**

- 对 LC-MS 谱图进行峰对齐，匹配不同样品中同一分析物的对应峰。
- 通过积分峰面积作为定量指标。
- 计算量大，对数据处理要求高。

**谱图计数法（Spectral counting）**

- 直接统计每个蛋白质 / 肽段被鉴定到的 MS/MS 谱图数量。
- 需要大数据集才能获得可靠结果。

------

### 图 3：Untargeted vs. targeted proteomics

**标题：非靶向 vs 靶向蛋白质组学**

#### 非靶向 “发现导向” 蛋白质组学

- 核心问题：“我的样品中有哪些蛋白质 / 蛋白质变体？”
- 类似基因组测序，旨在获得完整的组分列表，或发现新的、未知的蛋白质。
- 通常使用数据依赖型采集（DDA）：质谱被设定为选择丰度最高的母离子进行碎裂。
- 采样过程具有随机性，重复性较差，无法确认蛋白质 “不存在”。

#### 靶向 “假设驱动” 蛋白质组学

- 核心问题：“我的样品中是否含有蛋白 X？如果有，含量是多少？”
- 类似 DNA 芯片，旨在测量预先设定的目标肽段。
- 通常使用选择反应监测（SRM/PRM）：质谱被设定为专门 “寻找” 已知的目标母离子 / 碎片离子信号。
- 不具随机性，可以确认目标物的 “不存在”，更适合定量分析，且对预期目标的检测灵敏度更高。

