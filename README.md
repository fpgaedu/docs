# FPGAedu
The FPGAedu project aims to simplify the use of FPGAs as a tool for physical experimentation with digital logic. The project provides software tools that facilitate interaction with experiment setups hosted within a FPGA as well as tools that ease the development of new experiment setups. These tools offer the potential to increase the number of people that are enabled in using actual physical hardware in their learning and teaching about digital logic and computer hardware.

> FPGAs are a special class of computer chips. As opposed to regular computer chips with fixed functionality, FPGAs allow their functionality to be reconfigured. Their flexibility allows for FPGAs to be used in a wide field of areas, including computer chip development, reconfigurable computing and experimentation.

## Introduction
FPGAs provide a well-established means for physical containment of digital logic designs. The utilization of FPGAs however, generally requires specific technical knowledge and skills, limiting the applicability of FPGAs as an entry-level tool for education. The FPGAedu project is the result of a bachelor's thesis project that proposes a model of interaction and development for experiment setups contained within FPGAs. This model proposes different abstractions that reduce the complexity and skill requirements for the processes of experiment setup interaction and development. 

### Experimentation
> For more information, see the [user documentation](./users).

The FPGAedu project aims to minimize the resources and skills required for experimentation with digital logic using FPGAs. From a user's perspective, the FPGA can be considered a physical container in which experiment setups can be loaded and interacted with using simple commands. Users connect a FPGA to their PC, allowing for initialization of their experiment setup through the loading of pre-existing experimentation packages using the project's provided PC software. Users interact with the loaded experiment setup through the same software as well as the FPGA's peripheral human interface devices such as displays, leds, buttons and switches, reinforcing the physical experience. Users are explicitly witheld from  HDL modelling and use of FPGA development environments. The FPGAedu project considers FPGAs an educational tool as opposed to an educational goal. 

### Development
> For more information, see the [developer documentation](./developers).

In order to facilitate this level of abstraction to end users, experiment setups are developed by more experienced developers in the form of experimentation packages. These experiment packages contain the actual FPGA configuration as well as metadata that instructs the PC software. The FPGA configuration is compiled from the experiment setup's logic definition. Additional to the experiment setup's bare logic however, additional logic is required in order to facilitate interaction through the user's PC as well as the FPGA's peripheral I/O devices. In order to allow experiment setup developers to focus on their logic, the FPGAedu project aims to automate (parts of) the process of 'wrapping' an existing logic definition, such that a developer is not burdened by manually embedding the experiment setup design in an FPGA. 
