# dicom-viewer-3D
<img width="796" height="596" alt="example" src="https://github.com/user-attachments/assets/b075c69e-2f31-4ed0-900f-2c38c133a7ed" />

The program is designed for segmentation and creating 3D models of certain organs from DICOM images.
Main development tools Qt, VTK, C++.

The program only works with dicom data encoded in HU (Hounsfield units).
# Functionality
- Build 3D Model from DICOM
- Segmentation of certain organs
- Set volume extraction parameters for model
- Save 3D model to stl
# Model types
- Lungs
- Bones
- Skin
# Implementation
The application uses the vtkMarchingCubes surface construction algorithm
and some simple computational geometry algorithms to generate 3D models of certain organs.
# Build on Windows
<h2>Build requirements</h2>

- Visual Studio 2017 msvc compiler

- Qt 5
  
- VTK 9.3
  
- Windows 10 / 11
  
  
<h2>Preset</h2>

Download [VTK binarys msvc 2017](https://drive.google.com/file/d/14xWSCmUyoiDUJTjGzdh0Buf1E0NwSy7R/view?usp=sharing)

Unpack files to "C:\VTK" folder
```
C:\VTK
|_install
  |_bin
  |_include
  |_lib
  |_share
```
Create system path VTK_DIR
```
VTK_DIR = C:\VTK\install
```
Add VTK_DIR to path
```
%VTK_DIR%\bin
```
<h2>Install Cmake</h2>

Download and install last version


<h2>Install MS Visual Studio 2017</h2>

[download VS 2017 Community](https://aka.ms/vs/15/release/vs_community.exe)

<h2>Install Qt5</h2>

Preferred qt version **Qt5.12.12**

If you don`t have one, you can download [qt5.12.12 offline installer](https://download.qt.io/archive/qt/5.12/5.12.12/)

In Qt5 installer choose msvc 2017 64-bit complect (not minGW!)

<h2>Deploy</h2>

- Configure project in Qt Creator
- Select the kit corresponding to msvc 2017 64-bit
- Set the build type to Release
  
# Test
For testing, you can use [dicom example](https://github.com/ft-290008buchok/3d-dicom-viewer/tree/main/dicom-example)

