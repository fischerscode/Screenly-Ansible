# Screenly-Ansible



### Update screenly-ose-ansible dir

```shell
#https://stackoverflow.com/questions/23937436/add-subdirectory-of-remote-repo-with-git-subtree
git checkout screenly-ose/production
git subtree split -P ansible -b temporary-split-branch
git checkout master
git subtree merge --squash -P screenly-ose-ansible temporary-split-branch
# Now fix any conflicts if you'd modified third_party/git-completion.
git branch -D temporary-split-branch
```
