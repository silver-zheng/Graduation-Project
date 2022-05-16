## RTLacc

RTLacc is an acceleration method of RTL simulation based on code instrumentation.

We apply this acceleration method to the accelerator benchmark [MachSuite](https://github.com/breagen/MachSuite),so the benchmark programs that have been instrumented can be used as the C benchmark programs that have accelerated RTL simulation, and can be directly used by accelerator RTL simulation research.

## Organization

Folder organisation is of the following format:


	
       - ##### Accelerator folder
             -original accelerator source file
             -data file incleding input.data and check.data(or golden.dat) 
       - ##### Instrumented_Accelerator folder

             -instrumented accelerator source file
             -perfromance estimate file		

## Requirements
GCC is required. We used GCC 9.3.0 in the experiment so we suggest GCC 9.3.0 or more recent.
Vitis 2021.1 is required.Download and install [here](https://china.xilinx.com/support/download/index.html/content/xilinx/zh/downloadNav/vitis/2021-1.html)

RTL simulation tools can use Vivado XSIM that come with vitis and [ModelSim](https://eda.sw.siemens.com/en-US/ic/modelsim/), etc., and it can be modified in hls.tcl to call different RTL simulation tools.

##Run the bencnmark

After setting the environment ,if you want to use an accelerator benchmark to run RTL simulation whatever in the Accelerator folder or Instrumented_Accelerator folder
:
```

cd $RTLacc/aes/aes

vivado_hls hls.tcl

```

## Licensing



All code is open source (BSD-compatible) and free to use and distribute. Please 
look in the LICENSE file for details.

## Design Spaces

Users and designers can use this acceleration method to obtain approximate performance estimates in the early stage of accelerator design, and then adjust the design according to the feedback.
