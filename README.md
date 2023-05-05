# C++项目模板  
### 开发环境  
Windows：CMake、MinGW(可选)、MSBuild  
Linux：CMake、GCC  
### 部署项目  
1.获取子模块  
```
git submodule update --init --recursive --remote --progress
```
2.获取包管理工具  
```
./vcpkg/bootstrap-vcpkg.bat
```
3.安装依赖库  
MinGW：  
```
./vcpkg/vcpkg.exe install <包名> --triplet x64-mingw-static
```
Windows和Linux：  
```
./vcpkg/vcpkg.exe install <包名>
```
### 构建项目  
MinGW：  
1.生成项目  
```
cmake -Bbuild -G "MinGW Makefiles" -DVCPKG_TARGET_TRIPLET="x64-mingw-static"
```
2.编译项目  
```
cd ./build
mingw32-make
```
Windows：  
1.生成项目  
```
cmake -Bbuild -G "MinGW Makefiles"
```
2.编译项目  
```
cd ./build
使用vs编译
```
Linux：  
1.生成项目  
```
cmake -Bbuild -G "Unix Makefiles"
```
2.编译项目  
```
cd ./build
make
```
