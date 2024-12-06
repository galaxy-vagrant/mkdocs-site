## tag

在 Git 中，标签（tag）用于标记特定的提交点，通常用于标记发布版本。你可以使用 `git tag` 命令来创建标签，并使用 `git push` 命令将其推送到远程仓库。以下是具体步骤：

### 1. 创建标签

你可以使用 `git tag` 命令来创建一个标签。标签可以附加到特定的提交上，通常是你希望标记的提交。

#### 创建一个轻量级标签

轻量级标签只是指向特定提交的引用，不包含其他信息。

```sh
git tag <tag-name> <commit-hash>
```

例如，标记当前最新提交为 `v1.0`：

```sh
git tag v1.0
```

或者，标记特定的提交（使用提交哈希）：

```sh
git tag v1.0-beta a1b2c3d4e5f6
```

#### 创建一个带注释的标签

带注释的标签包含标签信息（如消息、签名等），通常用于发布版本。

```sh
git tag -a <tag-name> -m "Your tag message" <commit-hash>
```

例如：

```sh
git tag -a v1.0 -m "Release version 1.0"
```

### 2. 查看标签

你可以使用 `git tag` 命令查看所有本地标签：

```sh
git tag
```

### 3. 推送标签到远程仓库

标签创建后，你需要将其推送到远程仓库，以便其他人可以获取。

```sh
git push origin <tag-name>
```

例如：

```sh
git push origin v1.0
```

或者，推送所有标签：

```sh
git push origin --tags
```

### 4. 验证标签

在远程仓库中，你可以验证标签是否已成功推送。例如，在 GitHub 上，你可以在仓库的 "Releases" 页面查看标签。

### 5. 检出标签

虽然标签通常用于标记特定的提交点，但你也可以检出标签以查看该提交时的代码状态。注意，检出标签会处于“分离 HEAD”状态，这意味着你无法在该状态下进行提交。

```sh
git checkout <tag-name>
```

例如：

```sh
git checkout v1.0
```
