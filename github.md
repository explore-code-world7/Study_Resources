# Procedure
* generate keys

```bash
ssh-keygen -t  rsa
cat ~/.ssh/id_rsa.pub
```

* choose ssh login/upload

# change default branch
* Setting/Repositories/branch


# remote: error: GH007: Your push would publish a private email address.
[link](https://stackoverflow.com/questions/43863522/error-your-push-would-publish-a-private-email-address)
* local email address不要设置得和github email addressx相同
```bash
  git config --global user.email "{ID}+{username}@users.noreply.github.com"
```
```bash
git commit --amend --reset-author --no-edit
```
