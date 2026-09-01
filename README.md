# *StructureLDM:*  A Latent Diffusion Model for Sketch-based Structural Analysis 
###### [**Deng Yu**](https://scholar.google.com/citations?user=Yi4KFWwAAAAJ&hl=en)&nbsp;&nbsp; [**Guangtao Liu**]() &nbsp;&nbsp; [**Lin Jiao**]() &nbsp;&nbsp;  [**Yujie Liu***]()&nbsp;&nbsp; [**Zhumin Chen**]() &nbsp;&nbsp; [**Wanchao Su**]() &nbsp;&nbsp;

######  1 School of Artificial Intelligence, Shandong University, Shandong, China
######  2 Qingdao Institute of Software, College of Computer Science and Technology, China University of Petroleum (East China), Shandong Key Laboratory of Intelligent Oil and Gas Industrial Software, China
######  3 SensiLab, Faculty of Information Technology, Monash University, Melbourne, Australia

###### * Corresponding author

###### Accepted by [PG 20206](https://pacificgraphics2026.github.io/)


<img src="img/figure1.pdf" alt="teaser_stress" style="zoom:12%;" />

**Fig. 1 **: Our StructureLDM enables fast, interactive structural analysis across various sketch-based application scenarios by allowing
users to apply forces (red dots) directly on the sketch. (a) shows sketch-based structural analysis for identifying the weak regions (warmer
colors) on the sketched structure. (b) illustrates how our StructureLDM supports users perform structural refinement on these weak regions
of sketches: the upper row presents the progressively refined sketches, while the bottom row shows corresponding stress maps computed by
our system. (c) demonstrates the application of our structural analysis to product sketches in the OpenSketch dataset

## Abstract

In the process of product design and digital fabrication, structural analysis of a designed prototype is a fundamental and essential step. However, such a step is usually invisible or inaccessible to designers at the early sketching phase. This limits the users’ ability to contemplate a shape’s physical properties and structural soundness. To bridge this gap, we introduce a novel approach *Sketch2Stress* that allows users to perform structural analysis of desired objects at the sketching stage, as displayed in Figure 1. This method takes as input a sketch and a point map to specify the location of a user-assigned external force. It automatically predicts a normal map and a corresponding structural stress map distributed over the user-sketched underlying object. In this way, our method empowers designers to easily examine the stress sustained everywhere and identify potential problematic regions over their sketched object. Furthermore, combined with the predicted normal map, users are able to conduct a region-wise structural analysis efficiently by aggregating the stress effects of multiple forces in the same direction. We demonstrate the effectiveness and practicality of our system with extensive experiments and two user studies.

## Interface 

<img src="img/demo.png" alt="demo" style="zoom: 20%;" />

###### **Fig 2**: Our Sketching Interface.


## Pipeline

<img src="img/network_sk2stress.jpg" alt="network_sk2stress" style="zoom:23%;" />

**Fig 3**:  Overview of the multi-branch generator of *Sketch2Stress*. Given an input sketch (upper left) and an input point map (lower left) indicating a force location, the multi-branch generator uses its encoder to learn a sketch-force joint feature space, and then leverages two decoders to synthesize the corresponding stress map (lower branch) and a normal map (upper branch). We use warmer colors (reds and yellows) to show high stress and cooler colors (greens and blues) to show low stress. The normal map infers the force direction at the input force location. A shape mask and a point-attention mask are proposed to further emphasize the shape boundaries and force locations during the generation process.

## Sketch-based Structure Analysis

<img src="img/result_gallery.jpg" alt="result_gallery" style="zoom:14%;" />

**Fig 4**:  Result gallery of eleven categories in our synthetic sketch-to-stress dataset. The top row shows the input sketches and external force locations (plotted as red dots), while the middle and bottom rows are our generated normal maps (with predicted force directions at the center of red boxes) and synthesized stress maps. 

## Structure Refinement without/with our *Sketch2Stress*

<img src="img/user_study-Page-4.png" alt="user_study-Page-4" style="zoom: 12%;" />

**Fig 5**: Each triplet contains a structurally problematic sketch under different force configurations (red dots on sketches), and the user-refined results without and with our tool, respectively. The corresponding stress maps are provided under the refined sketches.

## Structural Analysis on Real Product Sketches

<img src="img/opensketch.jpg" alt="opensketch" style="zoom:16%;" />

###### **Fig 6**: Our *Sketch2Stress* method applied to the OpenSketch dataset. The concept and presentation sketches of the bump, shampoo bottle, and potato chip (in the first, second, and third rows) are from ”Professional1” while the bottom two rows of the tube and the house are from ”Professional5” and ”Professional6” in the OpenSketch dataset. Please zoom in to examine the details.

## Video

<video controls preload="metadata" width="1200" poster="">
  <source src="img/sketch2stress.mp4" type="video/mp4">
  你的浏览器不支持该视频播放
</video>




## Citation 

```tex
@ARTICLE{yu2024sketch2stress,
  author={Yu, Deng and Xiao, Chufeng and Lau, Manfred and Fu, Hongbo},
  journal={IEEE Transactions on Visualization and Computer Graphics}, 
  title={Sketch2Stress: Sketching With Structural Stress Awareness}, 
  year={2024},
  volume={30},
  number={10},
  pages={6851-6865},
  doi={10.1109/TVCG.2023.3342119}
  }
```



<img src="img/SCM_Logo.png" alt="SCM_Logo" style="zoom:50%;" />
