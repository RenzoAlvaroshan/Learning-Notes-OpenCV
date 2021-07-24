# Learning Notes OpenCV Installation

Learning Notes - Build and Install OpenCV With CUDA GPU Support on Windows 10 | OpenCV 4.5.1 | 2021 (TheCodingBug channel) (YouTube Com, 2021) $$$$$

Source: YouTube Com (2021) - Build and Install OpenCV with CUDA GPU Support on Windows 10 | OpenCV 4.5.1 | 2021 (TheCodingBug channel) $$$$$

---

Purpose: installing OpenCV 4.5.1 with GPU Support

**Steps**:
1. Setup Pre-requisities
2. OpenCV with CUDA in Base Environment
3. OpenCV with CUDA in Virtual Environment
  > Can be different Python version than Base Environment

--------------------

## 01 Setup Pre-Requisite

### (1) Anaconda Installer

Download Anaconda Installer:
anaconda.com/products/individual



Next, download `Visual Studio Community 2019 16.7.2'





Select `Desktop development with C++' option for Studio Code C++ support

--------------------

## (2) Cuda Toolkit Update

Now download `CUDA Toolkit 11.0 Update Downloads':

developer.nvidia.com/cuda-11.0-update1-download-archive?target_os=Windows&target_arch=x86_64



Choose `Windows' operating system for Select Target Platform.



Choose `CUDA Toolkit 11.0 Update 1 Downloads':



Choose the following options:

	⁃	Operating System: `Windows’
	⁃	Architecture: x86_84
	⁃	Version: 10
	⁃	Installer Type: exe (local)







Click `Download cuDNN v8.0.5 (November 9th, 2020), for CUDA 11.0' to expand the driver list:



Click `cuDNN Library for Windows (x86)' now the driver will be downloading.

Extract the driver file (.zip) you just downloaded:



Then copy the extracted files and folder inside `cudnn-11.0-windows-x64-v8.0.5.39' to:

(C:) › Program Files › NVIDIA GU Computing Toolkit › CUDA › v11.0 >



Here you will replace some files and folders with new ones:

	•	bin
	•	include
	•	lib
	•	NVIDIA_SLA_cuDNN_Support.txt



--------------------

(3) CMake GUI App 

Now download CMake GUI app:

cmake.org/download/



Choose files `cmake-3.19.3-win64-x64.msi’, then run the installer to setup CMake in your computer.







--------------------

(4) OpenCV Setup

Create a folder for OpenCV in you C: drive:

OpenCV_Build

Next, download source code of `OpenCV-4.5.1’ from:

opencv.org/releases/

Choose: `sources'



It will bring you to OpenCV repository in GitHub:

github.com/opencv/opencv/archive/4.5.1.zip 

Save it in folder `OpenCV_ Build' you just created:



Next, go to `opencv_contrib' folder in GitHub:

github.com/opencv/opencv_contrib



Click `Relase' button



Download OpenCV version `4.5.1.zip’ also save it in folder `OpenCV_ Build':



Now, extract both .zip files:

opencv_contrib-4.5.1.zip
opencv-4.5.1.zip



Now run CMake GUI app:



In `Where is the source code:'  click `Browse' to choose the folder of files to be compiled:



Select `(C:) › OpenCV_Build › opencv-4.5.1 >' folder



In `Where to build the binaries'  click `Browse' to choose the folder of files for the output.
Create a new sub-folder named `build'

C:/OpenCV_Build/build



Then make sure that `Grouped’ option is checked:



And click `Configure' button:



Choose:

• Specify the generator for this project: `Visual Studio 16 2019'
• Optional platform for generator(if empty, generator uses: x64): `x64'
• Use default native compilers = checked



Then click `Finish’.

CMake GUI app will start to build your OpenCV:



Upon finish, search keyword `python' to make sure that your OpenCV is built for `Anaconda':



Now check that the OpenCV modules is `Unavailable' for `python3'



If you don’t fix this, you will encounter the most common error `ModuleNoteFoundError' when you try to `import OpenCV' as shown below:



This is due to mismatch of Numpy version. We can fix it by by updating Numpy.



First, delete cache file from `File | Delete Cache' menu:



Then, run Anaconda prompt – choose `Run as administrator’:



Then run the following command to upgrade Numpy version to `1.19.5':

C: \WINDOWS \system32>pip install-upgrade numpy

Now hit `Configure' button again to re-configure CMake app:



Now you’ll see additional information in Python3 module:



Also, in OpenCV module:



Now let’s start the configuration.

Search `WITH_CUDA' keyword then enable its checkbox



Similarly with other parameters:

`OPENCV DNN CUDA'



`ENABLE FAST MATH'



`BUILD opency_world'



`opency_python'



Next, set the folder for `OPENCV_EXTRA_MODULES_PATH' by clicking three-dot […] button





--------------------
tag: #learning #notes #build #install #opencv #cuda #gpu #support #windows #2021 #thecodingbugchannel #youtube #$$$$$
