# ImperialDance-Dataset
The official Dataset proposed in "DanceMVP: Self-Supervised Learning for Multi-Task Primitive-Based Dance Performance Assessment via Transformer Text Prompting” [AAAI 2024].
Paper: [DanceMVP](https://ojs.aaai.org/index.php/AAAI/article/view/28893)

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
(ii) Compared to other dance-music datasets, which only provide one sample of the dance motion per choreography, we provide 100 repeating samples for each class (per music, genre, choreography, and expertise level). This will benefit the feature learning of particular dance motions and level progression modeling. 

## Dataset Formation
We collected 69,300 seconds of dance sequences from 5 different dance genres and 20 different dance chorographies with 5 subjects from 3 different expertise levels performed the same task 100 repeated times. The dataset has two types of data: dance motion and music.
### Dance Motion
For the dance motion, the data is collected using OptiTrack motion capture devices, where the motion camera records the coordinates of 21 skeletal body joints in 3D space in each frame at 100fps. All the dance sequences were normalized in 10 seconds. We provide the numpy array of each collected dance sequence, where the format of the array is (100,3,1000,21)  (samples, coordinates,10seconds\*100fps, joints).\

To view the dance skeletons, the index of the 21 body joints are described as below:\
Skeleton_Name = [RShin, RToe, RThigh, LThigh, LFoot, RShoulder, LHand, RHand, LFArm, LShoulder, RFoot, Neck, LShin, Chest, Head, LToe, Ab, RUArm, LUArm, Hip, RFArm].


Each dance sequence is named as format: **dance_level_[expertise_level]\_[genre]\_[choreography]**

For example, a dance sequence that describes the performance of Ballet choreography 0 performed by an Expert is named as dance_level_e_b_ch0.

This dataset has three different expertise levels: Expert, Intermediate and Beginner. Their short forms are e, i, and b, respectively.\
There are five dance genres: Ballet, K-pop, Jazz, Hip-Hop, and Urban. We use the letters b,k,j,h, and u to represent them in the file name, respectively.\
There are a maximum of five choreographies for each dance genre. We use ch0-ch4 to represent five different choreographies for each genre.
### Dance Music
We provide the Youtube ID or Bilibili ID for each dance music piece belonging to each choreography in the dataset. Dancers from all levels(Expert, Intermediate, and Beginner) have danced to the same choreography 100 repeating times.

K-Pop Choreography 0 (k_ch0): Youtube ID: WhHEQ-W3x5Y, music/choreography from 0:40 to 0:55. \
K-Pop Choreography 1 (k_ch1): Youtube ID: WhHEQ-W3x5Y, music/choreography from 0:55 to 1:10.\
K-Pop Choreography 2 (k_ch2): Youtube ID: T28Av5QZtUc, music/choreography from 1:20 to 1:30. \
K-Pop Choreography 3 (k_ch3): Youtube ID: T28Av5QZtUc, music/choreography from 1:10 to 1:20.\
K-Pop Choreography 4 (k_ch4): Youtube ID: DMOaEdw4KJM&t, music/choreography from 0:15 to 0:27. 

Ballet Choreography 0 (b_ch0): Youtube ID: ZLxIM2OpCdc, music/choreography from 1:50 to 2:05. \
Ballet Choreography 1 (b_ch1): Bilibili ID: BV1fN411f71F, music/choreography from 1:10 to 1:25.\
Ballet Choreography 2 (b_ch2): Bilibili ID: BV1fN411f71F, music/choreography from 0:55 to 1:10.\
Ballet Choreography 3 (b_ch3): Youtube ID: WYF-D6nsHyQ, starts from 1:07 to 1:25. \
Ballet Choreography 4 (b_ch4): Youtube ID: WYF-D6nsHyQ, starts from 0:33 to 0:58.   

Jazz Choreography 0 (j_ch0): Bilibili ID: BV1tW4y1t75U, music/choreography from 0:00 to 0:20.\
Jazz Choreography 1 (j_ch1): Bilibili ID: BV1XR4y1w7qT, music/choreography from 0:00 to 0:20.\
Jazz Choreography 2 (j_ch2): Bilibili ID: BV1DD4y1v7ag, music/choreography from 0:10 to 0:28.\
Jazz Choreography 3 (j_ch3): Bilibili ID: BV1jv4y1z7Lt - 《change》, music/choreography from 0:00 to 0:16.

Hip-Hop Choreography 0 (h_ch0): Bilibili ID: BV1sa411F7JZ - 《time goes by》, from 0:00 to 0:15.\
Hip-Hop Choreography 1 (h_ch1): Bilibili ID: BV1L84y1r7tk, from 0:00 to 0:17.

Urban Choreography 0 (u_ch0): Youtube ID: 96Xd1lzbfLk, music/choreography from 0:40 to 0:55.\
Urban Choreography 1 (u_ch1): Bilibili ID: BV1jv4y1z7Lt - 《insomnia》, music/choreography from 0:00 to 0:18.\
Urban Choreography 2 (u_ch2): Youtube ID: 1MwNg2pQS6w, music/choreography from 0:05 to 0:20. \
Urban Choreography 3 (u_ch3): Bilibili ID: BV1jv4y1z7Lt - 《Timber》, from 0:00 to 0:20.

## Dataset Download
The dance motion can be downloaded here: ([https://drive.google.com/drive/folders/1kSndi7ZIljpue_EzYXOpxZenHi52nujL?usp=sharing](https://drive.google.com/drive/folders/1kSndi7ZIljpue_EzYXOpxZenHi52nujL?usp=sharing)).\
As for the music, we have the corresponding Youtube IDs/Bilibili IDs in the previous section.

## Citation
```
@inproceedings{zhong2024dancemvp,
  title={DanceMVP: Self-Supervised Learning for Multi-Task Primitive-Based Dance Performance Assessment via Transformer Text Prompting},
  author={Zhong, Yun and Demiris, Yiannis},
  booktitle={Proceedings of the AAAI Conference on Artificial Intelligence},
  volume={38},
  number={9},
  pages={10270--10278},
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
