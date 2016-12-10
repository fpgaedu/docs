# `nexys4-usb-vivado`
The `nexys4-usb-vivado` environment specification describes an experimentation environment based around the Digilent Nexys 4 FPGA Development board. 

## Physical Setup
The environment prescribes that the Nexys 4 board is connected to the user's PC through a USB connection. The board is powered through the same USB connection, although one might decide to power the board through an external 5V power supply in order to allow for autonomous operation after programming. 

## Software Setup
- Xilinx Vivado 2016.3 or newer installed
- `vivado` command is available on the `PATH`
- Serial drivers installed such that a serial device becomes available when the board is connected to the PC.

## Verified Operating Systems
- Ubuntu 16.04

## Notes
- On Ubuntu, Vivado cable drivers have to be installed manually. See [UG973](https://www.xilinx.com/support/documentation/sw_manuals/xilinx2016_3/ug973-vivado-release-notes-install-license.pdf) page 25 for more information.