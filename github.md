# upload repository
* generate keys

```bash
ssh-keygen -t  rsa
cat ~/.ssh/id_rsa.pub
```

* choose ssh login/upload
## remote: error: GH007: Your push would publish a private email address.
[link](https://stackoverflow.com/questions/43863522/error-your-push-would-publish-a-private-email-address)
* local email address不要设置得和github email addressx相同
```bash
  git config --global user.email "{ID}+{username}@users.noreply.github.com"
```
```bash
git commit --amend --reset-author --no-edit
```
## change default branch
* Setting/Repositories/branch

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
