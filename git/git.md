# git 学习

## 命令
``` 
git init  
git clone <repo> <directory>  
git remote   
git add  
git push  
git pull  
git fetch  
git commit  
git checkout  
git rebase
git reflog
git log
git branch   
#  
git rm 
# 查看上次提交后是否有修改
git status [-s]                

```

## 创建流程
```
git init  
git add .  
git commit -m 'xxx'    
```

## git remote 
```
git remote add <shortname> <url>
git remote rename <shortname> <newname>

```

## git pull

## git push
```
git push <remote> <branch>
git push xxx -delete xxx
```

## git 撤销操作
会以最新的提交覆盖上一次提交
```
git commit -m "pre commit"
git add a.txt
git commit --amend
git 暂存过后取消某个文件的暂存
git reset HEAD xxxx
git 撤销文件的修改
git checkout -- xxxx
```

## git 打标签
```
git tag
git tag -l "xxx"
git tag -a xxx -m "xxx" # 创建附注标签
git tag show xx
git tag xxx # 创建轻量标签
git tag -a xxx <校验和>
git push <remote> <tagname>
git push <remote> --tags
git tag -d <tagname>
git push <remote> :refs/tags/<tagname>
git push <remote> --delete <tagname>
```

## git checkout 
```
git checkout -b xxx # git branch xxx           git checkout xxx
git checkout --track origin/xxx    # 创建跟踪分支
git checkout xxx     #如果你尝试检出的分支不存在且刚好只有一个名字与之匹配的远程分支，那么 Git 就会为你创建一个跟踪分支
git checkout -b xxx origin/xxxx
```

## git branch
```
git branch --merged
git branch --no-merged
git branch [-u | --set-upstream-to] origin/serverfix #设置已有的本地分支跟踪一个刚刚拉取下来的远程分支，或者想要修改正在跟踪的上游分支
```

## git rest
```
git reset [--soft | --hard] HEAD [^^ | ~2]
```

## git rebase 
```
git rebase <branch>
git rebase --onto master server client # 取出 client 分支，找出它从 server 分支分歧之后的补丁， 然后把这些补丁在master 分支上重放一遍，让 client 看起来像直接基于 master 修改一样
git rebase --continue
```

## gitk&