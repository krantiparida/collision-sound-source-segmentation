# Segmenting Collision Sound Sources in Egocentric Videos
This is the codebase for our paper [Segmenting Collision Sound Sources in Egocentric Videos](https://krantiparida.github.io/projects/cs3.html).


[Kranti Kumar Parida](https://krantiparida.github.io), [Omar Emara](https://omar-emara.github.io/), [Hazel Doughty](https://hazeldoughty.github.io/) [Dima Damen](https://dimadamen.github.io)

Links: [[arXiv]]() [[webpage]](https://krantiparida.github.io/projects/cs3.html)

![supported versions](https://img.shields.io/badge/python-3.x-brightgreen/?style=flat&logo=python&color=green)
![Library](https://img.shields.io/badge/library-PyTorch-blue/?style=flat&logo=pytorch&color=informational)
![GitHub license](https://img.shields.io/cocoapods/l/AFNetworking)

## Abstract
Humans excel at multisensory perception and can often recognise object properties from the sound of their interactions. Inspired by this, we propose the novel task of Collision Sound Source Segmentation (CS3), where we aim to segment the objects responsible for a collision sound in visual input (i.e. video frames from the collision clip), conditioned on the audio. This task presents unique challenges. Unlike isolated sound events, a collision sound arises from interactions between two objects, and the acoustic signature of the collision depends on both. We focus on egocentric video, where sounds are often clear, but the visual scene is cluttered, objects are small, and interactions are brief. 

To address these challenges, we propose a weakly-supervised method 
for audio-conditioned segmentation, utilising
foundation models (CLIP and SAM2).
We also incorporate egocentric cues, i.e. objects in hands, to find acting objects that can potentially be collision sound sources. Our approach outperforms competitive baselines by $3\times$ and $4.7\times$ in mIoU on two benchmarks we introduce for the CS3 task: EPIC-CS3 and Ego4D-CS3.
<!-- ![](./figures/teaser.jpg) -->
![](./figures/approach.jpg)


### Data
We provide start and end point for all the collision segments along with the video id for respective datasets. You can use these information to extract the collision sources from the corresponding video. 
For validation, we have provide the image frame along with the segmenation mask in the links below.
| Dataset   | Download Link |
|-----------|:--------------|
| EPIC-CS3  | [gdrive-epic-cs3-data](https://drive.google.com/drive/folders/1bdXCFJDg9xJ989vZLdH5eifShadUCHKK?usp=sharing) |
| Ego4D-CS3 | [gdrive-ego4d-cs3-data](https://drive.google.com/drive/folders/1HHMwXTGG55gWvidn_zbTDMAy1u9t-ryP?usp=sharing) |


## Citation
If using this work please consider citing our paper.
```
@InProceedings{parida2025segmenting,
title = {Segmenting Collision Sound Sources in Egocentric Videos},
author = {Parida, Kranti Kumar and Emara, Omar and Doughty, Hazel and Damen, Dima},
booktitle={ArXiv},
year = {2025},
}
```

Also cite the original EPIC-KITCHENS-100 and Ego4D paper (where the videos originate), the VISOR paper (from which we adopt some of the segmentation annotations), the Ego4DSounds paper (from which we adopt some of the ego4d audio segments).
```
@article{Damen2022RESCALING,
           title={Rescaling Egocentric Vision: Collection, Pipeline and Challenges for EPIC-KITCHENS-100},
           author={Damen, Dima and Doughty, Hazel and Farinella, Giovanni Maria  and and Furnari, Antonino 
           and Ma, Jian and Kazakos, Evangelos and Moltisanti, Davide and Munro, Jonathan 
           and Perrett, Toby and Price, Will and Wray, Michael},
           journal   = {International Journal of Computer Vision (IJCV)},
           year      = {2022},
           volume = {130},
           pages = {33–55},
           Url       = {https://doi.org/10.1007/s11263-021-01531-2}
} 
```
```
@inproceedings{grauman2022ego4d,
  title={Ego4d: Around the world in 3,000 hours of egocentric video},
  author={Grauman, Kristen and Westbury, Andrew and Byrne, Eugene and Chavis, Zachary and Furnari, Antonino and Girdhar, Rohit and Hamburger, Jackson and Jiang, Hao and Liu, Miao and Liu, Xingyu and others},
  booktitle={Proceedings of the IEEE/CVF conference on computer vision and pattern recognition},
  pages={18995--19012},
  year={2022}
}
```
```
@article{darkhalil2022epic,
  title={Epic-kitchens visor benchmark: Video segmentations and object relations},
  author={Darkhalil, Ahmad and Shan, Dandan and Zhu, Bin and Ma, Jian and Kar, Amlan and Higgins, Richard and Fidler, Sanja and Fouhey, David and Damen, Dima},
  journal={Advances in Neural Information Processing Systems},
  volume={35},
  pages={13745--13758},
  year={2022}
}
```
```
@inproceedings{chen2024action2sound,
  title={Action2sound: Ambient-aware generation of action sounds from egocentric videos},
  author={Chen, Changan and Peng, Puyuan and Baid, Ami and Xue, Zihui and Hsu, Wei-Ning and Harwath, David and Grauman, Kristen},
  booktitle={European Conference on Computer Vision},
  pages={277--295},
  year={2024},
  organization={Springer}
}
```

## License
MIT