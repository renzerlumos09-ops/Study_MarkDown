# Study Notes of 计算神经科学

---

## 模型类型

3 Models of computational to understanding the Brain: 3种描述大脑的计算模型:

|模型|概念|作用|
|---|---|---|
|Descriptive Models 描述模型|用于描述神经元如何对外部刺激做出反应，和如何使用编码模型来定量描述该过程|decoding(解码)：**“发生了什么？”** ——建立现象与数据的映射；|
|Mechanistic Models 机制模型|用于模拟单个神经元或计算机上的神经网络的行为|**“如何发生的？”** —— 拆解黑箱，模拟过程；|
|Interpretive(or Normative) Models 解释性/规范性模型|用于解释brain circuits operate the way they do神经回路的运行方式|Computational principles(神经回路的基本计算规则)： **“为何这样发生？”** —— 探寻最优原则（如能量最小化、信息最大化）。|

目前已知的CN研究计划：
>欧洲, Henry Markram, 人类脑计划, 超大神经网络极端模拟人类整体脑行为

 

### Recommended Textbooks 

[1] *Theoretical Neuroscience: Computational and Mathematical Modeling of Neural Systems*. By P. Dayan & L. Abbott

[2] *Tutorial on Neural Systems Modelling*. By T. Anastasio

[3] *神经科学——探索脑(第四版)*. By Mark F.Bear & Barry W. Connors & Michael A. Paradiso

---



## Class 1 - What is CN?

**Definition of Computational Neuroscience:**计算神经科学是提供三种不同操作工具和方法的领域，具体探究：

- 表征神经系统的功能——Description Models;

- 确认神经系统的功能机制——Mechanistic Models;

- 解释神经系统的特定运行模式——Interpretive(or Normative) Models.

  

### 什么是感受域？通过感受域来理解三种模型

Receptive Fields感受域的概念：

- Specific properties of a sensory stimulus that generate a strong response from the cell. 感官刺激的特定属性，能引起细胞强烈反应。

> “设有一束光斑投射到视网膜上，当光只作用于视网膜的一个小区域时，就会改变神经元的放电频率，视网膜的这个区域就被称为该神经元的*感受域/野*。”				《神经科学——探索脑(第四版)》Page 322



“感受域”实际上是一个用于描述*感觉系统*中**神经元反应特异性**的通用术语。

- 相关术语: *Electrical signal* from brain：输出呈微小数字脉冲的形式，被称为*尖峰或动作电位*。
    *Stimulus: 刺激*。
- Receptive Fields具有**方向特异性**：

> 感受域的形状会有所变化，并且相应的刺激能够最大程度地激活神经元，譬如：在视觉皮层的不同区域，神经元对**光条、光斑、甚至是复杂的具有生物学意义的形状(手和脸)**具有最佳反应。



### 感受域的特性与模型构建

a.   视觉系统的感受域具有层级化结构，从简单的特征检测发展到复杂的特征整合：

 

**两类**基础的感受域特性（**Descriptive Models****部分**）：

1) center-surround receptive fields 中心-环绕感受域：大圆套小圆的同心圆结构感受域，中心区域与环绕区域对光刺激的反应相反，大圆+则小圆-

a.   核心功能是检测**局部亮度**对比，输出特征对光点或任何朝向明暗边界有反应，但不具备**方向选择性**。

b.   代表细胞：Lateral Geniculate Nucleus(LGN)外膝体，位于左右丘脑枕外下方的一堆小核团，分为左LGN和右LGN.

2) Oriented receptive fields定向感受域：细长的椭圆形，具有并排的兴奋区与抑制区，核心功能是检测**特定朝向**的边缘或光条，**具有**方向选择性。

a.   代表细胞：Primary Visual Cortex(V1 RF)初级视觉皮层，位于大脑皮层主要负责处理视觉信息的部分，位于大脑后部的枕叶，具体位于Bordmann 17区.

 

b.   构建定向感受域（**Mechanistic Models****部分**）：

1) 基础机制：大量LGN RF cell发送信号给单个V1 RF cell信息，V1RF接受无方向性信息处理为具备方向性的信息：接收到的LGN信号以特殊方式排列与对其，通过给定前馈连接或在特定单元上的收敛，共同形成了方向信息.

a.   Oriented receptive fields定向感受域的**计算优势**：

**“Efficient Coding hypothesis”：**有效编码假说，认为大脑通过进化的目标是利用神经细胞忠实有效地表达图像，表现为不同V1RF的线性累加： ![img](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAKYAAAA4CAMAAABAOnN2AAAAAXNSR0IArs4c6QAAAHhQTFRFAAAAAAAAAAA6AABmADo6ADpmADqQAGa2OgAAOjoAOjpmOmaQOma2OpDbZgAAZmYAZmY6ZmZmZpC2ZrbbZrb/kDoAkGYAkGY6kNv/tmYAtmY6ttvbttv/tv/btv//25A627Zm2////7Zm/9uQ/9u2/9vb//+2///bSN8pvAAAAAF0Uk5TAEDm2GYAAAAJcEhZcwAAHYcAAB2HAY/l8WUAAAAZdEVYdFNvZnR3YXJlAE1pY3Jvc29mdCBPZmZpY2V/7TVxAAADKUlEQVRoQ+1YbXPaMAxOoNCsY91Lx7bQbSGElv//Dyv5VVaUxPZtHNezP3A525IeP3qxTFWVURgoDBQGCgOFgcJAYeD6DLR1/f36VlMtAsp69StV6tr7u3rzfKjXf69tN81eV2/7qjo2+HvD4/BJgRsebpzOZApfHyGY2bjFFOwA491XO74g4v8Nc2jQSlqiX/aBBKoYwzwRvu8+Phuf0VnYEJ8QaHP9O83zCIxYAHYFNjUBdmyMiXA2HmaVU9zR7Tr1cECwSk7HeowLLwf8sBXPzlYX+IqHCWym10zMIhIorQgTz6IX1Jc5lp8Fy/EwwWL8ZkcgxpgX6xZgKk/fa2EPEz7jLYMKoyApPtF33u2iqAekSpiBRGCmGARecqoJc7tkkcEcszkWOv+sV4jm+IGT0CZWI6sb3T7vBg9TOZ3HphDQat+2x+LDyJMySCVjOAT/4q5ZP3iYuNXmqZ0Fw1x6aHZ9V6//7Lf90ISlXArNOJh49NkaYQGpgrSxnaKdPY4Pedphhq0/3/fVZR+qBt8tZMJkoKPBObcrQHqsvrn+i8xKvoBlKf27zNAE8OzOHB2HANr5LnEeJuiULu6s4m4BgdvnmgHj3jNWI3tX+roJwgKbUEAkB+UVd4NzbOnErnoVf6rdcJ50iWUyPRCpqEqyIoZmXArhVc5P3tJAJzlN7gJe3gMRyCDvH7IiNjeRMNuFu84BUnTygiRn5oTONqPvMAYWk8/B1O3+qPUQgP770IQoYpUM0dBiwjok6U7nIl5psALuiG9SgtNDiRil5OVHMOc6S4xiR6efRX1MhHiIrOR07gZsEC1DoyCH99+gsG1V166L5RN86e7dccOuTKLVr+hDpr2DDMpTIHbSLL4+El321aNSRzcTECV21m4MRHCbO0C4ktLz+b0sMFsNc2iS3wHTIhnK+FlYYFrQXXqDPS2SoYzDDMvYGTyqkj6s1FF+mhbJUMYssse2zWKhg1yCOi2SoYwZC5/aulPDLkJF08sSsmB9WiRDGbNMWjHTTnqYx4ekfyYQjCwyvZLEg7QZijNpLKPUTYtkKIuyWDYVBgoDhYF3z8AbBKc17RuIWpUAAAAASUVORK5CYII=)，结果表现为呈现梯度式的明暗关系图像。

​    Î (重建的图像)；RF_i (感受野)；r_i (当前图像的响应强度)；

**该假设表明了大脑会尝试去找到对环境的忠实而有效的描述，因此该假说可拓展为所有的计算神经模型所使用的。**

 

### 神经的电性特征

> 《探索脑》Page 59

1. **EPSP = Excitatiory post-synaptic potential 兴奋性突触后电位**：是指由兴奋性突触的活动在突触后神经元中产生的去极化性质的膜电位变化。

- 当去极化超过阈值时，会导致突触后神经元的兴奋，进而产生动作电位。
- EPSP的产生是由于兴奋性递质作用于突触后膜上的受体，导致Na⁺或Ca²⁺通道开放，从而使局部膜去极化。
- 突触后电位的总和（包括EPSP和抑制性突触后电位IPSP）决定了是否会产生动作电位。

![EPSP](https://www.zysj.com.cn/lilunshuji/shenglixue/shenglixue205.gif)

2. 神经元的结构：**lipid bilayer**(凝脂双分子层) + gates/channels(门控/通道，镶嵌的蛋白质)

- Bilayer(双分子层) is **impermeable**(不可渗透性) to charged ion species such as Na+, Cl-, and K+.

- **Ionic channels** which is the name of protein in bilayer, embedded in membrane allow ions to flow in or out.

  - Each neuron maintians a potential difference_ across its membrane, inside is about <font color=red>-70 mV</font> relative to outside. [Na+] and [Cl-] higher outside while [K+] and orgainc anions [A-] higher inside.
  - **_Ionic pump_**(离子泵) maintains <font color=red>-70 mV</font> difference by expelling Na+ out and allowing K + ions in.

  <img src="C:\Users\23112\Downloads\1.png" width="40%">

  - Ionic pump are proteins that are **_selective_** and allow only specific ions to pass through. There are three gated:

    > 《探索脑》Page 92

    - <font color=red>Voltage-gated</font>(电压门控): Probabillity of opening depends on membrane voltage.

      > 电压门控是由**糖基化的多聚蛋白(glycosylated multimeric proteins)**或一条长链多肽构成，形成一个**势孔(potential pore)**，虽则和膜电位的变化会开合，从而调节离子在膜上的通量。有Ca、K等多种通道。
      >
      > > **电压钳(voltage clamp)**是专用于“钳制”神经元轴突的膜电位在任意数值，然后通过测量不同膜电位水平时流过膜的电流来推测膜电导的变化的工具。
      > >
      > > **膜片钳(patch clamp)**是专用于研究流过单个离子通道的离子电流的方法。

    - <font color=red>Chemically-gated</font>(化学门控): Binding or **_“synapses”_** to a chemical causes channel to open.

    - <font color=red>Mechanically-gated</font>(机械门控): Sensitive to pressure or stretch.

3. Action Potential(Spike) 动作点位(尖峰)

   > 《探索脑》Page 83

4. Action Potential**(Mathematically)** 数学方式描述尖峰

    - **Synapse**(突触) : the connection or junction between two neruons:

      > Page 111

      There have two type synapse: 

      - _Electrical_ synapse use _<font color=green>gap junctions</font>_(缝隙链接)：连接处，两个细胞的膜之间间隔约3nm，该狭窄的缝隙被称为**连接子蛋白(connexin)**的蛋白质簇所跨越，共约有20中不同的连接子蛋白亚型。

        - 6个连接子蛋白的亚基结合在一起形成的通道，为**连接子(connexon)**，2两个连接子(每个细胞一个)对接并结合，形成一个**缝隙链接通道(gap junction channel)**，通常孔径直径约1~2nm，

        1. 电突触是<font color=red>**双向的**</font>，电流以离子流的形式通过这些通道，这些由缝隙连接的细胞被称为**电耦联的(electrically coupled)**细胞。
        2. 突触前神经元的动作电位引起第二个神经元上的电介导的**突触后电位(postsynaptic potential, PSP)**，同时由于双向性使得突触前神经元也拥有一个PSP.

      - _Chemical_ synapse use _<font color=green>neurotransmitters</font>_(神经递质)

        1. Compare chemical synapse and electrical synapse, the advantage is chemical synapse can control the number of receptor in the second neuron and effectively control the action potential rather than electrical synapse.

      | 学说                             | 描述                                                         |
      | -------------------------------- | ------------------------------------------------------------ |
      | **The Synapse Doctrine**突触学说 | Synapses are the basis for memory and learning.<br />突触是记忆和学习的基础。 |

      4.1 Synaptic Plasticity discover how do brains learn.

      **Synaptic Plasticity**突触可塑性: meaning the repeat action potential between two neurons will influ the forming of synaptic.

      > If neuron A repeatedly takes part itfiring neuron B, then the synapsefrom A to B is strengthened.

      - **Long Term Potentiation(LTP)**: experimentally observed <font color=orange>increase</font> in synpatic strength that lasts for hours or days:

        By measuring the size of **EPSP** size for same input over time.

      - **Longt Term Depression(LTD)**: experimentally observed <font color=orange>decrease</font>  in synpatic strength that lasts for hours or days, it is opposite to LTP.

    - Synaptic Plasiticity depends on **Spike Timing**. LTP/LTD depends on relative timing of input and output spikes.

      ​	1. Δt > 0(spike timing > 0), input before output, LTP.

      ​	2. Δt < 0(spike timing < 0), input after output, LTD.

### Brain areas and their function

1. **Peripheral Nervous system(PNS)**外周神经系统: Somatic + visceral

   > Page 186

   1.1 Somatic PNS(外周躯体神经系统): 

   Nerves connecting to *voluntary skeletal mucles*(随意肌) and *sensory receptor*(感官感受器). There are twe different never fibers:

   - Afferent Nerve Fibers (incoming)传入神经纤维 : Axons(轴突) that carry info away from the periphery to the CNS.
   - Efferent Nerve Fibers (outcoming): Axons that carry info from the CNS outward to the periphery.

   1.2 Visceral PNS(外周内脏神经系统, also call involuntary nervous system 非随意神经系统, or vegetative nervous system 植物性神经系统, or autonomic nervous system 自主神经系统aka ANS):

   Nerves that connect to the heart, blood vessels, smooth muscles, and glands.

2. **Central Nervous system(CNS)**中枢神经系统: Spinal Cord + Brain

   > Page 185

   2.1 Spinal Cord(脊髓):  

   - it is *local feedback lopps* that control relfexes = reflex arcs. Spinal cord connect each part of body through *spinal nerve*. 
   - *Descending motor control signals* from brain activate spinal motor neurons.
   - *Ascending sensory axons* convey sensory information from muscles and skin back to the brain.

   2.2 Brain：

   > Page 182 and 194

   - The Hindbrain(后脑) is consists of three different regions.

   <img src="C:\Users\23112\Downloads\2.png" width="40%">

   		1. Medulla oblongata(延髓): controls brathing, muscle tone and blood pressure.
   		1. Pons: connected to the cerebellum & involved in sleep and arousal.
   		1. Cerebellum: Coordination and timing of voluntary movements, sense of equilibrium, language, attention...

    - The Midbrain & Retic. Formation: 

   <img src="C:\Users\23112\Downloads\3.png" width="40%">

   1. Midbrain: controls eye movements, visual and auditory reflexes(听觉).
   2. Reticular formation: modulates muscle reflexes, breathing & pain perception. Also regulates sleep, wakefulness & arousal.

   - Thalamus & Hypothalamus:

   <img src="C:\Users\23112\Downloads\4.png" width="40%">

   1. Thalamus: “Relay station” for all sensory info (except smell) to the cortex, regulates sleep/wakefulness.
   2. Hypothalamus: Regulates basic needs fighting, fleeding, feeding, and mating.

   - The Cerebrum: consist of cerebral cortex, basal ganglia, hippocampus, and amygdala.

   <img src="C:\Users\23112\Downloads\5.png" width="40%">

   1. involved in perception and motor control, cognitive functions, emotion, memory, and learning.
   2. Cerebral cortex is a layered sheet of neurons, it convoluted surface of cerebrum, about 1/8th of an inch think.
      - It has six layers of neurons, realtively unifrom in structure.

   <img src="C:\Users\23112\Downloads\6.png" width="40%">