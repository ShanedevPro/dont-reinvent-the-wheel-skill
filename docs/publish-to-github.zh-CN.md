# 发布到 GitHub 公开仓库

建议仓库名：

```text
anti-wheel-skill
```

## 最短流程

1. 在 GitHub 创建一个 public repository，名字用 `anti-wheel-skill`。
2. 把压缩包解压到本地（如果是从压缩包来的）。
3. 进入目录。
4. 初始化 Git 并提交：

```sh
git init
git add .
git commit -m "initial anti-wheel skill"
```

5. 连接你的远端仓库并推送：

```sh
git branch -M main
git remote add origin https://github.com/YOUR_NAME/anti-wheel-skill.git
git push -u origin main
```

把 `YOUR_NAME` 替换成你的 GitHub 用户名或组织名。

## 用 `gh` CLI 一步创建并推送

如果你装了 [GitHub CLI](https://cli.github.com/)，可以直接：

```sh
git init
git add .
git commit -m "initial anti-wheel skill"
git branch -M main
gh repo create anti-wheel-skill --public --source=. --remote=origin --push
```

## 如果你已经有 GitHub 仓库

直接在目录里执行：

```sh
git init
git add .
git commit -m "initial anti-wheel skill"
git branch -M main
git remote add origin YOUR_REPO_URL
git push -u origin main
```

## 之后想改成 private

在 GitHub 仓库的 Settings → General → Danger Zone → "Change repository visibility" 里可以随时切换。
