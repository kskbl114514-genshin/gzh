---
name: git-push-github
description: 提交项目并 push 到 GitHub 远程仓库 kskbl114514-genshin/gzh。当用户说'提交到github'、'推送到github'、'commit and push to github'、'提交并推送到github'时触发。不要用于推送到 Gitee（改用 git-commit-push）。
---

# git-push-github

## Description
提交到github：使用 git commit 并 push 当前项目到 GitHub 仓库 https://github.com/kskbl114514-genshin/gzh.git（SSH 公钥已配置）。

## Instructions
When this skill is invoked, perform the following steps:

1. Check current git status (`git status`)
2. Stage all changes (`git add -A`)
3. Create a commit with a descriptive message summarizing the changes
4. Push to the GitHub remote repository:
   - If remote `origin` is not set, add it with the SSH URL: `git remote add origin git@github.com:kskbl114514-genshin/gzh.git`
   - If remote `origin` exists but points to another URL (e.g. Gitee), add a separate remote: `git remote add github git@github.com:kskbl114514-genshin/gzh.git` and push to `github` instead
   - If the branch has no upstream, use: `git push -u <remote> main`
   - Otherwise use: `git push <remote> main`
5. If push fails with "Repository not found", inform the user that the GitHub repository needs to be created first at https://github.com/kskbl114514-genshin/gzh
6. If SSH authentication fails, verify the key with `ssh -T git@github.com`

## Trigger
User asks to commit and push the project to GitHub.

## Example prompts that should trigger this skill:
- "提交到github"
- "推送到github"
- "commit and push to github"
- "提交并推送到github"
