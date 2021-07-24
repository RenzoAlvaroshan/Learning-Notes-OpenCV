# Learning Notes - OpenCV Installation

Learning Notes - Build and Install OpenCV with CUDA GPU Support on Windows 10 | OpenCV 4.5.1 | 2021

Source: [YouTube Com (2021) - Build and Install OpenCV with CUDA GPU Support on Windows 10 | OpenCV 4.5.1 | 2021 (TheCodingBug channel)](https://www.youtube.com/watch?v=YsmhKar8oOc)

---

**Purpose**: installing OpenCV 4.5.1 with GPU Support

**Steps**:
1. Setup Pre-requisities
2. OpenCV with CUDA in Base Environment
3. OpenCV with CUDA in Virtual Environment
  > Can be different Python version than Base Environment

---

## 01 Setup Pre-Requisite

### (1) Anaconda Installer

Download [Anaconda Installer](anaconda.com/products/individual): ```anaconda.com/products/individual```

<img width="1440" alt="Anaconda Installers" src="https://user-images.githubusercontent.com/55566616/126862305-4bf9c0e8-b08f-4043-af9b-3743383f28a4.png">

<img width="490" alt="Anaconda3 2020 11 (64-bit) Setup" src="https://user-images.githubusercontent.com/55566616/126862344-4c2dab10-b0c8-44df-a60e-2480f2d75c7f.png">
<img width="491" alt="ANACONDA  Choose the folder in which to instal Anaconda3 2020 11 (64-bit)" src="https://user-images.githubusercontent.com/55566616/126862348-409286e2-6648-4f38-8917-55f68b22d734.png">
<img width="492" alt="Anaconda3 2020 11 (64-bit) Setup" src="https://user-images.githubusercontent.com/55566616/126862350-e348542b-7c5d-4bf3-8b91-b775248fa60a.png">
<img width="494" alt="Anaconda3 2020 11 (64-bit) Setup" src="https://user-images.githubusercontent.com/55566616/126862351-30e796ad-1f3b-4ceb-8404-673a6c1cbf54.png">
<img width="496" alt="2020 11 (64-bit) Setup" src="https://user-images.githubusercontent.com/55566616/126862355-be434046-0792-4a68-a556-73d1e5eb9948.png">

### (2) Microsoft Visual Studio

Next, download [Visual Studio Community 2019 16.7.2](https://visualstudio.microsoft.com/vs/community/): ```https://visualstudio.microsoft.com/vs/community/```

<img width="1440" alt="components Language packs" src="https://user-images.githubusercontent.com/55566616/126863268-c9f0dd02-4bc3-4408-a886-0dc58b908d85.png">

Select ```Desktop development with C++``` option for Studio Code C++ support

<img width="1440" alt="Installation details" src="https://user-images.githubusercontent.com/55566616/126863270-c24e8363-53b4-405d-b130-51cbd7b83ade.png">

### (3) Cuda Toolkit Update

Now download [CUDA Toolkit 11.0 Update Downloads](developer.nvidia.com/cuda-11.0-update1-download-archive?target_os=Windows&target_arch=x86_64): ```developer.nvidia.com/cuda-11.0-update1-download-archive?target_os=Windows&target_arch=x86_64```

<img width="1440" alt="Resources" src="https://user-images.githubusercontent.com/55566616/126863551-7019a69a-7f41-4b75-bc71-7ee6a98f8afb.png">

Choose ```Windows``` operating system for ```Select Target Platform```.

<img width="1440" alt="CUDA Toolkit Archive" src="https://user-images.githubusercontent.com/55566616/126863557-16f0e0f4-6d68-4004-9386-608281295170.png">

Choose ```CUDA Toolkit 11.0 Update 1 Downloads```:

<img width="1440" alt="CUDA Toolkit 11 0 Update 1 Downloads" src="https://user-images.githubusercontent.com/55566616/126863575-928096f3-e790-4bc5-8eb6-fb0d728b8247.png">

Choose the following options:

* Operating System: ```Windows```
* Architecture: ```x86_84```
* Version: ```10```
* Installer Type: ```exe (local)```

<img width="1440" alt="Pasted Graphic 11" src="https://user-images.githubusercontent.com/55566616/126863930-4190691d-becf-4379-bd5b-90c09b9f3dd2.png">
<img width="1440" alt="Pasted Graphic 12" src="https://user-images.githubusercontent.com/55566616/126863932-eeda04b4-03fa-402f-8944-4c65650a8fd9.png">
<img width="1440" alt="cuDNN Download" src="https://user-images.githubusercontent.com/55566616/126863933-9c7b22b7-f63c-4293-9688-4b22d8dbe9d0.png">

Click ```Download cuDNN v8.0.5 (November 9th, 2020), for CUDA 11.0``` to expand the driver list:

<img width="1440" alt="Library for Windows and Linux, Ubuntulx86_64   PPC architecture)" src="https://user-images.githubusercontent.com/55566616/126863946-19fcb2f6-e307-4fd3-9ef0-c860377ee33d.png">

Click ```cuDNN Library for Windows (x86)``` now the driver will be downloading.

Extract the driver file (.zip) you just downloaded:

<img width="1440" alt="Pasted Graphic 15" src="https://user-images.githubusercontent.com/55566616/126863951-ecae92ed-050c-4e9d-b630-7851aa87ad2b.png">

Then copy the extracted files and folder inside ```cudnn-11.0-windows-x64-v8.0.5.39``` to:

```(C:) › Program Files › NVIDIA GU Computing Toolkit › CUDA › v11.0 >```

<img width="1440" alt="Pasted Graphic 17" src="https://user-images.githubusercontent.com/55566616/126863961-5e1d3db3-6e89-4724-b816-daa72bd57cee.png">

Here you will replace some files and folders with new ones:

* ```bin```
* ```include```
* ```lib```
* ```NVIDIA_SLA_cuDNN_Support.txt```

<img width="1440" alt="Pasted Graphic 16" src="https://user-images.githubusercontent.com/55566616/126863972-8e0c6784-cfd8-4273-9ba1-fe68bca4b165.png">

### (4) CMake GUI App

Now download [CMake GUI](cmake.org/download/) app: ```cmake.org/download/```

<img width="1440" alt="Pasted Graphic 18" src="https://user-images.githubusercontent.com/55566616/126864488-24b131c1-e309-45f0-85d2-62b1e16b339f.png">

Choose files `cmake-3.19.3-win64-x64.msi', then run the installer to setup CMake in your computer.

<img width="419" alt="Open File - Security Warning" src="https://user-images.githubusercontent.com/55566616/126864492-4bbaa155-75b5-40b7-bfcd-111a55fc3e3b.png">
<img width="487" alt="Welcome to the CMake Setup Wizard" src="https://user-images.githubusercontent.com/55566616/126864495-7202ea33-52d9-44c8-aaab-d6e1976e9ea7.png">
<img width="487" alt="Welcome to the CMake Setup Wizard" src="https://user-images.githubusercontent.com/55566616/126864496-e0e5be17-89c3-47e3-94c2-aa520b4348bb.png">

### (5) OpenCV Setup

Create a folder for OpenCV in you ```C:``` drive: ```OpenCV_Build```

Next, download source code of [OpenCV-4.5.1](opencv.org/releases/) from: ```opencv.org/releases/```

Choose: ```sources```

<img width="1440" alt="Releases" src="https://user-images.githubusercontent.com/55566616/126864516-a2b18725-8b62-4961-8b03-13fc0bcd64bd.png">

It will bring you to [OpenCV repository](github.com/opencv/opencv/archive/4.5.1.zip) in GitHub: ```github.com/opencv/opencv/archive/4.5.1.zip```

Save it in folder ```OpenCV_ Build``` you just created:

<img width="1440" alt="Pasted Graphic 24" src="https://user-images.githubusercontent.com/55566616/126864532-3da3c143-4b6f-4dcc-9df1-c888580d959d.png">

Next, go to [opencv_contrib folder] (github.com/opencv/opencv_contrib) in GitHub: ```github.com/opencv/opencv_contrib```

<img width="1440" alt="Pasted Graphic 25" src="https://user-images.githubusercontent.com/55566616/126864546-c4d7ad19-8fe6-45eb-aa31-4ca25343b6d3.png">

Click ```Relase``` button

<img width="1440" alt="Pasted Graphic 26" src="https://user-images.githubusercontent.com/55566616/126864548-d1ffe6ea-0ba7-4da9-a4b0-a0d8f78a3908.png">

Download OpenCV version ```4.5.1.zip``` also save it in folder ```OpenCV_ Build```:

<img width="1057" alt="Pasted Graphic 27" src="https://user-images.githubusercontent.com/55566616/126864558-4b10e14b-e83b-467a-aaa3-0cfd35b28dc2.png">

Now, extract both .zip files:

* ```opencv_contrib-4.5.1.zip```
* ```opencv-4.5.1.zip```

<img width="1440" alt="Pasted Graphic 28" src="https://user-images.githubusercontent.com/55566616/126864568-12e246b0-d469-48b5-a0c6-0258231da39f.png">

Now run CMake GUI app:

<img width="1440" alt="Pasted Graphic 31" src="https://user-images.githubusercontent.com/55566616/126864570-e5cf6c40-c691-4617-b763-aa05cc4f5a0b.png">

In ```Where is the source code:```  click ```Browse``` to choose the folder of files to be compiled:

<img width="1440" alt="Pasted Graphic 32" src="https://user-images.githubusercontent.com/55566616/126864581-6cddf0fe-75cc-46a8-9892-c8f702c72486.png">

Select ```(C:) › OpenCV_Build › opencv-4.5.1 >``` folder

<img width="1108" alt="Pasted Graphic 33" src="https://user-images.githubusercontent.com/55566616/126864583-ac500673-4e77-4dc8-9139-74e7e3fab185.png">

In ```Where to build the binaries```  click ```Browse``` to choose the folder of files for the output.

Create a new sub-folder named ```build```

```C:/OpenCV_Build/build```

<img width="1108" alt="Pasted Graphic 34" src="https://user-images.githubusercontent.com/55566616/126864591-ad9cadbe-6c1d-4fbd-be17-984cd4ab9136.png">

Then make sure that ```Grouped``` option is checked:

<img width="1440" alt="Pasted Graphic 35" src="https://user-images.githubusercontent.com/55566616/126864593-79a8759d-d5dd-47ad-9dd8-f2903a815a58.png">

And click ```Configure``` button:

<img width="1440" alt="Pasted Graphic 36" src="https://user-images.githubusercontent.com/55566616/126864598-45c32717-6fe4-4ef4-8baa-995359237b9b.png">

Choose:

* Specify the generator for this project: ```Visual Studio 16 2019```
* Optional platform for generator(if empty, generator uses: x64): ```x64```
* Use default native compilers = checked

<img width="430" alt="Specify the generator for this project" src="https://user-images.githubusercontent.com/55566616/126864603-9672a899-af58-42ee-af60-1e8d92c3f35c.png">

Then click ```Finish```.

CMake GUI app will start to build your OpenCV:

<img width="1435" alt="Pasted Graphic 39" src="https://user-images.githubusercontent.com/55566616/126864614-6d4d756f-3fd1-4291-92e4-1758adaa17bd.png">

Upon finish, search keyword ```python``` to make sure that your OpenCV is built for `Anaconda':

<img width="1440" alt="Pasted Graphic" src="https://user-images.githubusercontent.com/55566616/126864615-16348cd5-eeac-47e1-8d53-d4a42e8a49ed.png">

Now check that the OpenCV modules is ```Unavailable``` for ```python3```

<img width="1440" alt="Pasted Graphic 1" src="https://user-images.githubusercontent.com/55566616/126864620-f3a35b15-6db9-471d-94c5-17cdc7528436.png">

If you don't fix this, you will encounter the most common error ```ModuleNoteFoundError``` when you try to ```import OpenCV``` as shown below:

<img width="783" alt="Traceback (most recent call last)" src="https://user-images.githubusercontent.com/55566616/126864624-b52f01d0-0770-4e28-9507-a2753940cf68.png">

This is due to mismatch of Numpy version. We can fix it by by updating Numpy.

<img width="1440" alt="Pasted Graphic 3" src="https://user-images.githubusercontent.com/55566616/126864637-03392071-0f06-49f3-9a8b-7286c399ca27.png">

First, delete cache file from `File | Delete Cache' menu:

<img width="356" alt="Reload Cache" src="https://user-images.githubusercontent.com/55566616/126864641-da2f07fc-a919-4b3d-ba0f-4b513a1300a0.png">

Then, run Anaconda prompt -- choose ```Run as administrator```:

<img width="904" alt="Anaconda Prompt (anaconda3)" src="https://user-images.githubusercontent.com/55566616/126864644-304ceccb-5f7a-4f36-84c1-96a676675e2d.png">

Then run the following command to upgrade Numpy version to ```1.19.5```:

```C: \WINDOWS \system32>pip install-upgrade numpy```

Now hit ```Configure`` button again to re-configure CMake app:

<img width="452" alt="Specify the generator for this project" src="https://user-images.githubusercontent.com/55566616/126864648-04e0a3c1-e4d8-41ff-b01c-b3e08debef57.png">

Now you'll see additional information in Python3 module:

<img width="1440" alt="Pasted Graphic 7" src="https://user-images.githubusercontent.com/55566616/126864654-da1a6771-4a37-4d0a-97c0-39e56fbd6b34.png">

Also, in OpenCV module:

<img width="1435" alt="Pasted Graphic 8" src="https://user-images.githubusercontent.com/55566616/126864656-bab199df-e952-468d-8034-ab9134902a6d.png">

Now let's start the configuration.

Search ```WITH_CUDA``` keyword then enable its checkbox

<img width="1440" alt="Pasted Graphic 9" src="https://user-images.githubusercontent.com/55566616/126864664-449743a3-d940-449a-a8c3-5492cfa3f4dd.png">

Similarly with other parameters:

```OPENCV_DNN_CUDA```

<img width="1440" alt="Pasted Graphic 10" src="https://user-images.githubusercontent.com/55566616/126864667-54bd1b00-87b6-431e-a910-6c78cfe843c1.png">

```ENABLE_FAST_MATH```

<img width="1440" alt="Pasted Graphic 11" src="https://user-images.githubusercontent.com/55566616/126864694-75830769-58ef-42eb-8db8-8a84d3768a78.png">

```BUILD_opency_world```

<img width="1440" alt="Pasted Graphic 12" src="https://user-images.githubusercontent.com/55566616/126864695-9dee1f2a-09ba-49ef-8e09-0dd53ec0074a.png">

```opency_python```

<img width="1440" alt="Pasted Graphic 13" src="https://user-images.githubusercontent.com/55566616/126864711-4c866117-33c3-4178-88fa-416d607f18b5.png">

Next, set the folder for `OPENCV_EXTRA_MODULES_PATH' by clicking three-dot [...] button

---

tag: ```#learning``` ```#notes``` ```#build``` ```#install``` ```#opencv``` ```#cuda``` ```#gpu``` ```#support``` ```#windows``` ```#2021``` ```#thecodingbugchannel``` ```#youtube``` ```#$$$$$```
