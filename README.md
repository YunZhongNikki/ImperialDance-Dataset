# ImperialDance-Dataset
The official Dataset proposed in "DanceMVP:Self-Supervised Learning for Multi-Task Primitive-Based Dance Performance Assessment via Transformer Text Prompting” [AAAI 2024].


## Table of Content
* Dataset Introduction
* Dataset Download
* Dataset Formation
* Citation

## Dataset Introduction
We developed **ImperialDance**, which comprises 69,300 seconds of dance motions and music, **5 genres**, **20 pieces of music** and **20 choreographies** with dancers of **3 different expertise levels**.\
Two advantages of our dataset could be summarized as:\
(i) It is the first dataset that describes the expertise level differences of dancing, which promotes the research on dacning skill assessment. \
(ii) Compared to other dance-music datasets that only provide one sample of the dance motion per choreography, we provide 100 repeating samples for each class (per music, per genre, per choreography and expertise level). This will benefit the feature learning of particular dance motions and level progression modeling. 

## Dataset Formation
We collect 69,300 seconds of dance sequences from 5 different dance genres and 20 different dance chorographies with 5 subjects from 3 different expertise levels performed the same task for 100 repeated times. There are two types of data in the dataset: dance motion and music.
### Dance Motion
For the dance motion, the data is collected by using OptiTrack motion capture devices, where the motion camera record the coordinates of 21 skeletal body joints in 3D space in each frame with 100fps. All the dance sequences have been normalized in 10-seconds. We provide the numpy array of each collected dance sequences, where the format of the array is [100,3,1000,21]([samples,coordinates,10seconds\*100fps,joints]).
### Dance Music

## Dataset Download

## Citation
```
@inproceedings{zhong2024dancemvp,
  title={Self-Supervised Learning for Multi-Task Primitive-Based Dance Performance Assessment via Transformer Text Prompting},
  author={Zhong, Yun and Demiris, Yiannis},
  booktitle={Proceedings of the AAAI Conference on Artificial Intelligence},
  volume={xx},
  number={x},
  pages={xxxx--xxxx},
  year={2024}
}
```
