# Developer Documentation

Within the FPGAedu project's scope, a developer concerns itself with the development of experimentation packages. Experimentation packages can be considered the project's unit of containment and distribution for experiment setup logic. Additional to the development of the actual experiment setup logic, a developer must encapsulate its work in order to conform to the project's specifications, such that end users can easily load and interact with the experiment setup. This encapsulation can be considered a three-stage process. 

The first stage of this process is concerned with the projection of a design's signals and stateful elements on an address space. This projection is achieved through the introduction of additional logic that 'wraps' the experiment setup's logic, converting it into a design entity that conforms to the experiment setup component specification. 
