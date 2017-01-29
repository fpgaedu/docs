
# Experimentation Package
An experimentation package is a unit of containment for the resources required to setup and interact with an experiment setup. The experimentation package is defined to be a `.zip`file archive. The contents of the file archive are unspecified, except for the file entry `manifest.yaml` which is reserved for the package's manifest file. The following listing displays an example file structure for an experimentation package:

```
+--+ directory
|  |- file 1
|  | ...
|  |- file m
|
|- file 1
|- ...
|- file n
|
|- manifest.yaml
```

## Manifest file
The experimentation package manifest file provides information about the package's contents. Additional to administrative metadata, the manifest file instructs on how the package contents should be interpreted. This information includes:

- The protocol used for programming and any associated protocol parameters, such as the package file entry containing the bitstream file.
- The protocol used for establishment of a communication channel with the experiment setup controller and any associated protocol parameters, such as the baud rate.
- The protocol used for interaction with the experiment setup and any associated protocol parameters, such as the width of the data bus.
- Optionally, the manifest file may contain a number of front-end directives which provides the front end with additional information, such as how the experiment setup's address space should te interpreted.

The following listing displays the contents of an example experimentation package manifest file `manifest.yaml`:
```
manifestVersion: 1.0
date: 2016-12-08T20:35:09+00:00
environment: nexys4-usb-vivado
experimentSetup:
    title: counter
    description: A simple 25-bit counter with an enable signal.
    version: 0.3
modules: 
  - identifier: vivado-programming
    configuration:
        bitStreamFile: bitstream.bit
  - identifier: serial
    configuration:
        baudRate: 9600
  - identifier: interaction-basic
    configuration:
        dataWidth: 32
        addressWidth: 32
  - identifier: address-space
    configuration:
        AddressSpaceDescriptionFile: address-space.yaml
    

		
```
