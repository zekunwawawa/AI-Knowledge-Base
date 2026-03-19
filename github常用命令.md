### 🎯 GitHub 常用 Git 命令总结（按场景分类） 以下是你管理 Obsidian 知识库最常用的命令，按「初始化/日常更新/问题修复」分类，新手直接复制用就行！ --- 
## 一、仓库初始化（仅第一次用） 
### 1. 本地初始化仓库（在知识库文件夹执行） 
```bash git init # 生成.git文件夹，标记为Git仓库 ``` 
### 2. 关联GitHub远程仓库（替换成你的仓库地址） 
```bash git remote add origin https://github.com/你的用户名/AI-Knowledge-Base.git ``` 
### 3. 首次推送到
GitHub ```bash git add . 
# 添加所有文件到暂存区 
git commit -m "初始化AI知识库" 
# 提交到本地仓库 
git push -u origin main # 推送到GitHub（-u绑定分支，后续可简化） ``` 
--- 
## 二、日常更新知识库（最常用） 
### 1. 查看文件变更状态（可选，确认要提交的内容） 
```bash git status # 显示哪些文件被修改/新增/删除 ``` 
### 2. 提交更新（三步曲） ```
bash git add . # 全部文件更新（推荐） #或只提交指定文件：
git add AI知识大扫盲/大语言模型.md 
git commit -m "更新：新增Transformer知识点/修复大语言模型笔记错误" # 描述要清晰 
git push # 推送到GitHub（首次绑定后可省略origin main） ``` --- 
## 三、仓库基础操作（查/切/删） 
### 1. 查看远程仓库关联信息 
```bash git remote -v # 查看当前关联的GitHub仓库地址 ``` 
### 2. 修改远程仓库地址（如果仓库名/用户名改了） 
```bash git remote set-url origin https://github.com/新用户名/新仓库名.git ``` 
### 3. 查看提交历史（追溯修改记录） 
```
bash git log # 查看所有提交记录（按q退出） 
git log --oneline # 简洁版日志（只显示提交ID和说明） 
``` 
--- 
## 四、问题修复/回滚（踩坑时用） 
### 1. 撤销暂存区文件（add错了文件）```
bash git reset HEAD # 撤销所有add的文件 # 或撤销指定文件：
git reset HEAD AI知识大扫盲/测试笔记.md ``` 
### 2. 放弃本地修改（还没commit，想恢复到上次提交状态） ```
bash git checkout -- . # 放弃所有本地修改 # 或放弃指定文件：
git checkout -- AI知识大扫盲/错误笔记.md ``` 
### 3. 拉取GitHub最新版本（多人协作/其他设备更新后同步） ```
bash git pull # 拉取远程仓库最新内容（本地没冲突时直接用） ``` 
### 4. 解决推送冲突（本地和远程版本不一致） ```
bash git pull --rebase origin main # 先拉取并合并远程修改，再推送 
git push # 合并后重新推送 ``` --- 
## 五、跨设备同步（新电脑拉取知识库） 
### 1. 克隆GitHub仓库到本地（新设备） ```
bash git clone https://github.com/你的用户名/AI-Knowledge-Base.git # 下载整个仓库到当前目录 ``` --- 
### 📌 核心总结 
1. **日常更新核心**：`git status` → `git add .` → `git commit -m "说明"` → `git push`； 
2. **初始化核心**：`git init` → `git remote add` → `git push -u origin main`；
3. **出错修复**：`git reset`（撤销add）、`git checkout`（放弃修改）、`git pull`（拉取同步）。 
4. 所有命令都要在你的 `my knowledge` 文件夹下执行，记不住可以收藏这份清单，用的时候直接查！