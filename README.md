# GCBI Breast Cancer Models
This is a document providing information about the GCBI Breast Cancer Models.
Note - these models require a set of Python utilities to run, which are not currently available to the public. 

## Overview
The GCBI Breast Cancer model is a deterministic model which describes the costs and health impacts of implementing various early-detection strategies, including early-awareness campaigns, clinical breast examination, and mammographic screening. The model is deterministic, meaning that we effectively dictate what will happen during the running of the model. The basis of the deterministic model are inputs, which are obtained through a review of the relevant literature, and this may be updated from time to time. 

## The scenarios
There are four scenarios which are modelled:
1. Baseline
2. Baseline + early awareness campaign
3. Baseline + early awareness campaign + screening
  a. Where screening is led by mammography
  b. Where screening is led by clinical breast exam

These four scenarios can be compared incrementally, meaning you can subtract a scenario from another scenario to see the incremental difference in costs and health impacts.
- Scenario 2 - Scenario 1 = Incremental costs and impact of early awareness campaigns
- Scenario 3 - Scenario 2 = Incremental costs and impact of screening

## 1 - The Baseline scenario
## 2 - The early awareness campaign scenario
## 3 - The screening scenarios
### 3a - Mammography led screening
### 3b - Clinical breast exam led screening
