# GCBI Breast Cancer Models
This is a document providing information about the GCBI Breast Cancer Models.
Note - these models require a set of Python utilities to run, which are not currently available to the public. 

## Overview
The GCBI Breast Cancer model is a deterministic model which describes the costs and health impacts of implementing various early-detection strategies, including early-awareness campaigns, clinical breast examination, and mammographic screening. The model is deterministic, meaning that we dictate what will happen during the running of the model.
We dictate the running of the model through assumptions, which are obtained through a review of the relevant literature, expert opinion, and calibrating the model to real-world observations.
These assumptions may change over time, in which case they will be documented in the commits.

## Scenarios: An overview
There are four scenarios which are modelled:
1. Baseline
2. Baseline + early awareness campaign
3. Baseline + early awareness campaign + screening
    a. Where screening is led by mammography
    b. Where screening is led by clinical breast exam

These four scenarios can be compared incrementally, meaning you can subtract a scenario from another scenario to see the incremental difference in costs and health impacts.
- Scenario 2 - Scenario 1 = Incremental costs and impact of early awareness campaigns
- Scenario 3 - Scenario 2 = Incremental costs and impact of screening

The models need to run for at least fifteen years, to demonstrate gradual scale-up of screening interventions. In this documentation, we index the years from 0, where 0 is the first year of the model running. 

## 1 - The Baseline scenario
The baseline scenario models the current country situation. We model this as a pool of cases, some of which are undiagnosed, some of which are diagnosed at a certain stage (Stages I-IV). All cases may die, and treated cases may recover, or receive palliative care. From this baseline scenario, we modify how many people are diagnosed, and the stage at which they are diagnosed. 

## 2 - The early awareness campaign scenario
Compared to the [Baseline scenario](#1-the-baseline-scenario), we model the costs and effects of the early awareness campaign. The effects are a shift in stage at diagnosis, an increased incidence.

### Stage Shift and increased diagnoses
Over the first five years of the implementation, we implement the early awareness campaign. Over this time, we see an increased proportion of diagnoses which are in early stages (Stage I and II breast cancer), and proportionally fewer cases which are in later stages (Stage III and IV). We also find more cases of breast cancer, because we are raising awareness.

## 3 - The screening scenarios
Compared to the [early awareness campaign scenario](#2-the-early-awareness-campaign-scenario), there are no changes to the mechanisms. However, we assume a strong stage shift, increased diagnoses, and new costing structures. Importantly, we make the assumption that screening scenarios *must happen after an early awareness campaign*. Therefore, these costs and benefits are not alternative strategies, but potential strategies after the original early awareness campaign has taken place. 

### 3a - Mammography led screening
Mammography led screening has the strongest stage shift (the highest proportion of cancers diagnosed in early stages), the largest number of cases diagnosed, and the largest costs. 

### 3b - Clinical breast exam led screening
Clinical breast exam screening has a stronger stage shift than the early awareness campaign, but less than mammography led screening. However, there are fewer associated costs. 
