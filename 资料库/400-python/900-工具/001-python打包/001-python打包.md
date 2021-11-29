python打包可选择 #python #exe #tool
[# Python程序打包成exe可执行文件](https://blog.csdn.net/zengxiantao1994/article/details/76578421)
![[900-python打包工具.png]]

对于那些网络比较稳定，能够流畅使用pip源地址的用户，直接下面的命令就可以搞定：
python -m pip install pyinstaller

通常我们会下载源码包，然后进入包目录，执行下面的命令（需要安装setuptools）：
python setup.py install
安装完后，检查安装成功与否：
pyinstaller --version

如果想只打包成一个exe：
 pyinstaller -F path\\mycode.py --noconsole
 dist里有对应.exe文件