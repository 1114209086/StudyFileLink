### VI编辑
1.  vi filename 编辑某个文件  
2.  i 进行编辑模式 （ 非编辑模式下 ）
3.  Esc 退出编辑模式 （编辑模式下 ）
4.  ：wq 保存关闭 （非编辑模式下 ）
### GIT
echo "# test" >> README.md  
git init  
git add README.md  （git add . 添加所有改动/ git add --update）
git commit -m "first commit"  
git remote add origin git@github.com:1114209086/test.git  
git push -u origin master  
git status  
git stash 	                             隐藏本地的改动  
git  pull --rebase 	                     拉最新的代码，忽略本地改动  
git stash pop	                           本地改动显示出来  
ll -la	                                 显示隐藏文件  
git diff file	                           查看文件的改动  
git clone -b [branchname] [url]	         clone code  
git log -p [filename]                    查看文件的log  
git checkout [filename]                  check out 文件的改动  
git reset [filename]                     reset commit 的代码  
git reset HEAD~1                         push 冲突，多一次提交，回退  
git diff --cached / $ git diff --staged                        add 之后查看改动  
touch .gitignore                         生成gitignore
### Other
$ ssh-keygen -t rsa                    生成ssh key

