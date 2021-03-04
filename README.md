[![Build Status](https://travis-ci.com/tinix84/pyplecs.svg?branch=master)](https://travis-ci.com/tinix84/pyplecs)

[![codecov](https://codecov.io/gh/tinix84/pyplecs/branch/master/graph/badge.svg)](https://codecov.io/gh/tinix84/pyplecs)

# Python Plecs Repository

I wrote a python package to automatize the python simulations. In the test_basic.py you can find all the unit test where every test case show a different function of the package pyPlecs. Just short summary of capabilities:

1. test03_plecs_app_open_highpriority: python open plecs as process in highpriority to execure faster simulations
2. test04_pyplecs_xrpc_server: python use the normal remote control to execute plecs with xrpc server
3. test07_sequential_simulation_server_different_file: pyPlecs generate different plecs file for every variant request and launch them sequentially with normal xrpc simulations
4. test09_gui_simulation: pyPlecs generate different plecs file for every variant request and open them all at the same time and execute them in parallel with just one user (interacting with plecs GUI)

Next development steps are:

1. creation of requirement.txt and setup.py to automatize installation
2. creation of a pool of simulation to manage multiprocessing or multithreading
3. new example for more complex simulation with gui in Ipython
4. generation montecarlo variants in python and then analysis in plecs 

If you want to use but you find bugs please let me know...


---------------

# Installing using conda
Below is a set of commands to configure the tool on windows 10 using conda.  Note pywinauto must be installed and comtypes `1.1.8` seems to have compatibility issues.

```
conda create --name PyPlecsTest --clone base  
conda activate PyPlecsTest
conda install git
conda install -c conda-forge pywinauto 
conda install -c conda-forge comtypes=1.1.7
pip install git+git://github.com/tinix84/pyplecs.git
```



