Collaboration for Astronomical Signal Processing and Electronics Research

main repository: casper-astro/mlib_devel
- contains sources for using matlab and simulink to create designs for FPGAs and generate bitstreams

tutorials repository: casper-astro/tutorials_devel
- contains example tutorials for using the CASPER toolflow
- supported platforms: SNAP, Skarab, Red Pitaya, RFSoC-Pynq 4x2

python interface repository: casper-astro/casperfpga
- a python library used to interact and interface with [**CASPER** Hardware](https://github.com/casper-astro/casper-hardware) 
- Functionality includes being able to reconfigure firmware, as well as read and write registers across the various communication interfaces.

Update existing toolchain:
- pull changes from GitHub
- With model open in MATLAB, run the following script: update_casper_blocks(bdroot)

Software Dependency Version Requirements by Platform:
- Red Pitaya (Zynq 7010 core): Ubuntu 20.04; MATLAB 2021a/2022a; Vivado 2021.1; repository branch: m2021a/m2022a; Python 3.8
- ZCU111 (Zynq RFSoC core): Ubuntu 20.04; MATLAB 2021a/2022a; Vivado 2021.1/2023.1; repository branch: m2021a/m2022a; Python 3.8;
- RFSoC-PYNQ 4x2 (Zynq RFSoC core): Ubuntu 20.04; MATLAB 2021a/2022a; Vivado 2021.1/2023.1; repository branch: m2021a/m2022a; Python 3.8;