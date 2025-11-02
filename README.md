# peakx
## This repository takes a schmitt trigger from Dr Wagenaar's excellent collection python libraries and makes it easy to install and import.

## Build instructions

Most of the code can be used as-is, however, a few functions have C++ backends that must be compiled before use. You will need a C++ compiler such as [GCC](https://gcc.gnu.org/), [Visual Studio Community](https://visualstudio.microsoft.com/vs/community/), or [XCode](https://developer.apple.com/xcode/) and you will need the [SCons](https://scons.org/) build system. Instructions are [here](https://scons.org/doc/production/HTML/scons-user/ch01s02.html), but basically, you open a terminal and type:

    python -m pip install scons
    
On Linux you may prefer to use the system's package manager. E.g., in Debian or Ubuntu:

    sudo apt install scons
    
with SCons installed, compile the C++ backends:

    cd peakx
    scons

After a little verbosity, that should print out “scons: done building targets.” If not, please report any errors.


## Installation instructions
Once you have build scons, install by navigating to the project directory in your terminal and enter:

pip install -e .

you can import and run this package as:

```python
import peakx
import numpy

arr = np.array([1,2,3,4,5,6,7,8,9,10])

on, off = peakx.schmitt(arr, 8,3)
```
