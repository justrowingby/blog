---
title: "Python Setup"
date: 2019-09-03T15:03:43-05:00
draft: true
---

#Python Setup for MacOS
This assumes homebrew is installed.
```
brew install python
```

##Cython:
```
pip install cython
```

##Scientific Computing:
```
pip install numpy
pip install numba
pip install scipy
pip install matplotlib
pip install pandas
pip install pillow
```

##Cartopy:
First, let's get proj@5.2.0
You want this version to avoid throwing errors about an API that's deprecated in later releases:
```
brew tap-new $USER/local-tap
brew extract --version=5.2.0 proj $USER/local-tap
brew install proj@5.2.0
```
The other special case is that Shapely needs to be built sans-binary
```
pip install --no-binary :all: shapely
```
Now the rest is fairly straightforward
```
pip install six
brew install geos
pip install pyshp

pip install Cartopy
```

##OpenCL:
```
python -m pip install pybind11
pip install pyopencl
brew install clblast
```
