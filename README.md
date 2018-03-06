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

### git tag
```
创建注释标签 git tag -a v1.0.0 -m "my version 1.0.0"
查看标签 git tag
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