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
```
将(被版本库追踪的)本地文件的变更(修改、删除)全部记录到暂存区中 git add -u
将工作区中的所有改动及新增文件添加到暂存区 git add -A
```

### git status
```
git status -s
```
### git diff
```
查看尚未添加到暂存区的变更 git diff
查看已暂存的内容会进入到下一次提交 git diff --staged
暂存区和HEAD比较 git diff --cached
工作区和HEAD比较 git diff HEAD
```

### git commit
```
重新提交 git commit --amend

commit message
格式： <type>(<scope>): <subject>
1. type-提交commit的类型
- feat: 新功能
- fix: 修复问题
- docs: 修改文档
- style: 修改代码样式，不影响代码逻辑
- refactor: 重构代码，理论上不影响现有功能
- perf: 提升性能
- test: 增加修改测试用例
- chore: 修改工具相关（包括但不限于文档，代码生成等）
- deps: 依赖升级
2. scope-修改文件的范围，可选，包括但不限于doc、plugins等
3. subject-用一句话清楚的描述这次提交做了什么
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
美化输出格式 git log --pretty=oneline    git log --oneline
```

### git reset
```
移出暂存区(git add反向操作) git reset HEAD README.md  git reset --soft HEAD^
上一个提交 git reset --hard HEAD^
任意一次提交 git reset--hard 9e8a761
查询到最早的提交ID git log --graph --oneline
工作区不改变,但是暂存区会回退到上一次提交之前,引用也会回退一次 git reset --mixed HEAD^
```

### git checkout
```
撤销对文件的修改 git checkout -- <filename>
恢复删除的文件 git checkout HEAD~1 -- welcome.txt
(HEAD~1即相当于HEAD^都指的是HEAD的上一次提交)
```

### git rebase 及一些规则
- 不使用 git pull 与 git merge。（git pull = git fetch + git merge）
- commit之后发现，远程 develop 分支已经有其他人已经commit并合并了。 那你应该在你的分支上：
    - git fetch
    - git rebase -i origin/develop
- 可以对你开发的分支进行各种操作 以及pull -f，但禁止直接操作 develop

### git stash
```
保存工作进度 git stash
显示进度列表 git stash list
恢复 git stash apply
```

### git tag
```
创建注释标签 git tag -a v1.0.0 -m "my version 1.0.0"
查看标签 git tag
```

### git reflog
```
master分支指向的变迁 git reflog show master|head -5
重置master为两次改变之前的值 git reset--hard master@{2}
```

### 分支
```
创建分支 git branch testing
切换分支 git checkout testing
相当于 git checkout -b testing

合并 git merge testing

删除分支 git branch -d testing
```

### 其他
- 避免https每次手动输密码 git config --global credential.helper cache