

## Concepts ##

### 5.2.4 ###

> The `--squash` option takes all the work on the merged branch and
  squashes it into one changeset producing the repository state
  as if a real merge happened, without actually making a merge
  commit. This means your future commit will have one parent only
  and allows you to introduce all the changes from another branch
  and then make more changes before recording the new commit.
  Also the `--no-commit` option can be useful to delay the merge
  commit in case of the default merge process.
  
Explanations: [link1][1] [link2][2]

- `merge --squash` 并不 commit. 而是将被merge branch 的全部
  changes 都 stage 起来，并等待用户commit。用户在commit 之前，可
  以添加其它修改的内容
- 需要注意 `merge --squash` 创建的commit 并不是 merge，而仅仅只是
  commit ，因此不会显示在 `git branch --merged` 的结果中。


[1]:http://stackoverflow.com/questions/3697178/git-merge-all-changes-from-another-branch-as-a-single-commit
[2]:http://stackoverflow.com/questions/19308790/git-branch-merged-no-merged-and-squash-option
