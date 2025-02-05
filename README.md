# pyinstall-demo
介绍pyinstall打包的一个示例项目


```shell

pyinstaller --onefile --add-data="util:util" --exclude-module=pyinstaller  main.py 
```

--add-data="source-data;dist-data" 的含义：
source-data 是你要打包的文件夹路径（相对于当前目录）。
dist-data 是打包后文件夹在 .exe 文件内部的路径。

--exclude-module 用来排除不需要的包（默认情况下，pyinstall会默认分析不需要的包，因此一般不用写），减少打包的体积,如果需要排除多个包，写多个--exclude-module即可