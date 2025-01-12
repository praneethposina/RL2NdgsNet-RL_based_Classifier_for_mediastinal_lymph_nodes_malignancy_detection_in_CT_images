# RL2NdgsNet: Reinforcement learning based efficient classifier for mediastinal lymph nodes malignancy detection in CT images

A deep reinforcement learning approach for detecting malignancy in mediastinal lymph nodes from CT images.

## Overview

RL2NdgsNet is a novel reinforcement learning-based deep learning network designed for diagnosing mediastinal lymph nodes (MLNs) as either benign or malignant. The model provides a non-invasive alternative to traditional biopsy procedures for cancer detection.

### Key Features

- Custom DQN (Deep Q-Network) policy architecture
- CNN-based feature extraction
- Experimentation with various activation functions and exploration fractions
- High accuracy in binary classification (benign vs malignant)

## Performance Metrics

The model achieves state-of-the-art performance:

- Sensitivity: 98.03%
- Specificity: 98.35% 
- Accuracy: 98.2%
- AUC: 98.19%

This represents significant improvements over baseline CnnPolicy:
- Accuracy: +5.69%
- Sensitivity: +4.78%
- Specificity: +7.25%
- AUC: +6.01%


## Technical Details

### Implementation
- Platform: Google Colab
- Deep Learning Framework: Keras
- Reinforcement Learning Library: Stable-baselines
- Architecture: Custom CNN Extractor + Leaky ReLU + Layer Normalization (ε=0.8) + Deep Q Network (DQN)

### Training Process
- Training set: 5400 images
- 5-fold cross validation
- Replay buffer initialization: First 1000 steps
- Regular weight replication between Q and T networks (every 500 steps)

## Citation

If you use this work in your research, please cite:

BibTeX
```
@INPROCEEDINGS{9984560,
  author={Praneeth, Posina and Lakshmi, Abothula Dhana and Tekchandani, Hitesh and Verma, Shrish and Londhe, Narendra D.},
  booktitle={2022 13th International Conference on Computing Communication and Networking Technologies (ICCCNT)}, 
  title={RL2NdgsNet: Reinforcement learning based efficient classifier for mediastinal lymph nodes malignancy detection in CT images}, 
  year={2022},
  volume={},
  number={},
  pages={1-5},
  keywords={Sensitivity;Computed tomography;Reinforcement learning;Cancer detection;Planning;Task analysis;Lymph nodes;Reinforcement learning;Lymph nodes;Deep learning;Cancer;CT},
  doi={10.1109/ICCCNT54827.2022.9984560}}
```
