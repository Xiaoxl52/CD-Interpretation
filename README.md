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
  
  ## 1.scene recognition：
  Six datasets were selected as components of our benchmark dataset：[BigEarthNet](http://bigearth.net/)、[RIS-CB](https://github.com/lehaifeng/RSI-CB)、[Optimal-31](http://crabwq.github.io/)、[UC-Merced](http://weegee.vision.ucmerced.edu/datasets/landuse.html)[WHU-RS19](http://captain.whu.edu.cn/datasets/WHU-RS19.zip)、[PatternNet](https://sites.google.com/view/zhouwx/dataset). We choose [BigEarthNet](http://bigearth.net/) and [RIS-CB](https://github.com/lehaifeng/RSI-CB) as standard target domains, and other four datasets are suggested as source domains for cross-domain scene recognition validation by constructing the source-target domains.
   
Subsequently, the selected datasets were unified and organized to merge similar semantic classes. In order to further refine the experimental setup across domains, we organized the category labels of the above selected base datasets
![image](https://github.com/Xiaoxl52/Interpretation-of-cross-domain-remote-sensing-scenes/assets/149050649/5babe8be-e5eb-4c7d-aa67-492eb738196b)
 ## 2.target recognition：
 

  
