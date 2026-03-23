<p>
<h2 align="center">3D multiplane SIM (3D-MP-SIM)<sub> Python </sub></h2>
</p>

<p align="center"><strong>Associated paper:</strong> <a href="https://doi.org/10.1038/s41566-025-01638-9">Fast, three-dimensional, live-cell super-resolution imaging with multiplane structured illumination microscopy</a></p>
<p align="center"><strong>Dataset:</strong> <a href="https://doi.org/10.6084/m9.figshare.28280615">https://doi.org/10.6084/m9.figshare.28280615</a></p>

## Recommended Hardware
- **OS**: Windows 11 or Windows 10
- **CPU**: Intel(R) Core(TM) i5-10400 CPU @ 2.90GHz
- **RAM**: 64GB DDR4 (2666MHz)
- **GPU**: NVIDIA GeForce RTX 4060 Ti (16 GB)
- **Storage**: 512GB

or

- **OS**: MacOS 12.6.7
- **CPU**: Intel Core i7
- **RAM**: 16GB
- **GPU**: Intel Iris Plus Graphics 655 1536MB
- **Storage**: 500GB

## Environment Requirements
- **Python**: 3.9.20
- **numpy**: 1.26.4
- **torch**: 2.5.1
- **tifffile**: 2023.7.18
- **opencv-python**: 4.8.0.74
- **EMD-signal**: 1.4.0
- **scikit-image**: 0.22.0
- **pyotf**: 0.0.3
- **Tools**:
  - **Anaconda** (https://www.anaconda.com/download/success)
  - **Visual Studio Code** (https://code.visualstudio.com/)

## Installation
- **Step 1**: Install Anaconda on your computer.

After installing Anaconda, Windows users should open **Anaconda Powershell Prompt**, while Mac users should open **Terminal**. Then enter the following commands and type `y` to confirm when prompted.

- **Step 2**: Create a Python environment with Anaconda.

```bash
conda create -n 3DMPSIM python==3.9.20
```

Activate this environment:

```bash
conda activate 3DMPSIM
```

- **Step 3**: Install the CPU version of PyTorch.

```bash
conda install pytorch torchvision torchaudio cpuonly -c pytorch
```

<!--
Alternatively, if your computer has a GPU (16GB or more memory) and CUDA installed, you can try installing the GPU version of PyTorch for better performance (make sure to match the appropriate CUDA version).
For example, if your CUDA version is 11.8, use the following command (for other versions, please refer to the official website):

```bash
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
```
-->

- **Step 4**: Install the required Python packages with `pip` and run each line separately.

`pip install numpy==1.26.4`

`pip install tifffile==2023.7.18`

`pip install opencv-python==4.8.0.74`

`pip install EMD-signal==1.4.0`

`pip install scikit-image==0.22.0`

`pip install pyotf==0.0.3`

The environment configuration is complete. You can now close the command line window.

**Note**: Please install the above packages **in order**, and use `pip list` to verify the package versions after installation, especially ensuring that the version of **numpy is less than 2.0**. If the installation order is incorrect and runtime errors occur, try recreating the environment and reinstalling the packages in the correct order.

## Visual Studio Code Setup
- **Step 1**: Install Visual Studio Code on your computer.
- **Step 2**: Install three extensions: **Pylance**, **Python**, and **Python Debugger**.

<div align="center">
  <img src="./assets/VScode-setting.jpg" alt="Visual Studio Code setup" width="30%">
</div>

## Run the Program
Please download the code and the registered eight-plane raw data, then open the project folder.

The raw data is available at: https://doi.org/10.6084/m9.figshare.28280615

<div align="center">
  <img src="./assets/VScode-program-1.jpg" alt="Open the project folder" width="60%">
</div>

Click the main script (**main-UI.py**) and then select the previously configured Python environment (**3DMPSIM**) in the bottom right corner.

<div align="center">
  <img src="./assets/VScode-program-2.jpg" alt="Select Python environment" width="60%">
</div>

Run **main-UI.py** to launch the main interface.

<div align="center">
  <img src="./assets/VScode-program-3.jpg" alt="Run the main interface" width="60%">
</div>

## Reconstruction Data
Follow the steps below:

1. Click the **Select Folder** button.
2. Select the **raw data** folder downloaded from the dataset link above. Do not enter subfolders.
3. Input the Wiener parameter. The default Wiener parameter for the example data is `0.0001`.
4. Click the **Run** button and wait for the program to complete.
   Approximate runtime on CPU is 10 minutes, during which the main interface may become unresponsive.
5. When the program finishes, a message box will show the location of the result files.
6. `Wiener_results.tif` is the reconstructed image.

<div align="center">
  <img src="./assets/UI-1234.jpg" alt="Main interface workflow" width="100%">
</div>

<div align="center">
  <img src="./assets/UI-56.jpg" alt="Reconstruction results interface" width="100%">
</div>

## Contributors
Contributions to this project include:
- Huang Xiaoshuai (&#40644;&#23567;&#24069;), Peking University, Beijing, China
- Fan Junchao (&#33539;&#39567;&#36229;), Chongqing University of Posts and Telecommunications, Chongqing, China

## Contact
For any questions or comments about this code, please contact <a href="mailto:hxs@hsc.pku.edu.cn">hxs@hsc.pku.edu.cn</a>.

## Copyright and Software License
Copyright (c) 2025 @ Huang Lab, Peking University, Beijing, China

The package is licensed under the [GNU GPL](https://www.gnu.org/licenses/).
