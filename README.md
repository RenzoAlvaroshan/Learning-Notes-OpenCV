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

Download [Anaconda Installer](anaconda.com/products/individual):

<img width="1440" alt="Anaconda Installers" src="https://user-images.githubusercontent.com/55566616/126862305-4bf9c0e8-b08f-4043-af9b-3743383f28a4.png">

<img width="490" alt="Anaconda3 2020 11 (64-bit) Setup" src="https://user-images.githubusercontent.com/55566616/126862344-4c2dab10-b0c8-44df-a60e-2480f2d75c7f.png">
<img width="491" alt="ANACONDA  Choose the folder in which to instal Anaconda3 2020 11 (64-bit)" src="https://user-images.githubusercontent.com/55566616/126862348-409286e2-6648-4f38-8917-55f68b22d734.png">
<img width="492" alt="Anaconda3 2020 11 (64-bit) Setup" src="https://user-images.githubusercontent.com/55566616/126862350-e348542b-7c5d-4bf3-8b91-b775248fa60a.png">
<img width="494" alt="Anaconda3 2020 11 (64-bit) Setup" src="https://user-images.githubusercontent.com/55566616/126862351-30e796ad-1f3b-4ceb-8404-673a6c1cbf54.png">
<img width="496" alt="2020 11 (64-bit) Setup" src="https://user-images.githubusercontent.com/55566616/126862355-be434046-0792-4a68-a556-73d1e5eb9948.png">

### (2) Microsoft Visual Studio

Next, download [Visual Studio Community 2019 16.7.2](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbUZjbnZwVWxneDBhZnNGZExHa0FlR2FiTEZ3d3xBQ3Jtc0trQ0doYzVlSDBDMDJEM2lpOWNMcXlkZFBMLTRlTzNUbU5LWnRGOWRJRmIzeGd0cVFjMXVqWk5INTNidzJNLXczVHcxbGpzS0FvV3NxTmk0cW1LMmRWdGZhRHdXNk9BRW5aTl83TzJNYldiLV9oU0RsTQ&q=https%3A%2F%2Fvisualstudio.microsoft.com%2Fvs%2Fcommunity%2F):

<img width="1440" alt="components Language packs" src="https://user-images.githubusercontent.com/55566616/126863268-c9f0dd02-4bc3-4408-a886-0dc58b908d85.png">

Select ```Desktop development with C++``` option for Studio Code C++ support

<img width="1440" alt="Installation details" src="https://user-images.githubusercontent.com/55566616/126863270-c24e8363-53b4-405d-b130-51cbd7b83ade.png">

### (3) Cuda Toolkit Update

Now download [CUDA Toolkit 11.0 Update Downloads](developer.nvidia.com/cuda-11.0-update1-download-archive?target_os=Windows&target_arch=x86_64):

<img width="1440" alt="Resources" src="https://user-images.githubusercontent.com/55566616/126863551-7019a69a-7f41-4b75-bc71-7ee6a98f8afb.png">

Choose ```Windows``` operating system for ```Select Target Platform```.

<img width="1440" alt="CUDA Toolkit Archive" src="https://user-images.githubusercontent.com/55566616/126863557-16f0e0f4-6d68-4004-9386-608281295170.png">

Choose ```CUDA Toolkit 11.0 Update 1 Downloads```:

<img width="1440" alt="CUDA Toolkit 11 0 Update 1 Downloads" src="https://user-images.githubusercontent.com/55566616/126863575-928096f3-e790-4bc5-8eb6-fb0d728b8247.png">

Choose the following options:

* Operating System: ```Windows```
* Architecture    : ```x86_84```
* Version         : ```10```
* Installer Type  : ```exe (local)```

<img width="1440" alt="Pasted Graphic 11" src="https://user-images.githubusercontent.com/55566616/126863930-4190691d-becf-4379-bd5b-90c09b9f3dd2.png">
<img width="1440" alt="Pasted Graphic 12" src="https://user-images.githubusercontent.com/55566616/126863932-eeda04b4-03fa-402f-8944-4c65650a8fd9.png">
<img width="1440" alt="cuDNN Download" src="https://user-images.githubusercontent.com/55566616/126863933-9c7b22b7-f63c-4293-9688-4b22d8dbe9d0.png">

Click `Download cuDNN v8.0.5 (November 9th, 2020), for CUDA 11.0' to expand the driver list:

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

Now download [CMake GUI](cmake.org/download/] app:
```
cmake.org/download/
```
![Pasted Graphic 18.png](blob:https://euangoddard.github.io/ac8d0e01-3542-4c22-9291-cdd6a0ec7113)

Choose files `cmake-3.19.3-win64-x64.msi', then run the installer to setup CMake in your computer.

![Pasted Graphic 20.png](blob:https://euangoddard.github.io/b2a1707b-1ca2-4e28-a6be-f5e18de3f3b9)

![Pasted Graphic 21.png](blob:https://euangoddard.github.io/6fc973bd-5e1a-40ae-99b0-1e2d034f2321)

![Pasted Graphic 21.png](blob:https://euangoddard.github.io/6fc973bd-5e1a-40ae-99b0-1e2d034f2321)

### (5) OpenCV Setup

Create a folder for OpenCV in you ```C:``` drive:

OpenCV_Build

Next, download source code of `OpenCV-4.5.1' from:

opencv.org/releases/

Choose: `sources'

![Pasted Graphic 23.png](blob:https://euangoddard.github.io/103c41ee-b4b1-471d-8ea1-f57656a08eb4)

It will bring you to OpenCV repository in GitHub:

github.com/opencv/opencv/archive/4.5.1.zip

Save it in folder `OpenCV_ Build' you just created:

![Pasted Graphic 24.png](blob:https://euangoddard.github.io/33edabd5-4336-4762-8c61-91593ba6dae3)

Next, go to `opencv_contrib' folder in GitHub:

github.com/opencv/opencv_contrib

![Pasted Graphic 25.png](blob:https://euangoddard.github.io/708e8eae-45c8-44a1-937c-a107aa290dba)

Click `Relase' button

![Pasted Graphic 26.png](blob:https://euangoddard.github.io/8337c03a-8f79-4868-bf59-7ea227dd9e71)

Download OpenCV version `4.5.1.zip' also save it in folder `OpenCV_ Build':

![Pasted Graphic 27.png](blob:https://euangoddard.github.io/a4caf35c-5459-49fd-aae3-854f3ad4272c)

Now, extract both .zip files:

opencv_contrib-4.5.1.zip

opencv-4.5.1.zip

![Pasted Graphic 28.png](blob:https://euangoddard.github.io/0fa85848-390a-4e05-9aaa-f512a793c650)

Now run CMake GUI app:

![Pasted Graphic 31.png](blob:https://euangoddard.github.io/613f3b75-ef78-48fd-811d-4d487e978935)

In `Where is the source code:'  click `Browse' to choose the folder of files to be compiled:

![Pasted Graphic 32.png](blob:https://euangoddard.github.io/c5d9bc7a-405e-4351-a31f-ae438bb1b59f)

Select `(C:) › OpenCV_Build › opencv-4.5.1 >' folder

![Pasted Graphic 33.png](blob:https://euangoddard.github.io/478995fc-b2e3-43fb-a41d-bd5485ca42cc)

In `Where to build the binaries'  click `Browse' to choose the folder of files for the output.

Create a new sub-folder named `build'

C:/OpenCV_Build/build

![Pasted Graphic 34.png](blob:https://euangoddard.github.io/7c062dfe-5c5b-4ece-a51b-2d3eaa3a0ec6)

Then make sure that `Grouped' option is checked:

![Pasted Graphic 35.png](blob:https://euangoddard.github.io/c5416260-c8b9-4225-a82f-8a71d29473a0)

And click `Configure' button:

![Pasted Graphic 36.png](blob:https://euangoddard.github.io/cc2246c0-fd61-41b3-88ce-a4de7bdaa791)

Choose:

- Specify the generator for this project: `Visual Studio 16 2019'

- Optional platform for generator(if empty, generator uses: x64): `x64'

- Use default native compilers = checked

![Pasted Graphic 38.png](blob:https://euangoddard.github.io/36eac7de-21bd-4e17-80e2-214f463f73f2)

Then click `Finish'.

CMake GUI app will start to build your OpenCV:

![Pasted Graphic 39.png](blob:https://euangoddard.github.io/958d5aee-5398-4756-bab4-cb777e6bd790)

Upon finish, search keyword `python' to make sure that your OpenCV is built for `Anaconda':

![Pasted Graphic.png](blob:https://euangoddard.github.io/43208b70-d058-40f8-86ba-37ba7dc40468)

Now check that the OpenCV modules is `Unavailable' for `python3'

![Pasted Graphic 1.png](blob:https://euangoddard.github.io/82742bbb-6c7a-43f8-9a66-b096d711cfa7)

If you don't fix this, you will encounter the most common error `ModuleNoteFoundError' when you try to `import OpenCV' as shown below:

![Pasted Graphic 2.png](blob:https://euangoddard.github.io/94f9e88d-a7cb-44a5-8276-afe07c8a2251)

This is due to mismatch of Numpy version. We can fix it by by updating Numpy.

![Pasted Graphic 3.png](blob:https://euangoddard.github.io/e7b6c275-1b95-44bd-9c8e-d14ae68bf8e0)

First, delete cache file from `File | Delete Cache' menu:

![Pasted Graphic 4.png](blob:https://euangoddard.github.io/4eeac18c-a33f-47f3-b416-dd3dd754c2a8)

Then, run Anaconda prompt -- choose `Run as administrator':

![Pasted Graphic 5.png](blob:https://euangoddard.github.io/61ad6bd7-0c2d-41d1-8f8d-ce334a8dd332)

Then run the following command to upgrade Numpy version to `1.19.5':

C: \WINDOWS \system32>pip install-upgrade numpy

Now hit `Configure' button again to re-configure CMake app:

![Pasted Graphic 6.png](blob:https://euangoddard.github.io/48fb6013-f799-43d4-b9a7-b25de80c3a1f)

Now you'll see additional information in Python3 module:

![Pasted Graphic 7.png](blob:https://euangoddard.github.io/67f87ad1-b77e-411c-9bb4-933391a70a42)

Also, in OpenCV module:

![Pasted Graphic 8_1.png](blob:https://euangoddard.github.io/90e495b9-6a47-4732-8e39-ba441f7ce0f7)

Now let's start the configuration.

Search `WITH_CUDA' keyword then enable its checkbox

![Pasted Graphic 9_1.png](blob:https://euangoddard.github.io/0611882a-763b-45d1-b69f-66fdaa95ae0d)

Similarly with other parameters:

`OPENCV DNN CUDA'

![Pasted Graphic 10_1.png](blob:https://euangoddard.github.io/028f9f02-9d07-405c-84b0-33002d53a235)

`ENABLE FAST MATH'

![Pasted Graphic 11_1.png](blob:https://euangoddard.github.io/37c69c5f-b25c-4f6e-a893-292f981f11b1)

`BUILD opency_world'

![Pasted Graphic 12_1.png](blob:https://euangoddard.github.io/a39b0657-c66e-422f-8ce8-4bb4ebee1ee4)

`opency_python'

![Pasted Graphic 13_1.png](blob:https://euangoddard.github.io/8e3cdb0d-c832-4c3a-a5e3-a97c4e610be9)

Next, set the folder for `OPENCV_EXTRA_MODULES_PATH' by clicking three-dot [...] button

--------------------

tag: #learning #notes #build #install #opencv #cuda #gpu #support #windows #2021 #thecodingbugchannel #youtube #$$$$$
