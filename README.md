# Social Media Addiction and Usage Datasets

## Overview

This repository contains three related datasets designed to explore social media behavior and its effects on students:

1. **Students Social Media Addiction Dataset**  
   Survey data capturing student demographics, social media habits, mental health status, and self-reported academic impact.

2. **Social Media Usage Dataset**  
   Quantitative metrics of daily user activity across different social media platforms, including posts, likes, follows, and time spent.

3. **Challenge/Test Dataset**  
   A separate dataset used for evaluating predictive models and generating submissions for academic performance impact challenges.

---

## Dataset Descriptions

### 1. Students Social Media Addiction Dataset
Includes features such as Gender, Academic Level, Country, Average Daily Usage Hours, Most Used Platform, Sleep Hours, Mental Health Score, Relationship Status, Conflicts Related to Social Media, and whether social media affects academic performance.

### 2. Social Media Usage Dataset
Contains User IDs, social media applications used, Daily Minutes Spent, Posts Per Day, Likes Per Day, and Follows Per Day.

### 3. Challenge/Test Dataset
Similar in structure to the training datasets but without target labels, intended for model validation and submission.

---

## Purpose

These datasets provide a comprehensive foundation for analyzing the impact of social media on student well-being and academic performance. They support exploratory data analysis, predictive modeling, and development of interventions to promote healthier social media use.

---

## Usage Instructions

### 1. Load Data

```python
import pandas as pd

# Load datasets
df_addiction = pd.read_csv('path/to/students_social_media_addiction.csv')
df_usage = pd.read_csv('path/to/social_media_usage.csv')
df_test = pd.read_csv('path/to/challenge_test.csv')
