# Unified settings in the interpretation of cross-domain remote sensing scenes（Scene recognition and Target Recognition）
# Introduction：
  Due to the lack of cross-domain benchmark datasets for remote sensing scene interpretation, in order to effectively evaluate the performance of remote sensing scene and target cross-domain recognition 	
models,existing methods usually simulate cross-domain scenarios based on multiple remote sensing dataset screening categories. 
  In this work, we suggest a unified cross-domain setup and try to perform a unified cross-domain setupfor remote sensing scene and target recognition datasets to facilitate the subsequent research in this field. 
In this project, we provide a cross-domain remote sensing dataset with a unified setup, and 
select some mainstream methods to do some simple comparative experiments on this dataset and the corresponding evaluation indexes, the specific information can be found in the following citations for more 
details：“**Zheng X T, Xiao X L, Chen X M, Lu W X, Liu X Y and Lu X Q. 2023. Advancements in cross-domain remote sensing scene interpretation research.** **Journal of Image and Graphics**. ”
# Benchmark：
  We give the corresponding cross-domain setup datasets based on two different decoding tasks-scene recognition, target recognition, respectively
  
  ## 1.Scene Recognition：
  Six datasets were selected as components of our benchmark dataset：[BigEarthNet](http://bigearth.net/)、[RIS-CB](https://github.com/lehaifeng/RSI-CB)、[Optimal-31](http://crabwq.github.io/)、[UC-Merced](http://weegee.vision.ucmerced.edu/datasets/landuse.html)[WHU-RS19](http://captain.whu.edu.cn/datasets/WHU-RS19.zip)、[PatternNet](https://sites.google.com/view/zhouwx/dataset). We choose [BigEarthNet](http://bigearth.net/) and [RIS-CB](https://github.com/lehaifeng/RSI-CB) as standard target domains, and other four datasets are suggested as source domains for cross-domain scene recognition validation by constructing the source-target domains.
   
Subsequently, the selected datasets were unified and organized to merge similar semantic classes. In order to further refine the experimental setup across domains, we organized the category labels of the above selected base datasets
![image](https://github.com/Xiaoxl52/Interpretation-of-cross-domain-remote-sensing-scenes/assets/149050649/5babe8be-e5eb-4c7d-aa67-492eb738196b)
 ## 2.Target Recognition：
  目标识别跨域设置主要包含可见光跨域目标识别设置、可见光-SAR跨域目标识别设置。
  ### a.可见光跨域目标识别设置
  由于不同的数据采集策略和遥感技术，各个遥感图像目标检测数据集在数据上存在显著的差异我们选择现有工作常用的三个数据集NWPU VHR-10、DIOR、HRRSD。
 
  ![image](https://github.com/Xiaoxl52/Interpretation-of-cross-domain-remote-sensing-scenes/assets/149050649/276370da-2737-4e0f-a75a-abbe281cdc38)
  
  我们将三个数据集的目标分布进行量化，进而选出最合适的源域数据集以及目标域数据集
  ![image](https://github.com/Xiaoxl52/Interpretation-of-cross-domain-remote-sensing-scenes/assets/149050649/3f59568d-ff35-4e86-94ab-e8fd4a01660a)

  从表中我们可以看出，在目标的分布上，三者存在较大差异但有着各自明显的特征。相对其他两个数据集，NWPU-VHR-10中目标的有着分布散目标小视角丰富的特点，并且NWPU VHR-10数据集的空间分辨率相较于DIOR、HRRSD数据集有较大的差异化，对检测的精度来说存在一定的挑战性，因此，我们建议选择NWPU-VHR-10为目标域数据集，而把DIOR与HRRSD作为源域。
  
  ### b.可见光-SAR跨域目标识别设置
  在构建跨域设置时，我们尽可能选择成像差异巨大的两个数据集作为源域和目标域，使得跨域算法研究更加关注目标本身的认知信息，学习最能代表目标特性的知识。在对大量的论文进行调研之后，目标域选择两个SAR图像数据集，包括HRSID和SSDD；由于选取的目标数据集均为船舰目标的SAR图像为例，因此我们在选取源域目标数据集时应当考虑该属性，因此HRSC2016仅包含船舰目标的数据集可作为源域数据集之一，另一方面为了保证任务影响因素可控，源域数据集应当在除了模态不同的情况下其他属性如目标尺寸、分布状态等尽可能与目标域保持一致，因此我们通过对数据的分析选取了DIOR数据集以及HRRSD数据集作为可选数据集进行模型的有效性评估。表6中对各个数据集的样本属性进行了分析，最终我们建议HRSC2016→HRSID为一组实验设置，DIOR→SSDD为一组实验设置，而HRRSD数据由于其较低的空间分辨率可作为HRSID目标域的备选源域设置或各组的辅助数据集使用。
  ![image](https://github.com/Xiaoxl52/Interpretation-of-cross-domain-remote-sensing-scenes/assets/149050649/33df9032-7088-417e-bde4-46e91a663716)

  
    

  
