# Fork
# clone
# upstream
- 添加原始仓库作为上游远程源
  git remote add upstream https://github.com/original-owner/repo.git
- 验证远程仓库配置
  git remote -v
# 同步最新代码
- 1. 切换到主分支（通常是 main 或 master）
  git checkout main
- 2. 从上游仓库拉取最新代码
  git fetch upstream
- 3. 合并上游变更到本地分支
  git merge upstream/main
- 4. 推送更新到你的 Fork（保持同步）
  git push origin main

# 创建新分支进行修改
- 创建并切换到新分支（分支名要有描述性）
  git checkout -b fix-typo-docs

# 修改代码并提交
- 添加修改的文件
  git add README.md
- 提交（写清晰的提交信息）
  git commit -m "docs: fix typo in introduction section"

# 推送分支到你的 Fork
  git push origin fix-typo-docs

# 发起 Pull Request (PR)

# 清理分支（合并后）
- 删除本地分支
  git checkout main
  git branch -d fix-typo-docs

# 删除远程分支（可选）
git push origin --delete fix-typo-docs

# 查看远端的origin与upstream信息
git remote -v
