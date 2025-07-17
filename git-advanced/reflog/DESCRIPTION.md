# Git 关卡 · Reflog 深度恢复挑战

> **目标：** 使用 `git reflog` 找回一条被 reset 丢失的提交。

## 背景

你曾提交过一个重要文件 `secret.txt`，但在后续提交和一次 reset 操作中被意外丢弃。

现在 `git log` 中已经找不到相关记录。

请你：

1. 使用 `git reflog` 查看 HEAD 历史变动
2. 找到那次添加 `secret.txt` 的提交
3. 使用 `git checkout` 或 `git reset --hard` 恢复到该提交

完成后执行：

```bash
/challenge/check

