## About ##

This code is about .pcd to .bin converting tool.  
PointCloud(.pcd) file includes `x, y, z, intensity, (ring, time)` data.  
You can convert all the .pcd files (sorted in ascending order by file name) in the directory.  

## How to use ##
### 0. Environment ###
Python 2.7

### 1. Install python libraries ###
`$ pip install numpy`  
`$ pip install argparse`  
`$ pip install pypcd`  
`$ pip install tqdm`  

### 2. Launch python file ###
~~`$ python pcd2bin.py --pcd_path={path of input pcd file directory} --bin_path={path of output bin file directory}  --file_name={name of bin file}`~~

`$ python pcd2bin.py --pcd_path={path of input pcd file directory} --bin_path={path of output bin file directory}`

#### Parameters ####
|Name|Description|Default value|
|:---|:---|:---|
|pcd_path|.pcd file path|"/home/user/lidar_pcd"|
|bin_path|.bin file path|"/home/user/lidar_bin"|
|~~file_name~~|~~.bin file name~~|~~"file_name"~~|


### Possible error

#### 1. Microsoft Visual C++ 9.0 is required
```
building 'lzf' extension
error: Microsoft Visual C++ 9.0 is required. Get it from http://aka.ms/vcpython27
```
The url http://aka.ms/vcpython27 is no longer valid.
You can install vcForPYTHon27.msi directly.

#### 2. failed with exit status 2
```
error: command ‘C:\Users\***\AppData\Local\Programs\Common\Microsoft\Visual C++ for Python\9.0\VC\Bin\amd64\cl.exe’ failed with exit status 2
```
Put stdint.h into `C:\Users\***\AppData\Local\Programs\Common\Microsoft\Visual C++ for Python\9.0\VC\include`