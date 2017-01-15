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
    element:
        bits: 8
        writable: true
    array: 
        size: 1024
        
```
