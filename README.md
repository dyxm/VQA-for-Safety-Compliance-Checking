# Safety compliance checking of construction behaviors using visual question answering (VQA)

[Paper](https://www.sciencedirect.com/science/article/pii/S0926580522004502#f0025) | [Citation](#citation) | [Dataset](#data)


## Introduction
Unsafe construction behavior, one of the leading factors of accidents and casualties, can be reduced by strengthening construction inspection. However, current methods use either manual inspection or inefficient cross-modal models based on multiple backbone networks. To alleviate the problems, a “rule-question” transformation and annotation system is formulated, and the unsafe behavior detection is turned into a visual reasoning task: visual question answering (VQA). The VQA model is developed based on a vision-and-language Transformer, and the unsafe behavior could be identified based on the output answers. A dataset containing 16 safety rules and 2386 related construction images is used to fine-tune and validate the VQA model. The results show that the developed VQA model achieves an average recall of 0.81 at a faster reasoning speed. Finally, an applet for safety report generation is implemented to demonstrate the feasibility and practicability of the safety compliance checking based on VQA.


## Method
Figure 1 demonstrates the research framework of this study, including data preparation, VQA modeling, and safety report generation. Firstly, some common construction safety rules and the onsite images related to the rules are collected. According to specific procedures, the rules are then converted into corresponding questions, and the answers to the questions are labeled based on the image content. After data preparation, a VQA model based on the ViLT pre-trained on large public datasets continues to be fine-tuned on the collected data to complete the reasoning task. Category balance and parameter optimization are conducted during modeling to obtain a better model. Finally, a safety compliance checking system based on visual reasoning is implemented, automatically generating the safety report for each image using answers predicted by the optimal VQA model.

![image](https://github.com/user-attachments/assets/41817bd9-972a-4617-8239-ada7690e9a12)

<div align="center">Figure 1. Research framework.</div>
<br>
<br>


## Data
The dataset used in this study can be accessed:
- at the [TeraBox download link](https://terabox.com/s/1pOcERrkL866GqayeeCfC4Q).
- or, at the [Baidu Netdisk download link]() using the code: **j80v**

![image](https://github.com/user-attachments/assets/342af909-4ee8-4dbe-ac3a-57a6e546d850)

<div align="center">Figure 4. Sample images with unsafe construction behaviors.</div>


## The implemented system for automatic safety compliance checking of construction behaviors

![image](https://github.com/user-attachments/assets/c6f5b67d-9236-4133-a5de-0a22c928f76b)
![image](https://github.com/user-attachments/assets/d9f4b437-deba-4fb2-af89-0ffd22fd030c)
![image](https://github.com/user-attachments/assets/dca1c185-fbf7-4209-8ac1-572f4d820ec3)


## Results
![image](https://github.com/user-attachments/assets/7122359c-0a49-4906-9743-7942eb5d2cec)

<div align="center">Figure 6. Examples with totally correct detection results.</div>
<br>
<br>


![image](https://github.com/user-attachments/assets/78eaa848-20ca-4625-ba6e-83eaca8e2d3e)

<div align="center">Figure 7. Examples with imperfect detections. The false detections are marked with yellow rectangles, and the missed detections are marked with red rectangles.</div>
<br>
<br>


## Citation
If you find this research useful, consider citing it using:
```
@article{DING2022104580,
  title = {Safety compliance checking of construction behaviors using visual question answering},
  journal = {Automation in Construction},
  volume = {144},
  pages = {104580},
  year = {2022},
  issn = {0926-5805},
  doi = {https://doi.org/10.1016/j.autcon.2022.104580},
  url = {https://www.sciencedirect.com/science/article/pii/S0926580522004502},
  author = {Yuexiong Ding and Muyang Liu and Xiaowei Luo},
}
```


