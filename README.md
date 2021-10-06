<!-- PROJECT LOGO -->
<br />
<p align="center">
    <img src="figures/title.PNG" alt="Logo" width="900" height="120">
</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#experiments">Experiments</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## About The Project

We present ConvTract, a DCNN-based framework for automatic whole-brain fiber tractography. The introduced model comprises 3D and 2D convolutional layers to regress the fiber Orientation Distribution Functions that are subsequently utilized to perform deterministic tractography using SD-Stream algorithm. The introduced pipeline was evaluated in terms of fODF estimation accuracy and tractography generalizability. Moreover, the framework was scored using the Tractometer tool, a publicly available tractography benchmark, for quantitative assessment of tractography quality. The obtained results showed that this approach outperforms classical and current state-of-the-art data-driven tractography algorithms.





<!-- USAGE  -->
## Usage
Here we provide a simple example for training and tracking.
### training
 ```sh
python3 convtract.py 'train' sample-data/dwi/ -labels sample-data/sh.nii.gz -bm sample-data/bm.nii.gz -wm sample-data/wm.nii.gz -save_dir ./
 ```
### tracking
 ```sh
python3 convtract.py 'track' sample-data/dwi/ -bm sample-data/bm.nii.gz -wm sample-data/wm.nii.gz -trained_model_dir ConvTract.hdf5 
```

Refer to _[help.txt](help.txt)_ for more details.


<!-- EXPERIMENTS -->
## Experiments

We tested our program on differents DWI data and confirmed that our pipeline performs high quality tractography.
<p align="center">
    <img src="figures/1.PNG" alt="Logo" width="800" height="600">
</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.




<!-- CONTACT -->
## Contact

S.M.H. Hosseiny - [@twitter](https://twitter.com/sotospeakk?s=09) - hosseiny290@gmail.com


