癫痫是最常见且最慢性的神经系统疾病之一。覆盖全年龄段。由于缺乏单一的确诊标准或生物标志物，其诊断高度依赖病史与多项临床测试。这种**多维度证据整合**的特性，使得流行病学研究极易产生误差，因此明确研究人群的背景对获取准确的患病率数据至关重要。

> Epilepsy is one of the most prevalent chronic neurological disorders, affecting individuals across all age groups. Due to the absence of a singular diagnostic criterion or biomarker, its diagnosis relies heavily on the integration of clinical history and various diagnostic tests. This multifaceted nature of diagnostic evidence inherently predisposes epidemiological research to potential errors. Consequently, a clear understanding of the target population's background is essential for deriving accurate incidence and prevalence data.

Hello everyone, we are group 4, teammate is LIjun, KANGzerui and Liqile . Our presentation topic is: Expert-level detection of Epileptiform discharge on EEG.

Let me start with the first part: Background and Study Design.

Epilepsy is one of the most prevalent **chronic neurological** disorders, affecting individuals across all age groups. Epileptiform discharges, **characterized** by d**istinctive spiky** or **sharp wave morphologies**, serve as key biomarkers of epilepsy. The common signal is spike wave which is clinically detected using EEG .

**Electroencephalogram** is the gold standard for the diagnosis of epilepsy by captures subtle voltage waves. In clinical practices, these bioelectrical signal are typically recorded using a standardized 19-channel **montage.**

However, several bottlenecks severely limit the efficiency of EEG diagnosis in various situations. First, there is a significant shortage of clinical resources, which places great pressure on diagnosis. Second, results are highly affected by expert subjectivity, leading to **inconsistency.** Third, manual diagnosis can take up to 30 continuous minutes per case, which is very **inefficient**.

Therefore, we propose using an automated model to solve these problems., The main challenges are: How to build a robust model to **precisely** locate epilepsy foci while making fully EEG data, and how to improve model performance by effectively reduce **false positives**?

We design a SpikeNet2 model. We cut the entire dataset from 30 minutes EEG-level recordings into 1 second event-level patches and perform multi-category analysis on the full EEG content. For the dataset, we selected three datasets including: MGB, HEP and SAI, to evaluate model **generalizability**, and split them into event-level and EEG-level subsets.

About the data preprocessing, We use four method include data resampling ,channel conversion, signal segmentation, and **amplitude** normalization. Theses steps help  the model to focus on **salient features** while controlling complexity.

Next is our model architecture.

---

临床上，棘波是判断有没有癫痫、癫痫病灶在大脑哪个位置的核心依据，棘波是一种**异常尖刺样电波**，存在散发性棘波和周期性放电等类型，其中**周期性放电**是一种临床上常见于重症监护者的明确癫痫异常放电类型。

> Clinically, **spike waves** serve as the pivotal diagnostic markers for identifying epilepsy and localizing the underlying focus. A spike wave is characterized as an **abnormal, sharp-contoured electrical discharge**. It encompasses various subtypes, such as sporadic spikes and **periodic discharges (PDs)**; the latter is a distinct type of epileptiform abnormality frequently observed in critically ill patients within intensive care settings.



EEG 是癫痫诊断的**金标准**，其中**痫样放电（棘波）**是判定癫痫及皮层过度兴奋的关键生物标志物。对于确诊患者，EEG 的主要临床意义在于通过电生理特征，将发作类型区分为局灶性或全身性，并辅助判定特定的癫痫综合征。

> For diagnosed patients, the primary clinical significance of EEG lies in its ability to classify seizure types as either focal or generalized based on electrophysiological characteristics, further assisting in the identification of specific epilepsy syndromes.

从电生理机制来看，EEG是通过记录施加在头皮上的电极电位，捕捉微弱的**电位波动**。这些电位主要源于大脑皮层中垂直排列的**大型锥体神经元**，是大量兴奋性突触后电位（EPSP）与抑制性突触后电位（IPSP）**空间总和**的结果。

> "From an electrophysiological perspective, EEG captures subtle voltage fluctuations by recording electrode potentials applied to the scalp. These potentials primarily originate from large, vertically oriented pyramidal neurons within the cerebral cortex, representing the spatial summation of numerous excitatory postsynaptic potentials (EPSPs) and inhibitory postsynaptic potentials (IPSPs).

在临床实践中，这种生物电信号通常采用 **19通道（基于 10-20 国际标准系统）** 进行标准化记录，以确保电极覆盖能够全面反映大脑各区域的功能状态。

> In clinical practice, these bioelectrical signals are typically recorded using a standardized **19-channel configuration (based on the International 10-20 System)** to ensure that the electrode coverage comprehensively reflects the functional status of various cortical regions.

理解发作间期和发作期脑电图的生理基础，还有助于了解不同类型癫痫的病理生理和治疗方法。但全球超 7000 万癫痫患者中，多数地区缺乏专业神经电生理医生，人工 EEG 判读存在**高误诊率、高阅片者间差异**的问题。

> Understanding the physiological basis of interictal and ictal EEG is essential for gaining insights into the pathophysiology and treatment of different types of epilepsy. However, among the more than 70 million epilepsy patients worldwide, most regions suffer from a severe shortage of specialized neurophysiologists. Consequently, manual EEG interpretation is plagued by **high misdiagnosis rates and significant inter-rater variability**.

Understanding the physiological basis of **interictal and ictal EEG** is crucial for gaining insights into the pathophysiology and treatment of various epilepsy types.

However, with over 70 million patients globally and a severe shortage of neurophysiologists, manual EEG interpretation is plagued by **high misdiagnosis rates** and **significant inter-rater variability**.



How to enhance detection accuracy across various seizure levels and intensities?

How to build a robust system to precisely pinpoint epileptogenic foci?

How to fully leverage multi-channel EEG data for comprehensive feature extraction?

How to improve performance by effectively eliminating physiological and environmental noise?

How to manage class imbalance to ensure stable and unbiased model training?