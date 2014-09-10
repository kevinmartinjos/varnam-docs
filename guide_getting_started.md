###Getting started

####Setting up libvarnam
Libvarnam is the core of the varnam project and is written in c. These instructions are specific to linux. Follow these instructions to compile and install libvarnam on your computer. First download the latest version of libvarnam from [here](http://download.savannah.gnu.org/releases/varnamproject/libvarnam/source/).

######Requirements 

You need to install the following packages in debian/ubuntu before we can proceed:

+ ruby and ruby dev. `sudo apt-get install ruby ruby-dev` on the terminal installs these packages

+ The ruby gem ffi. The ruby foreign function interface is needed to call functions written in c from ruby. `sudo gem install ffi` on the terminal. This might take some time

+ cmake. `sudo apt-get install cmake`

+ build-essential (optional). This package contains many development tools and libraries that are usually required when using debian/ubuntu for development. Though you might not need many of the packages under build-essential for varnam, it is good (and safe) to have them. `sudo apt-get install build-essential`

+ check (optional). check is a c library used by varnam to write unit tests. If you are not planning to run the tests, then you don't need this package. However, running tests after installation makes it easier to locate and rectify problems if any. `sudo apt-get install check`
