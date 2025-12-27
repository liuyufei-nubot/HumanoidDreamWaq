# DreamWaQ

## Description
This repo is built upon [DreamWaq](https://github.com/Manaro-Alpha/DreamWaQ)

This project has been migrated to the Unitree G1 12-degree-of-freedom robot.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
  
## Installation
This repo requires the following packages:
- [Isaac Gym](https://developer.nvidia.com/isaac-gym)
- Legged Gym
- RSL-RL

To install Isaac Gym, go to the link and follow the instructions on the page.

1. clone this repo

2. 
```bash
  cd rsl_rl-1.0.2
  pip install -e .
  cd ..
```
3. 
```bash
  cd legged_gym
  pip install -e .
  cd ..
```

## Usage
To train your robot run
```bash
    python3 legged_gym/scripts/train.py --task=[robot name]  
```  

If you wish to implement blind stair climbing on the G1 robot
```bash
    python3 legged_gym/scripts/train.py --task=g1 --headless
```  

To evaluate the trained policy run
```bash
    python3 legged_gym/scripts/play.py --task=g1 (--load_run=xxxx --checkpoint=xxxx)
```  

For example, we provide pretrained checkpoints for g1 and go1:
```bash
    python3 legged_gym/scripts/play.py --task=g1 --load_run pretrained --num_envs=1
    python3 legged_gym/scripts/play.py --task=go1 --load_run pretrained --num_envs=1
```  

## Configuration
Requires python 3.8 and numpy version<=1.24.  Recommend numpy==1.21.1

