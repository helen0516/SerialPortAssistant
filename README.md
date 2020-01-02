Serial Port Assistant
=====================

Author: Kang Lin (kl222@126.com)
--------------------------------

[<img src="Resource/png/China.png" alt="Chinese" title="Chinese" width="16" height="16" />Chinese](README_zh_CN.md)

1. ![Project: https://github.com/KangLin/SerialPortAssistant](https://github.com/KangLin/SerialPortAssistant)  
This project is a cross-platform serial assistant. It can run on:
    - [x] WINDOWS
    - [x] linux
    - [x] Android
    - [x] mac  
        Mac os, I don't have the corresponding equipment,
        please compile and test the user with the corresponding equipment.

2. Complie status

[![windows、android](https://ci.appveyor.com/api/projects/status/y77e828ysqc79r9o?svg=true)](https://ci.appveyor.com/project/KangLin/serialportassistant)
[![linux](https://travis-ci.org/KangLin/SerialPortAssistant.svg?branch=master)](https://travis-ci.org/KangLin/SerialPortAssistant)

3. Multi-language
    * Chinese  
    ![Chinese](Docs/ui-zh.jpg)
    * Englisth  
    ![Englisth](Docs/ui-en.jpg)

4. Multi style

5. ![Release download](https://github.com/KangLin/SerialPortAssistant/releases)  
![Latest release download](https://github.com/KangLin/SerialPortAssistant/releases/latest)

- windows
    + [SerialPortAssistant-Setup-v0.5.1.exe](https://github.com/KangLin/SerialPortAssistant/releases/download/v0.5.1/SerialPortAssistant-Setup-v0.5.1.exe)

- linux
    + [SerialPortAssistant_v0.5.1.tar.gz](https://github.com/KangLin/SerialPortAssistant/releases/download/v0.5.1/SerialPortAssistant_v0.5.1.tar.gz)  
        The AppImage format executable can be run directly on the Linux system, see: https://appimage.org/  
        Usage:    
        1. Decompress. Copy SerialPortAssistant_v0.5.1.tar.gz to install directory, then decompress it:
    
                  sudo mkdir /opt/SerialPortAssistant
                  cd SerialPortAssistant
                  sudo wget https://github.com/KangLin/SerialPortAssistant/releases/download/v0.5.1/SerialPortAssistant_v0.5.1.tar.gz
                  sudo tar xvfz SerialPortAssistant_v0.5.1.tar.gz
    
        2. install
    
                  sudo ./install1.sh install SerialPortAssistant
    
        3. If you want to uninstall
    
                  sudo ./install1.sh remove SerialPortAssistant

- ubuntu
    + [serialportassistant_0.5.1_amd64.deb](https://github.com/KangLin/SerialPortAssistant/releases/download/v0.5.1/serialportassistant_0.5.1_amd64.deb)

            sudo dpkg -i serialportassistant_0.5.1_amd64.deb

- android
    + [SerialPortAssistant_v0.5.1.apk](https://github.com/KangLin/SerialPortAssistant/releases/download/v0.5.1/SerialPortAssistant_v0.5.1.apk)
    
6. Donate  
If you are satisfied, you can donate to me  
 
![donation](https://github.com/KangLin/RabbitCommon/raw/master/Src/Resource/image/Contribute.png "donation")

7. Dependence  

  + [Qt (LGPL v2.1)](http://qt.io/)
  + RabbitCommon: https://github.com/KangLin/RabbitCommon
  
  ```
  git clone https://github.com/KangLin/RabbitCommon.git
  ```
  
8. Developer  
8.1. Compile  
  - Download source code

        git clone https://github.com/KangLin/SerialPortAssistant.git

  - Compiled with QtCreator
    * Open the project file ![SerialPortAssistant.pro](SerialPortAssistant.pro) with QtCreator
    * Set the parameter RabbitCommon_DIR  
      Project -> Build & Run -> Build -> Build settings -> Build step -> qmake 
    * Direct compilation can generate programs
  - Compile with the command line
    * Build the build directory in the project root directory
    * *qmake* build compilation project
    * *make* install Build the program with the local toolchain
    * The program is generated in the *install* directory

          mkdir build
          cd build
          qmake ../SerialPortAssistant.pro
          make install
          cd install  #The program is generated in the install directory

8.2. Script  
  - build_debpackage.sh  
    + This script generates the deb package under linux.
      Before use, please make sure the following programs are installed
  
            sudo apt-get install debhelper fakeroot 
      
    + Use system qt
    
            sudo apt-get install -y -qq qttools5-dev qttools5-dev-tools \
                 libqt5serialport5-dev qtbase5-dev qtbase5-dev-tools

  - tag.sh
    This script is used to generate new release version numbers and tag
