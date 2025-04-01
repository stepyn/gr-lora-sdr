# gr-lora-sdr
Implementation of LoRa in gnu radio (LM22.1)
*** 
This project was created for the universaty tasks. 
Firstly thnx [J. Tapparel](https://github.com/tapparelj/gr-lora_sdr) and his team for opportunity to explore this project. 

Here you can find installation tutorial on Linux Mint 22.1 without docker and miniconda/conda

# Installation

```
sudo apt-get update
```
Install dependences:
```
sudo apt-get install cmake g++ libboost-all-dev libusb-1.0-0-dev \
libfftw3-dev libcomedi-dev libcppunit-dev libsdl1.2-dev \
libqt4-dev libqt4-opengl-dev libprotobuf-dev protobuf-compiler \
libgmp-dev libmpfr-dev libyaml-cpp-dev python3-dev python3-mako \
python3-pyqt5
```
Clone the repo
```
git clone https://github.com/tapparelj/gr-lora_sdr.git
cd gr-lora_sdr
```
Building the project 
```
mkdir build
cd build
cmake ..
make
sudo make install
```



