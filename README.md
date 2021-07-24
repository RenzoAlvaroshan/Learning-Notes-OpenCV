# Learning Notes - Build and Install OpenCV with CUDA on Windows 10

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

Choose files ```cmake-3.19.3-win64-x64.msi```, then run the installer to setup CMake in your computer.

<img width="419" alt="Open File - Security Warning" src="https://user-images.githubusercontent.com/55566616/126864492-4bbaa155-75b5-40b7-bfcd-111a55fc3e3b.png">
<img width="487" alt="Welcome to the CMake Setup Wizard" src="https://user-images.githubusercontent.com/55566616/126864495-7202ea33-52d9-44c8-aaab-d6e1976e9ea7.png">
<img width="487" alt="Welcome to the CMake Setup Wizard" src="https://user-images.githubusercontent.com/55566616/126864496-e0e5be17-89c3-47e3-94c2-aa520b4348bb.png">

---

## 02 OpenCV with CUDA in Base Environment

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

Upon finish, search keyword ```python``` to make sure that your OpenCV is built for ```Anaconda```:

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

Next, set the folder for ```OPENCV_EXTRA_MODULES_PATH``` by clicking three-dot ```...``` button

<img width="1440" alt="Pasted Graphic 14" src="https://user-images.githubusercontent.com/55566616/126865140-a1b29fd4-0c47-4ec6-b5a0-47b86cafcb7b.png">

Move to modules folder: ```(C:) OpenCV_Build › opencv_contrib-4.5.1 › modules```

<img width="1097" alt="Pasted Graphic 15" src="https://user-images.githubusercontent.com/55566616/126869509-c3b88831-092e-401d-b884-a56a53c3ed60.png">

<img width="1440" alt="Pasted Graphic 16" src="https://user-images.githubusercontent.com/55566616/126869510-1f6dc42c-da7c-4572-9e5c-9674bf43ea03.png">

Hit again the ```Configure``` button. Now CMake should be able to find and detect ```cudnn.lib``` files and its suitable version.
```
- Found cuDNN: C:/Program Files/NVIDIA GPU Computing Toolkit/CUDA/v11.0/11b/x64/cudnn.lib (found suitable version "8.0.5", minimum required is "7.5")
- CUDA detected: 11.0
```

<img width="1440" alt="Pasted Graphic 17" src="https://user-images.githubusercontent.com/55566616/126869565-9e87b3b6-836d-44f2-872f-67a28ec4f82e.png">

Once detection is finished, search ```CUDA_FAST MATH``` keyword then enable its checkbox.

<img width="1440" alt="Pasted Graphic 18" src="https://user-images.githubusercontent.com/55566616/126869575-56e45a8f-2d14-4c60-8613-d00e8480f049.png">

Next, search CUDA architecture property of ```CUDA_ARCH_BIN``` keyword, its value should be read as ```3.5;3.7;5.0;5.2;6.0;6 1;7.0;7.5;8.0```.

<img width="1440" alt="Pasted Graphic 19" src="https://user-images.githubusercontent.com/55566616/126869597-a5c2a2b3-c738-450f-81f2-22e4857e36f4.png">

Now you have to find the CUDA model that suitable with your GPU architecture.

In order to find the right GPU architecture, go to ```Wikipedia``` of CUDA: ```[en.wikipedia.org/wiki/CUDA](http://en.wikipedia.org/wiki/CUDA)``` to find your GPU model

<img width="1440" alt="It is Wikipedia's birthday!" src="https://user-images.githubusercontent.com/55566616/126869627-4bc152b8-9d82-4871-b9cb-b326e4b50946.png">

In this case, we use Nvidia GTX 1000 » then the ```Compute capability (version)``` should be ```6.1``` and its Micro-architecture is ```Pascal```

<img width="1440" alt="Pasted Graphic 21" src="https://user-images.githubusercontent.com/55566616/126869638-dfc90603-ba0f-4b61-81be-80cf5d8f59dc.png">

Therefore, now remove all values, except ```6.1```

<img width="1440" alt="Pasted Graphic 22" src="https://user-images.githubusercontent.com/55566616/126869665-f89a7cfc-ef7d-42ec-a3de-9e7b67fbd537.png">

Now search ```pref``` keyword for ```CMAKE``` parameter.

<img width="1440" alt="Pasted Graphic 24" src="https://user-images.githubusercontent.com/55566616/126869668-68379266-3f90-4c0d-9ede-a346c8de7012.png">

Create a sub-folder named ```install``` under ```build``` folder.

<img width="1102" alt="Pasted Graphic 25" src="https://user-images.githubusercontent.com/55566616/126869685-0d62c51f-fca6-4742-bbb4-e8650ba21ca7.png">

and select this folder by hitting ```Select Folder``` button:

<img width="1103" alt="Pasted Graphic 26" src="https://user-images.githubusercontent.com/55566616/126869686-3e759658-0a59-4ad2-9fc8-2a689684cebe.png">

Next search ```config``` keyword for ```MAKE CONFIGURATION TYPES``` then remove one of its value: ```Debug;``` but leave the other value: ```Release```

<img width="1440" alt="Remove Debug" src="https://user-images.githubusercontent.com/55566616/126869689-f4a46d69-865b-4be1-a3c8-d740ab366b04.png">

Now hit ```Configure``` button one last time:

<img width="1440" alt="Pasted Graphic 30" src="https://user-images.githubusercontent.com/55566616/126870860-cde4b2eb-96ac-4045-aece-a4915f488253.png">

Check again the ```OPENCV``` module using search keyword ```config```.

Also, ```Python``` module should install ```Python-3.8``` in Anaconda install path ```/anaconda3/```

Next hit ```Generate``` button:

<img width="1440" alt="Pasted Graphic 31" src="https://user-images.githubusercontent.com/55566616/126870884-ea012a25-0fdd-4b8b-bad4-7d06702550dd.png">

Now open Windows Command Shell (terminal) and type:

```
C:\OpenCV_Build>"C:\Program Files\CMake\bin\cmake.exe" --build "C:\OpenCV_Build\build" --target INSTALL --config Release
```

<img width="1117" alt="Pasted Graphic 33" src="https://user-images.githubusercontent.com/55566616/126870898-0bd1fecb-88d0-47af-84dc-e3ade689242f.png">

If the process completed without any errors, then you are done.

<img width="1116" alt="Pasted Graphic 34" src="https://user-images.githubusercontent.com/55566616/126870903-54318ec7-35c2-4c9a-8366-31c7936d7bad.png">

The output of your generation (build) would be installed in folder:

```
(C:) › OpenCV_Build › build > lib > python3 › Release
```

<img width="1440" alt="Pasted Graphic 35" src="https://user-images.githubusercontent.com/55566616/126870912-c14ace49-0229-4357-a5bd-58f0b563ce8e.png">

Same output will also be installed in folder:

```
(C:) › Users › Haroon.LAPTOP-IBPFI2VB > anaconda3 > Lib › site-packages › cv2 › python-3.8
```

<img width="1440" alt="Pasted Graphic 36" src="https://user-images.githubusercontent.com/55566616/126870927-17fb3c58-eda0-450e-9414-dfb21bb3304b.png">

Now test your built process. You should be able to do ```import cv2```.

Open Terminal app and type ```python``` and in Python prompt, type: ```import cv2``` then hit ```<Enter>```

<img width="1053" alt="Pasted Graphic 38" src="https://user-images.githubusercontent.com/55566616/126870940-289fd93d-abc2-4f4e-b7cd-95bdc403790b.png">

You can also use this cv2 module by typing ```cv2. __version__```:

```
››› cv2. __version__
'4.5.1'
```

<img width="1440" alt="YOLO" src="https://user-images.githubusercontent.com/55566616/126870952-77a4fa77-07a3-4d91-9731-2867364d10ef.png">

---

## 03 OpenCV with CUDA in Virtual Environment

Now create a ```virtual environment``` by typing the following command in terminal:

```
(base) C:\Users \Haroon.LAPTOP-IBPFI2VB›conda create -n opencv_gpu python=3.8
```

<img width="1052" alt="Pasted Graphic 41" src="https://user-images.githubusercontent.com/55566616/126873116-f51f0871-37dc-4b86-98a3-2e87d1e297e4.png">

Click ````y```

<img width="1051" alt="Pasted Graphic 42" src="https://user-images.githubusercontent.com/55566616/126873132-3cfd07f3-9adf-4f21-afe9-896977a6d529.png">

However if you try to activate the OpenCV by typing:

```
(base) C:\Users\Haroon.LAPTOP-IBPFI2VB>conda activate opencv_gpu
(opencv_gpu) C:\Users\Haroon.LAPTOP-IBPFI2VB>
```

<img width="1051" alt="Pasted Graphic 45" src="https://user-images.githubusercontent.com/55566616/126873144-36e4e6b2-e003-4793-bbe1-8da7b14e47ed.png">

And try to import OpenCV in your Python script by typing:

```
(opencv_gpu) C:\Users\Haroon.LAPTOP-IBPFI2VB>python<Enter>

>>> import cv2
```

you will get an error:

```
ModuleNotFoundError: No module named 'cv2'
```

<img width="1051" alt="Pasted Graphic 45" src="https://user-images.githubusercontent.com/55566616/126873232-100ad9db-bdc0-46d0-aae3-2a0a592c8886.png">

To fix this problem, open again CMake GUI again and search for ```python3``` keyword:

<img width="1440" alt="Pasted Graphic 48" src="https://user-images.githubusercontent.com/55566616/126873240-6d8ea1f7-274a-464d-8874-4583bc1565d2.png">

You see that the path to these Python modules are not correct.

Change the path of ```PYTHON3_EXECUTABLE``` and browse the ```opencv_gpu``` folder where ```python.exe``` is located.

Then click ```Open``` button.

<img width="1096" alt="Pasted Graphic 49" src="https://user-images.githubusercontent.com/55566616/126873264-3c1253bd-9779-4622-850e-961e346d0135.png">

Now the path is modified from:

```
C:/Users/Haroon.LAPTOP-IBPFI2VB/anaconda3/python.exe
```

to:

```
C:/Users/Haroon.LAPTOP-IBPFI2VB/anaconda3/**envs/opencv_gpu/**python.exe
```

<img width="1440" alt="Pasted Graphic 50" src="https://user-images.githubusercontent.com/55566616/126873273-16f8e89f-ccf6-49bf-9a1a-0784490999dd.png">

Now add the same new path for OpenCV virtual environment to other modules:

```
/envs/include                                    to  /envs/opencv_gpu/include
/anaconda3/include                               to  /anaconda3/envs/opencv_gpu/include
/anaconda3/libs/python38.lib                     to  /anaconda3/envs/opencv_gpu/libs/python38.lib
/anaconda3/lib/site-packages/numpy/core/include  to  /anaconda3/envs/opencv_gpu/lib/site-packages/numpy/core/include
```

<img width="1440" alt="Pasted Graphic 51" src="https://user-images.githubusercontent.com/55566616/126873341-1a7f329e-1466-45ca-af19-a8e6542a9b7a.png">

Previously we have installed Numpy for ```base environment```, but have not yet for ```virtual environment```.

Now let’s do that again for virtual environment. Open terminal and type:

```
(opencv_gpu) C:\Users\Haroon.LAPTOP-IBPFI2VB>pip install --upgrade numpy
```

<img width="901" alt="Pasted Graphic 52" src="https://user-images.githubusercontent.com/55566616/126873355-09de1a9a-ef97-4912-a051-86759a770831.png">

We have to repeat the same process for ```virtual environment``` as we did for ```base environment```, including configuration process, build process, and install process (Notes: you don’t have to separate between ```build-process``` and ```install-process```)

Next, push ```Configure``` button:

<img width="1440" alt="Pasted Graphic 53" src="https://user-images.githubusercontent.com/55566616/126873382-f8a11ca2-4a4a-4a70-9816-2f46c5118cde.png">

Now see that our configuration have been bound to virtual environment.

<img width="939" alt="Pasted Graphic 54" src="https://user-images.githubusercontent.com/55566616/126873392-039247ae-9a13-4c27-b54a-e220986f0ced.png">

Next, hit ```Generate``` button to build OpenCV in virtual environment:

<img width="1435" alt="Pasted Graphic 55" src="https://user-images.githubusercontent.com/55566616/126873397-72106a6b-22bd-4f94-9b0f-0bdd6ce2f9ad.png">

Now open Windows Command Shell (terminal) and type:

```
C:\OpenCV_Build>"C:\Program Files\CMake\bin\cmake.exe" --build "C:\OpenCV_Build\build" --target INSTALL --config Release
```

<img width="894" alt="Pasted Graphic 56" src="https://user-images.githubusercontent.com/55566616/126873427-4d10b1a5-abc6-4677-bbaa-4a2968e35777.png">

And try to import OpenCV in your Python script by typing:

```
(opencv_gpu) C:\Users\Haroon.LAPTOP-IBPFI2VB>python <Enter>

>>> import cv2
```

Also, you can now use this cv2 module by typing ```cv2. __version__```:

```
››› cv2. __version__
'4.5.1'
```

<img width="1440" alt="YOLO" src="https://user-images.githubusercontent.com/55566616/126873435-e724860b-cd64-4e7c-9bae-32bb2e64964c.png">

Finally, you test your OpenCV installed base using the following script:

```
(base) C:\OpenCV_Build›python test_script.py
```

[test_script.py] (https://github.com/haroonshakeel/opencv4.5.1_with_cuda_gpu/blob/main/test_script.py): github.com/haroonshakeel/opencv4.5.1_with_cuda_gpu/blob/main/test_script.py

```
import numpy as np
import cv2 as cv
import time

npTmp = np.random.random((1024, 1024)).astype(np.float32)

npMat1 = np.stack([npTmp,npTmp],axis=2)
npMat2 = npMat1

cuMat1 = cv.cuda_GpuMat()
cuMat2 = cv.cuda_GpuMat()
cuMat1.upload(npMat1)
cuMat2.upload(npMat2)
start_time = time.time()
cv.cuda.gemm(cuMat1, cuMat2,1,None,0,None,1)
print("CUDA --- %s seconds ---" % (time.time() - start_time))
start_time = time.time()

cv.gemm(npMat1,npMat2,1,None,0,None,1)
print("CPU --- %s seconds ---" % (time.time() - start_time))
```

<img width="1435" alt="Pasted Graphic 57" src="https://user-images.githubusercontent.com/55566616/126873472-74fe25d8-ce1e-429b-be0c-242330c5c297.png">

It is perfectly working.

Your OpenCV is now ready to go.

---

## 04 Clean Up Your Installation

This is an optional process.

**01** You can remove all files and folders under ```(C:) OpenCV_Build> build ›``` EXCEPT ```lib``` folder (this is the working directory, DO NOT delete it!!)

<img width="1435" alt="Pasted Graphic 59" src="https://user-images.githubusercontent.com/55566616/126873495-9675c2a7-51be-47e8-99d0-2c179950fa0f.png">

**02** You can also remove the following folders under ```(C:) OpenCV_Build›``` folder:

• ```opencv_contrib-4.5.1```
• ```opencv-4.5.1```

<img width="1435" alt="Pasted Graphic 60" src="https://user-images.githubusercontent.com/55566616/126873515-8542aba9-14ac-4ae9-ad7e-072d1c33aa11.png">

**03** Move the two download zip files to ```other_stuff``` folder:

• ```opencv_contrib-4.5.1.zip```
• ```opencv-4.5.1.zip```

<img width="1435" alt="Pasted Graphic 61" src="https://user-images.githubusercontent.com/55566616/126873529-1f9cbe3f-9fc2-4757-9d71-4098326da699.png">

--------------------

Voila… you’re done.

Congratulation!


---

tag: ```#learning``` ```#notes``` ```#build``` ```#install``` ```#opencv``` ```#cuda``` ```#gpu``` ```#support``` ```#windows``` ```#2021``` ```#thecodingbugchannel``` ```#youtube``` ```#$$$$$```
