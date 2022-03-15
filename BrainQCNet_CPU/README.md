# Documentation for CPU users

All the code of BrainQCNet for CPU machines is available [here](https://github.com/garciaml/BrainQCNet_CPU).

## Step 1: Install Docker

https://docs.docker.com/get-docker/

## Step 2: Get our docker image
In your terminal, type:
```
docker pull garciaml/brainqcnetcpu:latest
```

## Step 3: Get our best model
In order to be able to run BrainQCNet, please download saved_models.zip that contains our best model [here](https://drive.google.com/file/d/16kmV3B6EM7_8ObRlejyjq18JvPv-KHr2/view?usp=sharing).

You will need to **unzip saved_models.zip**, and to move **saved_models/** to a choosen folder. We will need to refer to the path of this chosen folder when launching the app. 

## Step 4: Run BrainQCNet

**1/ Participant-level**
```
docker run -it --rm -v /home/user/BIDS_data/:/bids_dir:ro -v /home/user/out_brainqcnet/:/out_dir -v /home/user/saved_models/:/saved_models:ro brainqcnetcpu /bids_dir /out_dir participant --modeldir /saved_models/resnet152/19112020/
```
This command-line launches BrainQCNet processing on all the subjects of BIDS_data. It generates folders into out_brainqcnet corresponding to each subject.
In each subject folder in out_brainqcnet, there is six files:
- global_analysis.log: is the global log file containing the prediction of each slice, the global mean and median of predictions, and the percentage of slices predicted class 0 or 1. 
- table.csv: is a table containing 3 columns: "pred" for the prediction, "slice" for the number of the slice, "axis" for the corresponding axis of the slice.
- tot_df.csv: 
- x_results_locally.csv: contains the percentage of slices predicted class 1 (i.e. with artefacts) within chosen ranges of slices on the axis x. The ranges of slices are automatically generated based on the parameter n_areas that enables to gather several slices together and to analyse the predictions into larger areas than each slice separately. By default, n_areas=3, then it creates 3 bins of slices. 
- y_results_locally.csv: similar to x_results_locally.csv but on the y axis.
- z_results_locally.csv: similar to x_results_locally.csv but on the z axis.

Example to set n_areas to 5:
```
docker run -it --rm -v /home/user/BIDS_data/:/bids_dir:ro -v /home/user/out_brainqcnet/:/out_dir -v /home/user/saved_models/:/saved_models:ro brainqcnetcpu /bids_dir /out_dir participant --modeldir /saved_models/resnet152/19112020/ --n_areas 5
```

Example: generating the results of specific subjects 
```
docker run -it --rm -v /home/user/BIDS_data/:/bids_dir:ro -v /home/user/out_brainqcnet/:/out_dir -v /home/user/saved_models/:/saved_models:ro brainqcnetcpu /bids_dir /out_dir participant --modeldir /saved_models/resnet152/19112020/ --participant_label 20001 20003
```
Here, it generates the results for sub-20001 and sub-20003 present into our BIDS_data.


**2/ Group-level**
```
docker run -it --rm -v /home/user/BIDS_data/:/bids_dir:ro -v /home/user/out_brainqcnet/:/out_dir brainqcnetcpu /bids_dir /out_dir group
```
This command-line launches the analysis at the group level: it gathers all the results from the analyses at the participant level, and stores the results into a file called **group_results.csv** into the folder out_brainqcnet.


## Citation
When using BrainQCNet, please cite:

*BrainQCNet: a Deep Learning attention-based model for multi-scale detection of artifacts in brain structural MRI scans*, Melanie Garcia, Nico Dosenbach, Clare Kelly. bioRxiv 2022.03.11.483983; doi: https://doi.org/10.1101/2022.03.11.483983
