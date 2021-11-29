
#git #删除 #rm #历史文件
* 确保本地仓库最新
* 项目下检查大文件
```git
git rev-list --all | xargs -rL1 git ls-tree -r --long | sort -uk3 | sort -rnk4 | head -10
```
* 删除文件，修改{filepath}，如果是文件夹，修改参数 -f 为-rf
```git
git filter-branch --tree-filter "rm -f {filepath}" -- --all
```
* 强制提交远程仓库
```git
git push -f --all
```