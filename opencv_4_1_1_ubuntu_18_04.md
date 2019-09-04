#Notes for installing OpenCV 4.1.1 on Ubuntu 18.04

#System Dependancies
sudo apt update -y # Update the list of packages


#Build tools
sudo apt-get install build-essential cmake unzip pkg-config

#Video/Image Libs
sudo apt remove -y x264 libx264-dev # Remove the older version of libx264-dev and x264
sudo apt-get install libjpeg-dev libpng-dev libtiff-dev
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
sudo apt-get install libxvidcore-dev libx264-dev

sudo apt-get install libgtk-3-dev
sudo apt-get install libatlas-base-dev gfortran

#Python Dev for 2 and 3 
sudo apt-get install python2-dev
sudo apt-get install python3-dev

#Get OpenCV and Contrib from https://opencv.org/releases/

#Python Package Dep
pip install numpy

cd ~/opencv 
mkdir build
cd build

cmake -D CMAKE_BUILD_TYPE=RELEASE \
	-D CMAKE_INSTALL_PREFIX=/usr/local \
	-D INSTALL_PYTHON_EXAMPLES=ON \
	-D INSTALL_C_EXAMPLES=OFF \
	-D OPENCV_ENABLE_NONFREE=ON \
	-D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib/modules \
	-D PYTHON_EXECUTABLE=~/.virtualenvs/cv/bin/python \
	-D BUILD_EXAMPLES=ON ..

#Check output

sudo make install
sudo ldconfig
  
  make -j4
  
  
