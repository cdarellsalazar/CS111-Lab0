# A Kernel Seedling
This is the documentation for CS 111 Lab 0.

## Building
```shell
In order to build the module, simply run the "$ make" command. The rest will be handled by the Makefile.

If you'd like to remove previous build information, you can run the "$ make clean" command. 
```

## Running
```shell
To run the actually kernel module itself, you must load the module into the kernel. This can be done via
the "$ sudo insmod proc_count.ko" command. You can verify that the module has been loaded by looking in the
proc directory, to see if the file "count" exists in that directory .
```
The results can be found by running "$ cat /proc/count". This will print out the number of processes running
(which is stored in the count file). 

## Cleaning Up
```shell
If you wish to unload the module, simply run the "$ sudo rmmod proc_count" command. This will remove the 
module from the kernel.

NOTE: This command MUST be run prior to using the python test script.
```

## Testing
```python
python -m unittest
```
After running the above command, I receieve the following output:

"Ran 3 tests in 0.762s

OK"

On failed tests, it will report which test failed and what line in the script an exception was thrown. 

## Version
```shell
uname -r -s -v
```
The kernel release version that thsi module was tested on was 5.15.8-arch1-1. This output was received from 
running the "$ uname -r" command.
