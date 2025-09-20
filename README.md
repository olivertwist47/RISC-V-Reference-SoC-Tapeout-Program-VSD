# RISC-V-Reference-SoC-Tapeout-Program-VSD
This repository documents my journey through the VSD RISC-V SoC Tapeout Program. Here you'll find a weekly log of tasks completed and lessons learned.

<details>
	<summary>Day 0 - Tools Installation </summary>
	
# Day 0 - Tools Installation
## Yosys
```
$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make               # If make is not installed
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
# Yosys build depends on a Git submodule called abc, which hasn't been initialized yet. You need to run the following command before running make
$ git submodule update --init --recursive
$ make 
$ sudo make install
```
<img width="702" alt="yosys" src="https://github.com/olivertwist47/RISC-V-Reference-SoC-Tapeout-Program-VSD/blob/37a8b278b0fd97e5a409aa7a84daad3e2539dbf3/Yosys1.png">
<img width="702" alt="yosys" src="https://github.com/olivertwist47/RISC-V-Reference-SoC-Tapeout-Program-VSD/blob/27e0832e3b7bd56f50a975c3fac429030b133c15/Yosys2.png">

## Iverilog
```
$ sudo apt-get update
$ sudo apt-get install iverilog
```
<img width="702" alt="iverilog" src="https://github.com/olivertwist47/RISC-V-Reference-SoC-Tapeout-Program-VSD/blob/27e0832e3b7bd56f50a975c3fac429030b133c15/Iverilog.png">

## GTKWave
```
$ sudo apt-get update
$ sudo apt install gtkwave
```
<img width="604" alt="gtkwave" src="https://github.com/olivertwist47/RISC-V-Reference-SoC-Tapeout-Program-VSD/blob/27e0832e3b7bd56f50a975c3fac429030b133c15/GTKwave.png">

## Ngspice
```
$ sudo apt update
$ sudo apt install ngspice
```
<img width="702" alt="iverilog" src="https://github.com/olivertwist47/RISC-V-Reference-SoC-Tapeout-Program-VSD/blob/27e0832e3b7bd56f50a975c3fac429030b133c15/Ngspice.png">

## Magic VLSI
```
# Install required dependencies
sudo apt-get install m4
sudo apt-get install tcsh
sudo apt-get install csh
sudo apt-get install libx11-dev
sudo apt-get install tcl-dev tk-dev
sudo apt-get install libcairo2-dev
sudo apt-get install mesa-common-dev libglu1-mesa-dev
sudo apt-get install libncurses-dev

# Clone Magic repository
git clone https://github.com/RTimothyEdwards/magic
cd magic

# Configure build
./configure

# Build Magic
make

# Install system-wide
sudo make install
```
<img width="702" alt="iverilog" src="https://github.com/olivertwist47/RISC-V-Reference-SoC-Tapeout-Program-VSD/blob/27e0832e3b7bd56f50a975c3fac429030b133c15/Magic.png">
</details>



