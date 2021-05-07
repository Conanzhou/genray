# Build instructions for Ubuntu 18.04
First install gcc9-fortran from arch4edu
```
yay gcc9-fortran
```
Then change the makefile **makefile_gfortran64** to make gfortran-9 be the default gfortran
```
vim makefile_gfortran64
```
Just change the line
```
COMPILER=	gfortran
```
to
```
COMPILER=	gfortran-9
```

Install dependencies

```
#yay nco(actually i do not know which pkg the nco means )
yay -S netcdf pgplot
```
Build & test
```
make -f makefile_gfortran64 clean
make -f makefile_gfortran64
ctest
```

