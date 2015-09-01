# README #

This README would normally document whatever steps are necessary to get your application up and running.

### PadeOps ###

* Quick summary : Hybrid OpenMP/MPI derivative operators using Compact Difference (6th and 10th Order) and Spectral (Fourier and Chebyshev) Methods to solve PDEs.
* Version : 0.1
* Tutorials : TBD/Incomplete

### How do I get set up? ###

* Summary of set up
* Configuration :
    * The Fortran compiler (FC) (preferably even the CC and CXX variables) need to be set to the desired MPI fortran compiler. Also the FFTW library path (FFTW_PATH) and 2DECOMP&FFT library path (DECOMP_PATH) need to be set.
    * Examples of this are in the setup folder. For your system, either use one of the SetupEnv_<Machine>\_<CompilerID>.sh files or copy the closest one to your own SetupEnv_<Machine>\_<CompilerID>.sh. Then, from the main directory (PadeOps), run `source setup/SetupEnv_<Machine>_<CompilerID>.sh` to set the correct environment variables.

    * Now, build the required dependencies:
         * FFTW
             * Extract the fftw-<version>.tar.gz file in the dependencies folder. Change directory using `cd fftw-<version>.tar.gz`. Set the envireonment variables `F77` and `MPICC` to the correct fortran and MPI C compilers. Configure the build using $./configure --prefix=<current directory>$. Then build the library using `make; make install`. At the end of this, there should be a folder in this directory called `lib` and a folder called `include` with the static library file and the include files respectively.
         * 2DECOMP&FFT
         * Lib_VTK_IO
              * Extract the Lib_VTK_IO.tar.gz file and `cd` into the created directory. Make a build directory and move to it using `mkdir build; cd build`. Then build the library using `cmake ..; make`. Now, set the VTK_IO_PATH to the current directory in your SetupEnv.sh script. 

    * To build the code, run the following commands:
~~~
           mkdir build
           cd build
           cmake ..
           make
~~~
* Dependencies :
    * CMake 2.8 or above
    * MPI Library (https://www.mpich.org/)
    * FFTW (www.fftw.org/)
    * 2DECOMP&FFT (http://www.2decomp.org/)
* Database configuration : TBD
* How to run tests : TBD
* Deployment instructions : TBD

### Contribution guidelines ###

* TBD

### Who do I talk to? ###

* Akshay Subramaniam or Aditya Ghate