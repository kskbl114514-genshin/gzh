---
name: "git-commit-push"
description: "提交项目并 push 到 Gitee 远程仓库。当用户说'提交项目'、'commit and push'、'推送到gitee'、'提交并推送代码'时触发。"
---

# git-commit-push

## Description
提交项目：使用 git commit 并 push 当前项目到 https://gitee.com/whalefox/gzh2

## Instructions
When this skill is invoked, perform the following steps:

1. Check current git status (`git status`)
2. Stage all changes (`git add -A`)
3. Create a commit with a descriptive message summarizing the changes
4. Push to the remote repository:
   - If remote `origin` is not set, add it: `git remote add origin https://gitee.com/whalefox/gzh2.git`
   - If the branch has no upstream, use: `git push -u origin main`
   - Otherwise use: `git push`
5. If push fails with "repository not found", inform the user that the Gitee repository needs to be created first at https://gitee.com/whalefox/gzh2

## Trigger
User asks to commit and push the project to Gitee.

## Example prompts that should trigger this skill:
- "提交项目"
- "commit and push"
- "推送到gitee"
- "提交并推送代码"
