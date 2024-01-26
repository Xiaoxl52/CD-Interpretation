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
  Target recognition cross-domain settings mainly include visible cross-domain target recognition settings, and visible-SAR cross-domain target recognition settings.
  ### a.Visible cross-domain target recognition setup
   Due to different data acquisition strategies and remote sensing technologies, there are significant data differences among the various remote sensing image target detection datasets We choose three datasets commonly used in existing work NWPU VHR-10, DIOR, and HRRSD.
 
  ![image](https://github.com/Xiaoxl52/Interpretation-of-cross-domain-remote-sensing-scenes/assets/149050649/276370da-2737-4e0f-a75a-abbe281cdc38)
  
  We quantify the target distributions of the three datasets and thus select the most appropriate source domain dataset as well as the target domain dataset
  
  ![image](https://github.com/Xiaoxl52/Interpretation-of-cross-domain-remote-sensing-scenes/assets/149050649/3f59568d-ff35-4e86-94ab-e8fd4a01660a)

  From the table, we can see that in the distribution of the targets, the three datasets are quite different but have their own distinctive features. Relative to the other two datasets, the distribution of targets in NWPU-VHR-10 is characterized by the richness of scattered targets and small viewpoints, and the spatial resolution of the NWPU VHR-10   dataset is more differentiated than that of the DIOR and HRRSD datasets, which is challenging for the accuracy of the detection, so we suggest choosing NWPU-VHR-10 as the target domain dataset and DIOR and HRRSD as the source domain dataset. and DIOR and HRRSD as the source domain.
  
  ### b.Visible-SAR cross-domain target recognition setup
   When constructing the cross-domain setup, we choose two datasets with huge differences in imaging as source and target domains as much as possible, which makes the cross-domain algorithm research pay more attention to the cognitive information of the target itself and learn the knowledge that best represents the target characteristics. After 
 researching a large number of papers, two SAR image datasets are selected for the target domain, including HRSID and SSDD; since the selected target datasets are all SAR images of ship targets as an example, we should consider this attribute when selecting the target dataset for the source domain, so the HRSC2016 dataset which contains only ship 
 targets can be one of the source domain datasets, on the other hand, in order to ensure that the mission impact factors are controllable, the source domain dataset should be consistent with the target domain as much as possible in other attributes such as target size, distribution state, etc., except for the modal difference, so we selected the DIOR 
 dataset and the HRRSD dataset as the optional dataset for the evaluation of the model's validity through the analysis of the data.
  
  ![image](https://github.com/Xiaoxl52/Interpretation-of-cross-domain-remote-sensing-scenes/assets/149050649/cb4bd296-0a10-49ac-89d3-4e3fc19b1467)

   The sample properties of each dataset are analyzed in the table, and ultimately we recommend HRSC2016→HRSID as a set of experimental settings, DIOR→SSDD as a set of experimental settings, and the HRRSD data can be used as an alternative source domain setting for the HRSID target domains or as an auxiliary dataset for each group due to its lower spatial resolution.

  
    

  
