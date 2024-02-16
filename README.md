# ImperialDance-Dataset
The official Dataset proposed in "DanceMVP:Self-Supervised Learning for Multi-Task Primitive-Based Dance Performance Assessment via Transformer Text Prompting” [AAAI 2024].

![p](https://github.com/YunZhongNikki/ImperialDance-Dataset/blob/main/new_frameworkk_large-1.png)

## Table of Content
* [Dataset Introduction](Dataset-Introduction)
* [Dataset Formation](Dataset-Formation)
* [Dataset Download](Dataset-Download)
* [Citation](Citation)

## Dataset Introduction
![dataset_sample](https://github.com/YunZhongNikki/ImperialDance-Dataset/blob/main/dataset_sample.png)
We developed **ImperialDance**, which comprises 69,300 seconds of dance motions and music, **5 genres**, **20 pieces of music** and **20 choreographies** with dancers of **3 different expertise levels**.\
Two advantages of our dataset could be summarized as:\
(i) It is the first dataset that describes the expertise level differences of dancing, which promotes the research on dacning skill assessment. \
(ii) Compared to other dance-music datasets that only provide one sample of the dance motion per choreography, we provide 100 repeating samples for each class (per music, per genre, per choreography and expertise level). This will benefit the feature learning of particular dance motions and level progression modeling. 

## Dataset Formation
We collect 69,300 seconds of dance sequences from 5 different dance genres and 20 different dance chorographies with 5 subjects from 3 different expertise levels performed the same task for 100 repeated times. There are two types of data in the dataset: dance motion and music.
### Dance Motion
For the dance motion, the data is collected by using OptiTrack motion capture devices, where the motion camera record the coordinates of 21 skeletal body joints in 3D space in each frame with 100fps. All the dance sequences have been normalized in 10-seconds. We provide the numpy array of each collected dance sequences, where the format of the array is (100,3,1000,21)  (samples,coordinates,10seconds\*100fps,joints).\

Each dance sequence is named as format: **dance_level_[expertise_level]\_[genre]\_[choreography]**

For example, a dance sequence that describes the performance of Ballet choreography 0 performed by an Expert is named as dance_level_e_b_ch0.

There are three different expertise levels in this dataset: Expert, Intermediate and Beginner. The short form of them are: e,i,b respectively.\
There are five different dance genres: Ballet, K-Pop, Jazz, Hip-Hop, Urban. We use letters: b,k,j,h,u to represent them in the file name respectively.\
There are maximum five choreography for each dance genre, we use ch0-ch4 to represent 5 different choreographies for each genre.
### Dance Music
We provide YoutubeID for each dance music that belongs to each choreography in the dataset. Dancers from all the levels(Expert, Intermediate and Beginner) have danced to the same choreography for 100 repeating times.

Ballet Choreography 0 (b_ch0):\
Ballet Choreography 1 (b_ch1):\
Ballet Choreography 2 (b_ch2):\
Ballet Choreography 3 (b_ch3):\
Ballet Choreography 4 (b_ch4):

K-Pop Choreography 0 (k_ch0):\
K-Pop Choreography 1 (k_ch1):\
K-Pop Choreography 2 (k_ch2):\
K-Pop Choreography 3 (k_ch3):\
K-Pop Choreography 4 (k_ch4):

Jazz Choreography 0 (j_ch0):\
Jazz Choreography 1 (j_ch1):\
Jazz Choreography 2 (j_ch2):\
Jazz Choreography 3 (j_ch3):

Hip-Hop Choreography 0 (h_ch0):\
Hip-Hop Choreography 1 (h_ch1):

Urban Choreography 0 (u_ch0):\
Urban Choreography 1 (u_ch1):\
Urban Choreography 2 (u_ch2):\
Urban Choreography 3 (u_ch3):

## Dataset Download
The dance motion can be downloaded here:LINKS\
As for the music, please find the corresponding YoutubeIDs in the previous section.

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
```
@INPROCEEDINGS{10096824,
  author={Zhong, Yun and Zhang, Fan and Demiris, Yiannis},
  booktitle={ICASSP 2023 - 2023 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)}, 
  title={Contrastive Self-Supervised Learning for Automated Multi-Modal Dance Performance Assessment}, 
  year={2023},
  volume={},
  number={},
  pages={1-5},
  keywords={Humanities;Self-supervised learning;Signal processing;Robustness;Task analysis;Speech processing;Motion analysis;Human Motion analysis;Action Performance Assessment;Multi-modal Signal Processing},
  doi={10.1109/ICASSP49357.2023.10096824}}
```
