欢迎来到 Git 学习之旅的第四关！

本关任务较为基础，目标是把当前 `main` 分支推送到指定远程仓库，并让本地 `main` 跟踪 `origin/main`。

**具体任务：**

1. 查找并添加远程仓库（本地模拟）。

2. 推送当前分支到远程

完成后运行`/challenge/check`即可获取 flag!

**提示：**

- 远程仓库是本机路径，添加方式与 `file:///…` 或绝对路径相同。  
- 成功推送后，本地 `main` 应显示上游：  
  ```bash
  git status   # On branch main, your branch is up to date with 'origin/main'.
  ```