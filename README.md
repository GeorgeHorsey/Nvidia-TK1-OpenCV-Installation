# Nvidia-TK1-OpenCV-Installation

Followed doc: http://docs.opencv.org/3.0-beta/doc/tutorials/introduction/linux_install/linux_install.html

sudo apt-get install build-essential

sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev

sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev

cd ~/<my_working _directory>
#working dir is to be changed to a name you will remember

git clone https://github.com/Itseez/opencv.git

#Create a temporary directory, which we denote as <cmake_binary_dir>, where you want to put the generated Makefiles, project files as well the object files and output binaries.

cd <cmake_binary_dir>

cd ~/opencv

mkdir release

cd release

cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ..

#Enter the temporary dir you made use cd <your temp dir>

make -j8 

sudo make install
