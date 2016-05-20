- add添加要提交的文件的时候，如果文件名是中文，会显示形如274\232\350\256\256\346\200\273\347\273\223.png的乱码。
**解决方案：**
在bash提示符下输入：
```
git config --global core.quotepath false
```
> core.quotepath设为false的话，就不会对0×80以上的字符进行quote。中文显示正常。

- git remote -v 
> 查看远程仓库路径。路径为git://开头的时候不能push文件，需要改成git@开头 或者https://开头

- git reset --hard HEAD^
> 硬回退到上个版本，当前变化过得的已跟踪的文件全部删除（危险）

- git clean -fd
> 删除所有没有add（untracking）过得文件
