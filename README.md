# gr-lora-sdr
Implementation of LoRa in gnu radio (LM22.1)
*** 
This project was created for the universaty tasks. 
Firstly thnx [J. Tapparel](https://github.com/tapparelj/gr-lora_sdr) and his team for opportunity to explore this project. 

Here you can find installation tutorial on Linux Mint 22.1 without docker and miniconda/conda

## Installation

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
## Issues
`ImportError: libspdlog.so.1.11: cannot open shared object file: No such file or directory`

Your program requires the libspdlog.so.1.11 library, but the system cannot find it. This means that either the library is not installed or the system does not know where to find it.

-**Problem when terminal closes instantly:**

GNU Radio runs the script with the command:
`/usr/bin/x-terminal-emulator -e /usr/bin/python3 -u /home/mint/Downloads/gr-lora_sdr/examples/tx_rx_functionality_check.py`

Type to see errors:
```
python3 -u /home/mint/Downloads/gr-lora_sdr/examples/tx_rx_functionality_check.py
```
Now you can see different types of errors like missing libraries, such as `ImportError: libgnuradio-lora_sdr.so.1.0.0git: cannot open shared object file: No such file or directory`
make sure you have these libraries installed:
```
find /usr/local -name “libgnuradio-lora_sdr.so*”
```
Then you can copy them to necessary for GR dir:

(thinking its always /usr/lib/)
```
sudo cp /usr/local/lib/x86_64-linux-gnu/libgnuradio-lora_sdr.so /usr/lib/
sudo cp /usr/local/lib/x86_64-linux-gnu/libgnuradio-lora_sdr.so.1.0.0git /usr/lib/
```






