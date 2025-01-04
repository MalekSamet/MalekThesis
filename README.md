# Thesis Repository 

## Contribution
This work aims for augmenting a dataset (SANPO) in terms of weather conditions and e-scooters. It provides training, inference and evaluation of the whole work.

## Overview
This repository serves as a guide to effectively use and manage a suite of interconnected projects. Each project focuses on a specific aspect of the workflow, and this document provides clear instructions for setup, usage, and integration.

---

## Features
This repository enables users to perform the following tasks:
1. **Train ALDM on SANPO**
2. **Inference ALDM on SANPO**
3. **Run Image Captioning w/ BLIP**
4. **Inference Inpaint_Anything**
5. **Segmentation Model for Evaluation**

---

## Submodules and Conda Environments
This repository consists of the following submodules, each with its corresponding Conda environment (All environments are in the folder "/environment" and they have also copies in their corresponding repositories):

1. **[repo1]https://github.com/MalekSamet/ADLM-Laajim.git** 
   - Conda Environment: `environment_ALDM.yml`

2. **[repo2]https://github.com/MalekSamet/BLIP_laajim.git** 
   - Conda Environment: `environment_ALDM.yml`

3. **[repo3](https://github.com/your-username/repo3)** 
   - Conda Environment: `env_repo3`

4. **[repo4](https://github.com/your-username/repo4)** 
   - Conda Environment: `env_repo4`

5. **[repo5](https://github.com/your-username/repo5)** 
   - Conda Environment: `env_repo5`

---

## Setup Instructions
To get started, clone this repository along with its submodules:
For HTTPS:

```bash
git clone --recurse-submodules https://github.com/MalekSamet/MalekThesis.git
cd meta-repo
```
For SSH:

```bash
git clone --recurse-submodules git@github.com:MalekSamet/MalekThesis.git
cd meta-repo
```

## Features Usage
1. **Train ALDM on SANPO**

First, we need environment_ALDM.yml:
```bash
cd ADLM_Laajim
conda env create -f environment.yml
conda activate ALDM
```
Before starting the training, ensure that the dataset has the following structure in the folder dataset/:
### SANPO Original:
sanpo │ ├── images │ ├── train │ └── val │ └── annotations ├── train └── val
### SANPO Edit (3 extra classes for snow, bench & billboard):
sanpo │ ├── images │ ├── train │ └── val │ └── processed_annotations ├── train └── val

