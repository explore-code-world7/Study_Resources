# upload repository

* generate keys

```bash
ssh-keygen -t  rsa -f /path/to/key/name/without/suffix
# default
cat ~/.ssh/id_rsa.pub
# if setting keyfile's location
cat /path/to/key/name/without/suffix.pub
```

* 将密钥添加到ssh-agent中，这样重装也能用

```bash
eval "(ssh-agent -s)"
# 添加密钥
ssh-add  /path/to/key/name/without/suffix
# list out& delete
ssh-add -l
ssh-add -d /path/to/key/name/without/suffix
```

* choose github界面的ssh login/upload

* push to server

```bash
git push origin main
```

## remote: error: GH007: Your push would publish a private email address.

[link](https://stackoverflow.com/questions/43863522/error-your-push-would-publish-a-private-email-address)

- local email address不要设置得和github email addressx相同
  
  ```bash
  git config --global user.email "{ID}+{username}@users.noreply.github.com"
  ```
  
  ```bash
  git commit --amend --reset-author --no-edit
  ```

## change default branch

- Setting/Repositories/branch

# delete commit points

[link](https://stackoverflow.com/questions/1338728/how-do-i-delete-a-commit-from-a-branch)

## Method 1:

```bash
git stash
git reset --hard branch_id
git stash pop/apply
git add .
git commit -m "illustration"
```

## Method 2:

```bash
git rebase -i branch_id
```

* 配置编辑器
  
  ```bash
  git config --global core.editor "code --wait"  # 使用 VS Code
  git config --global core.editor "vim"   # 使用 vim
  git config --global core.editor "nano"  # 使用 nano
  ```

* 在git.rebase-todo文件中，保留需要的分支，删除不要的，close即可

# push to private server

## first push

* 本机仓库添加服务器addr

```python
git remote remove server
git remote add server  ssh://chenlei@10.15.82.118:10022/home/chenlei/IsaacLab/.git
```

* 注意服务器上，先建立~/IsaacLab空目录，之后直接`git init`的分支是"master"
  
  要切换分支

```python
git checkout main
```

* 本机执行推送

```bash
git push server main
```

```bash
枚举对象中: 24377, 完成.
对象计数中: 100% (24377/24377), 完成.
使用 16 个线程进行压缩
压缩对象中: 100% (8602/8602), 完成.
写入对象中: 100% (24377/24377), 37.84 MiB | 9.50 MiB/s, 完成.
总共 24377（差异 14260），复用 23935（差异 13996），包复用 0
remote: Resolving deltas: 100% (14260/14260), done.
To ssh://10.15.82.118:10022/home/chenlei/IsaacLab/.git
 * [new branch]          main -> main
```

## later push

* 之后的推送可能遇到如下问题

```bash
Git push error '[remote rejected] master -> master (branch is currently checked out)'
```

https://stackoverflow.com/questions/2816369/git-push-error-remote-rejected-master-master-branch-is-currently-checked

* 解决办法
1. 服务器设为中央仓库，接受推送

```bash
git  config  --bool  core.bare true
```

2. 推送代码

```bash
git push server main
```

3. 关闭中央 仓库，来进行git reset, git add ., git commit等操作

```bash
git config --bool core.bare true
```

4. 需要推到服务器的时候服务器再次设为中央仓库即可～

## bare_repo

https://stackoverflow.com/questions/2816369/git-push-error-remote-rejected-master-master-branch-is-currently-checked

# submodule
