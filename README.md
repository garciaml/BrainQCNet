# BrainQCNet : Detection of Artifacts on Brain T1-weighted Scans
# <img src="https://github.com/garciaml/BrainQCNet/blob/master/T1_low_quality_2.jpg" width="3000px">

BrainQCNet is a software that automatically detects the presence of defaults on brain structural MRI scans. 

It is based on a Deep Learning algorithm, you can find more details on how it was built on the paper [here](https://doi.org/10.1101/2022.03.11.483983).

To run BrainQCNet on your data, you can either use the BIDS-app that:
- works on **Nvidia GPU machines with CUDA [here](https://github.com/garciaml/BrainQCNet/blob/master/BrainQCNet_GPU/)**,
- works on **CPU machines [here](https://github.com/garciaml/BrainQCNet/tree/master/BrainQCNet_CPU)**.

A list of Nvidia GPUs with CUDA technology is provided [here](https://developer.nvidia.com/cuda-gpus).

<p align="center"> :bell: <b>We strongly recommend users to run the app on a machine with CUDA-compatible GPU ! </b> :bell: </p>

### Explicative videos
Videos are available on YouTube in order to guide you when using BrainQCNet: 
- [GPU & CUDA users](https://www.youtube.com/watch?v=dSyHAcg8d8I)
- [CPU users](https://www.youtube.com/watch?v=Snv3d6SXfDQ)

### How to report errors
Users can get help using the [brainqcnet-users mailing list](https://groups.google.com/g/brainqcnet-users).

All bugs, concerns and enhancement requests for this software can be submitted [here for the GPU version](https://github.com/garciaml/BrainQCNet_GPU/issues) and [here for the CPU version](https://github.com/garciaml/BrainQCNet_CPU/issues).

### Citation
When using BrainQCNet, please include the following citation:

*BrainQCNet: A Deep Learning attention-based model for the automated detection of artifacts in brain structural MRI scans.*, Mélanie Garcia, Nico Dosenbach, Clare Kelly;  Imaging Neuroscience 2024; 2 1–16. doi: https://doi.org/10.1162/imag_a_00300
