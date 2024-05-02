# Zephyr sample for working with KConfig and CMakeLists
This repository contains a Zephyr dummy example to simply showcase how KConfig and CMakeLists files can be used for building the codebase existing in nested files and integrating configuration options both for the build process and the application utilization.

### Implemented Personal Approach On Involving Subfolders/Submodules Into The Project
Dummy module file given inside the nested file (at app/example_module) self configures itself in the build process when some other upper level Kconfig and CMakeLists point to the module file to use its own Kconfig and CMakeLists files. This approach is taken beacuse it feels more intuitive that each module/submodule/driver/library etc. takes care of itself after its folder is decided to be included in the codebase in some other configuration file that's upper level on the folder tree (hierarchical) structure.

### Building and running

- nRF Connect SDK is used when building and is application is run with nRF52840DK board. SDK and Toolchain version used: 2.6.0
- Should be able to be built without nRF Connect SDK and with Zephyr only. Other supported boards can be used, too. Further explanation in repository given in References section can be used for further detail.


### References

- made with the help of this [more detailed example application][more_detailed_example_application].

[more_detailed_example_application]: https://github.com/zephyrproject-rtos/example-application
