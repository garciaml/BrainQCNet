# BrainQCNet : Detection of Artifacts on Brain T1-weighted Scans
# <img src="https://github.com/garciaml/BrainQCNet/blob/master/T1_low_quality_2.jpg" width="3000px">

BrainQCNet is a software that automatically detects the presence of defaults on brain structural MRI scans. 

It is based on a Deep Learning algorithm, you can find more details on how it was built on the paper [here](https://doi.org/10.1101/2022.03.11.483983).

To run BrainQCNet on your data, you can either use the BIDS-app that works on **Nvidia GPU machines with CUDA [here](https://github.com/garciaml/BrainQCNet/blob/master/BrainQCNet_GPU/)**, or the one that works on **CPU machines [here](https://github.com/garciaml/BrainQCNet/tree/master/BrainQCNet_CPU)**.

A list of Nvidia GPUs with CUDA technology is provided [here](https://developer.nvidia.com/cuda-gpus).

**We strongly recommend users to run the app on a machine with CUDA-compatible GPU !**


### How to report errors
Users can get help using the [brainqcnet-users mailing list](https://groups.google.com/g/brainqcnet-users).

All bugs, concerns and enhancement requests for this software can be submitted [here for the GPU version](https://github.com/garciaml/BrainQCNet_GPU/issues) and [here for the CPU version](https://github.com/garciaml/BrainQCNet_CPU/issues).

### Citation
When using BrainQCNet, please include the following citation:

*BrainQCNet: a Deep Learning attention-based model for multi-scale detection of artifacts in brain structural MRI scans*, Melanie Garcia, Nico Dosenbach, Clare Kelly. bioRxiv 2022.03.11.483983; doi: https://doi.org/10.1101/2022.03.11.483983
