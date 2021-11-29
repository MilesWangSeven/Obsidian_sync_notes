#submodule #gitmodules
#3 fatal: No url found for submodule path ‘xxx/xxx’ in .gitmodules
1.  windows上add submodule
2.  git submodule init时发生错误
3.  查看.gitmodules内容如下
```shell
[submodule ".\\components\\ft_crc\\"]
	path = .\\components\\ft_crc\\
	url = git@192.168.1.197:finsiot/ft_crc.git
 ```
 修改为
 ```shell
 [submodule "components/ft_crc/"]
 	path = components/ft_crc
 	url = git@192.168.1.197:finsiot/ft_crc.git
```
4. 执行
```git
git submodule init
git submodule sync
git submodule update
```
总结,  
1. git submodule add [path] 路径中不要写./  
2. windows上添加子模块后最好改把.gitmodule的路径反斜杠改下