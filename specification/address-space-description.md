# Address Space Description Specification

The address space description provides a mapping between the address space's positions and human-readable identifiers. This mapping allows for identification of elements within an experiment setup's address space and prevents manual lookup of postions. The address space description does not prescribe how values are to be interpreted, but is only concerned with the mapping of bit sequences. 

The address space description can be used for identification of single elements, as well as homogeneous arrays of sequential elements. The listing below displays an example address space description encoded in YAML. 

```
partitions: 
  - name: signal-a
    description: Example 1-bit output signal.
    address: 0x0
    element: 
        bits: 1
        writable: false
  - name: signal-b
    description: Example 13-bit input signal.
    address: 0x1
    element:
        bits: 13
        writable: true
  - name: register-file
    description: example 32-bit register file with 32 positions
    address: 0x3
    element:
        bits: 32
        writable: true
    array:
        size: 32
  - name: example-ROM
    description: Example ROM with 1024 8-bit positions. From the experiment setup's perspective, the memory's contents are read-only. In order to be able to set the memory's contents, the memory is set to be writable. 
    address: 0x83
    element:
        bits: 8
        writable: true
    array: 
        size: 1024
        
```
