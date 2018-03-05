# Git
### 初始
```
git init

git remote add origin https://github.com/iyolee/git_test.git

git push --set-upstream origin master
```
### git config
```
查看所有的配置 git config --list

git config --global user.name "lee"
git config --global user.email zhongjianlee@git.com
```
### git add 

### git status
```
git status -s
```
### git diff
```
查看尚未添加到暂存区的变更 git diff
查看已暂存的内容会进入到下一次提交 git diff --staged
```

### git commit
```
重新提交 git commit --amend
```

### git rm
```
目录保留 git rm --cache
```

### git mv
```
git mv README README.md
相当于
mv README README.md
git rm README
git add README.md
```

### git log
```
最近两次提交引入的差异 git log -p -2
每个提交的简要统计信息 git log --stat
美化输出格式 git log --pretty=oneline
```

### git reset
```
移出暂存区 git reset HEAD README.md
```

### git checkout
```
撤销对文件的修改 git checkout -- <filename>
```