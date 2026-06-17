# 🌐 部署指南 - 让别人也能访问

## 方法一：Vercel（推荐 ⭐⭐⭐）

**优点：免费、快速、国内可访问、自动HTTPS**

### 步骤：

#### 1️⃣ 注册 Vercel
- 打开 https://vercel.com
- 用 **GitHub账号** 或 **邮箱** 登录（推荐GitHub，方便后续更新）

#### 2️⃣ 上传项目（两种方式选一种）

##### 方式A：拖拽上传（最快，30秒）
1. 打开 https://vercel.com/import
2. 点击 **"Upload"** 标签页
3. 把整个 `weekend-planner` 文件夹拖进去
4. 点击 **Deploy**
5. 等待30秒 → 得到链接 ✅

##### 方式B：通过 GitHub（推荐，方便更新）
1. 在 GitHub 创建新仓库（Private 或 Public 都行）
2. 把项目文件上传到仓库：
   ```bash
   cd weekend-planner
   git init
   git add .
   git commit -m "初始版本"
   git remote add origin https://github.com/你的用户名/weekend-planner.git
   git push -u origin main
   ```
3. 回到 Vercel → **Import Git Repository** → 选择你的仓库
4. 点击 **Deploy**

#### 3️⃣ 获取链接
部署成功后，Vercel 会给你一个类似这样的链接：
```
https://weekend-planner-xxx.vercel.app
```
**把这个链接发给任何人，他们就能打开使用！** 🎉

---

## 方法二：Cloudflare Pages（国内速度最快 ⚡）

### 步骤：
1. 打开 https://pages.cloudflare.com
2. 登录 Cloudflare 账号（免费注册）
3. 点击 **"Create a project"** → **"Direct Upload"**
4. 上传 `weekend-planner` 文件夹（不需要 node_modules）
5. 部署完成 → 得到 `xxx.pages.dev` 链接

---

## 方法三：GitHub Pages（完全免费）

### 步骤：
1. 在 GitHub 创建仓库 `weekend-planner`
2. 上传代码（同方法一的Git步骤）
3. 进入仓库 → **Settings** → **Pages**
4. Source 选择 **Deploy from a branch**
5. Branch 选 **main** / folder 选 **/(root)**
6. 点击 **Save**
7. 等待2分钟 → 访问 `https://你的用户名.github.io/weekend-planner`

---

## 📱 手机访问测试

部署成功后：

1. **手机浏览器打开链接** → 应该能看到完整界面
2. **配置API Key** → 其他人需要自己输入API Key（每人用自己的）
3. **点击导航按钮** → 自动打开高德地图APP

---

## 🔗 自定义域名（可选）

如果想要更好记的域名，比如 `niuniu.example.com`：

### Vercel 自定义域名：
1. Vercel 项目 → **Settings** → **Domains**
2. 输入你的域名（如 `plan.niuniu.com`）
3. 按提示在域名DNS添加CNAME记录

---

## ⚠️ 注意事项

1. **API Key 安全性**
   - API Key 保存在用户浏览器的 localStorage
   - 每个人需要输入自己的 Key
   - 不会泄露给其他人 ✅

2. **无需服务器**
   - 这是纯前端应用，部署后自动运行
   - 不需要你开着电脑 ✅

3. **免费额度**
   - Vercel 免费版：每月100GB流量
   - 对于这个应用完全够用 ✅

---

## 🆘 常见问题

### Q: 国内打不开 Vercel？
A: 一般可以访问。如果不行，用 Cloudflare Pages（国内有节点）

### Q: 想更新代码怎么办？
A: 如果用的 GitHub 方式：`git push` 后 Vercel 自动重新部署

### Q: 可以绑定自己的域名吗？
A: 可以！Vercel 支持免费绑定自定义域名

---

## 🎯 快速开始（推荐流程）

```
1. 注册 GitHub 账号（如果没有）
2. 注册 Vercel 账号（用GitHub登录）
3. GitHub 创建仓库 → 上传代码
4. Vercel 导入仓库 → 一键部署
5. 获得链接 → 发给朋友/评委 👍
```

**总时间：5分钟以内！**
