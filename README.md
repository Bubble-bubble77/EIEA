# KDD submission
This repository is the official implementation.


# Environment
The essential package and recommened version to run the code:
```
pip install -r EIEA-env.txt
```

# Dataset
The **MMEA-data** and **ECS-results** can be download from  [GoogleDrive](https://drive.google.com/drive/folders/1wfErYdAV93yxPtPHqkGanbmb_Ztv-LRU?usp=drive_link).
The original MMEA dataset can be download from  [MMKB](https://github.com/mniepert/mmkb) and [MMEA](https://github.com/lzxlin/mclea?tab=readme-ov-file).
Those files should be organized into the following file hierarchy:
```
EIEA
├── data
│   └── ECS_results
|        └── seed0.2
|              └── FB15K-DB15K
|              └── FB15K-YAGO15K
|        └── seed0.5
|        └── seed0.8
|   └── MMEA_name
|   └── MMEA-data
|        └── seed0.2
|              └── FB15K-DB15K
|              └── FB15K-YAGO15K
|        └── seed0.5
|        └── seed0.8
└── src
└── DBP15K_src
└── ECS_compute

```
**NOTE**
Based on the URLs given in the original dataset, we use crawling techniques to obtain entity name information. However, due to the unavailability of some URLs, the name information of certain entities in FB15K is missing. 
All entity name information can be found in **MMEA_name**.

# Run EIEA
python runxxx.py DATASET RATE 

For example: 
```
python run0.2.py FB_YAGO 0.2
python run0.2.py FB_DB 0.2
python run0.2.py FB_DB 0.5
```
# EIEA on FB-DB/ FB-YAGO
![image](https://github.com/BubbleWang-wly/EIEA/blob/main/MMKG_result.jpg?raw=true)

# EIEA On DBP15K
![image](https://github.com/BubbleWang-wly/EIEA/blob/main/dbp_result.jpg?raw=true)

# Run EIEA on DBP15K
```
cd DBP15K_src
python run.py zh_en
python run.py ja_en
python run.py fr_en
```
# Note
In FB-YG and FB-DB :
  Name/Att: use Roberta_finetuning_semantic_similarity_stsb_multi_mt

In DBP:
  Name: use Roberta_finetuning_semantic_similarity_stsb_multi_mt
  Att: use LaBSE



