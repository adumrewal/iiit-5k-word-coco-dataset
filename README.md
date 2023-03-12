### Overview
This repository contains the [IIIT5K](https://cvit.iiit.ac.in/research/projects/cvit-projects/the-iiit-5k-word-dataset) dataset. The original dataset shared by IIIT is in matlab format. In this repository, we have converted the dataset to readable `.csv` and `coco` format for easy loading into `python` codes.

#### This dataset contains:
1. Cropped word images split into training and test sets
2. Ground truth annotation, small and medium sized lexicons
3. Lexicon with 0.5 million words (from Weinman et al. 2009)
4. Character bounding box level annotations

The lexicon used to compute language priors is in the file `sample/og_labels/lexicon.txt`. This lexicon was provided by Weinman et al. 2009. The cited [article](https://github.com/adumrewal/iiit-5k-word-coco-dataset#lexicon) should be cited when using this lexicon.

### Sample dataset
#### Train dataset
|img_1||img_2||img_3||img_4|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|<img src="./sample/images/train/6_7.jpg" alt="drawing" width="150"/>||<img src="./sample/images/train/440_2.jpg" alt="drawing" width="150"/>||<img src="./sample/images/train/195_5.jpg" alt="drawing" width="150"/>||<img src="./sample/images/train/13_2.jpg" alt="drawing" width="150"/>|

#### Test dataset
|img_1||img_2|
|:-:|:-:|:-:|
|<img src="./sample/images/test/3_1.jpg" alt="drawing" width="150"/>||<img src="./sample/images/test/14_1.jpg" alt="drawing" width="150"/>|

### Folder structure
- `sample/` : contains sample dataset structure to help understand what you're downloading
    - `images/` : images folder with train/test split
    - `labels/` : labels folder with train/test split in coco format
    - `og_labels/` : original label files shared by the authors in csv format.
        - `lexicon.txt`
        - `testCharBound.csv`
        - `testdata.csv`
        - `trainCharBound.csv`
        - `traindata.csv`
    - `test.txt` : list of test image files (coco format)
    - `train.txt` : list of train image files (coco format)

### Steps to access complete dataset:
- Clone this repo: `git clone https://github.com/adumrewal/iiit-5k-word-coco-dataset.git`
- Setup [git-lfs](https://git-lfs.com/)
    -  `sudo apt-get install git-lfs` or `brew install git-lfs`
    - `git lfs install` (inside the cloned repo)
- `git lfs pull`    (pulls the `.zip` file onto your system)
- `unzip IIIT5K_coco.zip -d .`

### Post Script
- Thanks to [IIIT5K](https://cvit.iiit.ac.in/research/projects/cvit-projects/the-iiit-5k-word-dataset) for open-sourcing the dataset.
- Incase you need the script to convert from `csv` to `coco` format, please feel free to reach out.
- If you have any comments/suggestions, please feel free to drop an e-mail or raise an issue in this repo.
- If you like what I've provided here, it would be great if you could star this repo.

### Citations
#### IIIT-5K Dataset
Please mention the following citation if you plan on using this dataset. More details can be found on original dataset webpage.
```
@InProceedings{MishraBMVC12,
 author   = "Mishra, A. and Alahari, K. and Jawahar, C.~V.",
 title    = "Scene Text Recognition using Higher Order Language Priors",
 booktitle= "BMVC",
 year     = "2012"
}
```
#### Lexicon
```
@article{Weinman09,
    author = {Jerod J. Weinman and Erik Learned-Miller and Allen Hanson},
    title  = {Scene Text Recognition using Similarity and a Lexicon with Sparse Belief Propagation},
    journal= {IEEE Trans. Pattern Analysis and Machine Intelligence},
    volume = {31},
    number = {10},
    pages  = {1733--1746},
    month  = {Oct},
    year   = {2009}
}
```