欢迎来到 Git 学习之旅的第一关！

本关任务较为基础，目标是让你学会如何查看 Git 提交历史，并回退到指定版本。

**具体任务：**

1. 把仓库恢复到 _answer.txt_ 第一次被添加时的状态。

2. 配置 Git 用户信息, 例如:
```
   git config user.name "pwnuser"
   git config user.email "pwn@hust.edu.cn"
```
3. 使用：
      - `git log` 查看提交历史 
      
      - `git diff` 确认文件差异 
4. 找到提交信息为 **“Add correct answer”** 的那一版 

5. 让当前 **HEAD** 指向该提交 

   - 可以 `git checkout <commit>`（会进入 detached HEAD）

   - 也可以 `git reset --hard <commit>`（回滚分支） 

完成后运行
```
   /challenge/check 
```   
即可获取 flag!


