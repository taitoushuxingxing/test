#测试由cmake生成.sln解决方案

1.文件目录
   /code/main.cpp
  /code/CMakeLists.txt
 2.进入debug,生成debug解决方案
cd ../debug
cmake -G "Visual Studio 16 2019" -DCMAKE_BUILD_TYPE=Debug -A Win32 ../code
3.编译
msbuild /m TestVsCMake.sln /p:Platform="Win32" 
4.进入debug目录，即可看到生成的解决方案，相比于直接在vs studio创建解决方案，分离了代码和编译后的内容，更方便管理以及git推送。