
# 整理提交历史

在真实项目中，我们经常需要整理零碎的提交, 让提交历史更干净易读
本关目标：使用 git rebase、git reset 等命令, 把原本零碎的提交整理成更简洁的历史

在当前仓库中，我们帮你准备了 4 个提交: initial commit、add part1、add part2、add part3

具体任务: 
使用 git rebase 或其它方法把最后的 3 次提交合并成 1 次提交, 合并后, 最终只剩 2 条提交记录: 
  - initial commit
  - 新的提交，包含 part1.txt, part2.txt, part3.txt

完成后运行 /challenge/check 即可获取 flag! 