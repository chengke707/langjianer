# 程柯 · 个人简历网站

一个现代化、简洁专业的静态个人简历展示网站。纯前端、无后端，面向企业 HR 浏览场景设计，电脑端体验最佳。

## 项目文件清单

| 文件 / 文件夹 | 作用 |
| --- | --- |
| `index.html` | 网站主页面（样式、交互全部内置在这一个文件里） |
| `avatar.jpg` | 头像照片 |
| `certs/` | 证书扫描件图片（共 5 张，点击证书卡片可查看大图） |
| `.github/workflows/deploy-pages.yml` | GitHub Pages 自动部署工作流（方式二用，方式一用不到） |
| `README.md` | 本说明文档 |

---

## 一、本地预览（不用上网）

直接**双击 `index.html`**，浏览器就会打开网站。改完代码刷新页面即可看到最新效果。

---

## 二、部署到 GitHub Pages（方式一 · 最简单，推荐）

全程只用浏览器点鼠标，不需要安装任何软件、不需要敲命令。免费，无需自定义域名。

### 第 1 步：登录 GitHub

用浏览器打开 https://github.com ，登录账号 `chengke707`。

### 第 2 步：新建一个仓库

1. 点右上角的 **+** 号 → **New repository**
2. **Repository name** 填：`langjianer`
3. 选 **Public**（公开，免费的 Pages 必须公开）
4. 其他什么都不用勾选（**不要**勾 "Add a README file"）
5. 点绿色按钮 **Create repository**

### 第 3 步：把文件传上去

1. 进入刚建好的仓库页面，点 **Add file** → **Upload files**
2. 打开本地 `chengke-resume` 文件夹，**全选**里面的所有文件和文件夹（`index.html`、`avatar.jpg`、`certs` 文件夹，连同 README 一起也没关系）
3. 一起**拖进**网页的上传框里
4. 等文件上传完成，点绿色按钮 **Commit changes**（提交信息不用改，直接点）

> 注意：`certs` 文件夹要整个文件夹拖进去，网页会自动保留文件夹结构。

### 第 4 步：开启 Pages

1. 仓库页面上方点 **Settings**（设置）
2. 左侧菜单找到 **Pages**
3. 在 **Build and deployment** 区域：
   - **Source** 下拉框选 **Deploy from a branch**
   - **Branch** 下拉框选 **main**，旁边文件夹选 **/ (root)**
4. 点 **Save**

### 第 5 步：拿到网址

1. 回到 **Settings → Pages** 页面，等大约 1～2 分钟
2. 页面顶部会出现一行蓝底提示：**"Your site is live at https://chengke707.github.io/langjianer/"**
3. 打开这个网址，网站就上线了，任何人、任何设备都能访问

**这个网址就是你的在线简历，可以直接发给 HR。**

---

## 三、方式二：用自动化工作流部署（.yml 文件）

项目里已经配好了 `.github/workflows/deploy-pages.yml`，想要自动化部署的话这样操作：

1. 完成上面方式一的第 1、2、3 步（上传文件时**连同 `.github` 文件夹一起拖进去**，不要漏掉）
2. 进 **Settings → Pages**
3. **Source** 下拉框选 **GitHub Actions**
4. 点仓库上方 **Actions** 标签页，可以看到一个叫 **Deploy static content to Pages** 的任务自动开始跑
5. 等它变成绿色对勾 ✅（约 1 分钟），回到 **Settings → Pages** 页面就能看到网址

两种方式效果完全一样，选一种即可。

---

## 四、以后怎么更新内容

> 打开 `index.html` 文件最上面有一段「自定义指南」，写明了每类内容在哪里改。

### 改文字、改项目经历

1. 打开仓库里的 `index.html`
2. 点右上角**铅笔图标**（编辑）
3. 改完后点 **Commit changes**
4. 等约 1 分钟，刷新网址即可看到新内容

### 换头像

1. 准备一张新照片，文件名改成 `avatar.jpg`
2. 在仓库里打开旧 `avatar.jpg` → 右上角**垃圾桶图标**删除 → 提交
3. 再用 **Add file → Upload files** 把新 `avatar.jpg` 传上去
4. 刷新网址

### 加一张新证书

1. 把证书图片放进本地 `certs` 文件夹（随便起个英文名，如 `cert-new.jpg`）
2. 用 **Add file → Upload files** 把它传到仓库的 `certs` 文件夹里
3. 让我帮你在页面里加上对应的证书卡片（或者照着现有卡片照抄一段）

---

## 五、常见问题

| 问题 | 解决办法 |
| --- | --- |
| 打开网址显示 404 | 检查网址是否带上了仓库名后缀 `/langjianer/`；刚部署完要等 1～2 分钟 |
| 网站出来了但图片不显示 | 确认 `avatar.jpg` 和 `certs` 文件夹已上传，且文件名与页面里写的一致 |
| 修改后网站没变化 | 等 1 分钟左右再刷新；或按 Ctrl+F5 强制刷新 |
| 网址太长了想要好记的 | 免费的固定网址就是这种形式，自定义域名需要付费购买，不推荐 |
