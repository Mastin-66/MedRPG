# Medical Phrase Grounding with Region-Phrase Context Contrastive Alignment
Implementation for the MICCAI 2023 paper **"Medical Phrase Grounding with Region-Phrase Context Contrastive Alignment"**[[ArXiv link](https://arxiv.org/abs/2303.07618)].  

#### News: In 2024.6.20, we added a web access interface for MedRPG.
#### News: In 2023.8.15, we first released the code of MedRPG.

***
![Image Text](https://github.com/eraserNut/MedRPG/blob/master/figures/framework.png)
## Environment
As shown in ```requirements.txt```

## Get to know MedRPG
Users can utilize MedRPG directly by accessing the [web interface](https://annotation.evydlab.com/). The system supports image uploads by users, allowing them to obtain a corresponding grounded image based on the entered phrase.

## Try a demo with our pretrained checkpoint
1. Download our [released checkpoint](https://drive.google.com/file/d/1STt5oG52YenG3XLYyjOm13HsVdFLrKKv/view?usp=sharing) to folder ```released_checkpoint```
2. Modify line 144,145,146 in ```demo.py``` to config the input (we put some images in the folder ```data_demo```)
3. Run ```demo.py``` and the output image will be saved in ```demo_cases```

## Train and Test
1. Download the pretrained baseline model to folder ```pretrained``` (include [DETR pretrained model](https://drive.google.com/file/d/1ZhDVssCXjm5ZnfObeF9eCtj9C90G1c-D/view?usp=sharing) and [TransVG pretrained model](https://drive.google.com/file/d/1xDd19fFEmvl0uzs8LmMM6OFXkO5ZjTsU/view?usp=sharing))
2. Download the [MS_CXR dataset](https://drive.google.com/file/d/1ATalb6PKdCJL1XXPIWlO_lEhYWNa8iQI/view?usp=sharing) to folder ```ln_data```
3. Run the script ```script_ours_MS_CXR.sh``` to train, val and test our model, models will be saved in folder ```checkpoint```

## Citation
@inproceedings{chen23MedRPG,   
&nbsp;&nbsp;&nbsp;&nbsp;  author = {Chen, Zhihao and Zhou, Yang and Tran, Anh and Zhao, Junting and Wan, Liang and Ooi, G.S.K. and Cheng, L.T.-E. and Thng, C.H. and Xu, Xinxing and Liu, Yong and Fu, Huazhu},    
&nbsp;&nbsp;&nbsp;&nbsp;  title = {Medical Phrase Grounding with Region-Phrase Context Contrastive Alignment},    
&nbsp;&nbsp;&nbsp;&nbsp;  booktitle = {MICCAI},    
&nbsp;&nbsp;&nbsp;&nbsp;  year  = {2023}    
}
