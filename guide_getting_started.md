###Getting started

If you have not compiled a piece of software before, this might seem a little intimidating at first. However, it is not as difficult as it sounds. Following the below instructions step by step should get you there. If you're still stuck, feel free to send an email to varnamproject-discuss@nongnu.org. Just remember to [subscribe](https://lists.nongnu.org/mailman/listinfo/varnamproject-discuss) first or else your emails won't reach us.

####Setting up libvarnam
Libvarnam is the core of the varnam project and is written in c. These instructions are specific to linux. Follow these instructions to compile and install libvarnam on your computer. First download the latest version of libvarnam from [here](http://download.savannah.gnu.org/releases/varnamproject/libvarnam/source/).

#####Requirements 

You need to install the following packages in debian/ubuntu before we can proceed:

+ ruby and ruby dev. `sudo apt-get install ruby ruby-dev` on the terminal installs these packages

+ The ruby gem ffi. The ruby foreign function interface is needed to call functions written in c from ruby. `sudo gem install ffi` on the terminal. This might take some time

+ cmake. `sudo apt-get install cmake`

+ build-essential (optional). This package contains many development tools and libraries that are usually required when using debian/ubuntu for development. Though you might not need many of the packages under build-essential for varnam, it is good (and safe) to have them. `sudo apt-get install build-essential`

+ check (optional). check is a c library used by varnam to write unit tests. If you are not planning to run the tests, then you don't need this package. However, running tests after installation makes it easier to locate and rectify problems if any. `sudo apt-get install check`

#####compile libvarnam

Extract the download libvarnam tarball and navigate to the directory using the `cd` command.

In the terminal, type **_one_** of the following commands to compile libvarnam

`cmake .` - to build the source
`cmake -DBUILD_EXAMPLES=true .` - to build the source and contents in the /examples directory
`cmake -DBUILD_TESTS=true .` - to build the source and the unit tests
`cmake -DCMAKE_BUILD_TYPE=debug .` - to build the source with the debug flag on

You can combine two or more options as follows :

`cmake -DCMAKE_BUILD_TYPE=debug -DBUILD_TESTS=true .`

After using cmake, type in `make` and then `sudo make install` to compile and install libvarnam.

#####Compile scheme file

libvarnam stores all the infromation about the languages it supports and the corresponding mapping to patterns in English in a 'scheme file'. The scheme files for the currently supported languages can be found inside /schemes directory.
Even though it doesn't look much like it, the scheme file is actually a ruby script. Scheme files will be discussed in detail later. For now, just understand that the scheme file contains all the information needed by libvarnam to convert whatever you type in English to alphabets in the target language. Each language has got its own scheme file. For example, the scheme file for Hindi is /schemes/hi.

Before varnam can start using information contained in the scheme file, it should parse the scheme file and create an sqlite database that describes which keys transliterate to which alphabets. To create the database, do :

`varnamc -c schemes/<scheme_file>`

For example, if you want to compile the scheme file for Malayalam, do :

`varnamc -c schemes/ml`

Doing so will create a .vst (varnam symbol table) file in the /schemes directory. This is the generated database that has all the rules needed by varnam. 

However, we need the .vst file somewhere else if varnam can use it. Type in `sudo make install` again and this will send the .vst file to where it belongs.

To see if you've done everything right, we will try out the varnam command line tool. Type `varnamc -s ml -t varnam` to transliterate 'varnam' to the equivalent in malayalam. Do not forget to replace 'ml' with the language of your choice.

If you had compiled varnam with `-DBUILD_TESTS=true`, then you can run the unit tests to see if everything has been set up correctly. `cd` to the /tests directory and run the tests with `./runtests`.

That's it! You've successfully configured libvarnam. Now we move onto more exciting parts.

######[Next][input tools]
######[Prev][front page]

[input tools]: guide_input_tools.md
[front page]: guide_front.md