# 📦 NPM 包管理指南

Modern Homepage 现已支持通过 NPM 进行安装和管理，让您可以更轻松地创建和更新个人主页项目。

## 🚀 快速开始

### 方式一：使用脚手架创建项目（推荐）

```bash
# 创建新项目
npx create-homepage my-homepage

# 进入项目目录
cd my-homepage

# 安装依赖
npm install

# 启动开发服务器
npm run dev
```

### 方式二：手动安装

```bash
# 创建项目目录
mkdir my-homepage
cd my-homepage

# 初始化 npm 项目
npm init -y

# 安装模板包
npm install @penjc/homepage

# 安装依赖
npm install next react react-dom typescript
```

## 📋 包信息

- **包名**: `@penjc/homepage`
- **仓库**: https://github.com/penjc/homepage
- **NPM**: https://www.npmjs.com/package/@penjc/homepage

## 🛠️ CLI 工具

### homepage

创建和管理个人主页项目的CLI工具。

```bash
# 创建新项目
npx @penjc/homepage create [项目名称]

# 示例
npx @penjc/homepage create my-blog
npx @penjc/homepage create john-portfolio
```

**功能特性：**
- ✅ 自动复制模板文件
- ✅ 生成示例配置文件
- ✅ 创建示例内容
- ✅ 配置项目依赖
- ✅ 生成项目文档

### 更新项目

更新现有项目的框架版本。

```bash
# 在项目根目录中运行
npx @penjc/homepage update
```

**功能特性：**
- ✅ 自动备份重要文件
- ✅ 检查版本更新
- ✅ 更新框架依赖
- ✅ 验证配置文件
- ✅ 运行构建测试

## 📁 项目结构

使用 CLI 创建的项目结构：

```
my-homepage/
├── app/                    # Next.js App Router
├── components/             # 可复用组件
├── lib/                    # 工具函数
├── content/               # 内容文件
│   ├── blog/             # 博客文章
│   └── thoughts/         # 随笔记录
├── public/               # 静态资源
│   └── images/           # 图片资源
├── styles/               # 样式文件
├── site.config.ts        # 站点配置
├── package.json          # 项目依赖
└── README.md             # 项目文档
```

## ⚙️ 配置管理

### 站点配置

编辑 `site.config.ts` 文件来自定义您的网站：

```typescript
export const siteConfig = {
  // 基本信息
  name: "Your Name",
  title: "您的个人主页",
  description: "个人简介",
  url: "https://yourdomain.com",
  
  // 个人信息
  profile: {
    avatar: "/images/avatar.jpg",
    bio: "您的个人介绍",
    email: "your@email.com",
    github: "https://github.com/username",
  },
  
  // 更多配置...
};
```

### 配置验证

```bash
# 验证配置文件
npm run verify-config
```

## 🔄 版本更新

### 检查更新

```bash
# 检查当前版本
npm list @penjc/homepage

# 检查最新版本
npm view @penjc/homepage version
```

### 更新方式

#### 自动更新（推荐）

```bash
# 使用 CLI 工具更新
npx @penjc/homepage update
```

#### 手动更新

```bash
# 更新到最新版本
npm update @penjc/homepage

# 更新到特定版本
npm install @penjc/homepage@^2.0.0
```

### 更新流程

1. **备份重要文件**
   - `site.config.ts`
   - `content/` 目录
   - `public/images/` 目录
   - `.env.local`

2. **更新框架包**
   - 下载最新版本
   - 更新依赖

3. **验证配置**
   - 检查配置文件兼容性
   - 运行构建测试

4. **完成更新**
   - 提供更新报告
   - 生成备份记录

## 📦 包的版本管理

### 语义化版本

Modern Homepage 遵循 [语义化版本](https://semver.org/lang/zh-CN/) 规范：

- **主版本号**：不兼容的 API 修改
- **次版本号**：向下兼容的功能性新增
- **修订号**：向下兼容的问题修正

### 版本选择

```json
{
  "dependencies": {
    "@penjc/homepage": "^1.0.0"  // 推荐：自动获取小版本更新
    "@penjc/homepage": "~1.0.0"  // 保守：仅获取补丁更新
    "@penjc/homepage": "1.0.0"   // 固定：锁定特定版本
  }
}
```

## 🔒 内容保护

### 安全的文件

更新时不会被覆盖的文件：

- ✅ `content/blog/` - 您的博客文章
- ✅ `content/thoughts/` - 您的随笔内容
- ✅ `public/images/` - 您的个人图片
- ✅ `site.config.ts` - 您的配置文件（可能需要手动合并）
- ✅ `.env.local` - 环境变量

### 需要注意的文件

可能在更新时发生变化：

- ⚠️ `package.json` - 依赖版本更新
- ⚠️ `next.config.js` - 框架配置更新
- ⚠️ `tailwind.config.js` - 样式配置更新

### 会被更新的文件

框架核心文件，更新时会被覆盖：

- 🔄 `app/` 目录 - 页面和布局组件
- 🔄 `components/` 目录 - 可复用组件
- 🔄 `lib/` 目录 - 工具函数

## 🚀 部署

### 构建项目

```bash
# 构建生产版本
npm run build

# 启动生产服务器
npm run start
```

### 部署平台

推荐的部署平台：

- **Vercel** (推荐)
- **Netlify**
- **GitHub Pages**
- **自托管服务器**

## 🛠️ 开发工具

### 可用脚本

```bash
# 开发
npm run dev          # 启动开发服务器
npm run build        # 构建生产版本
npm run start        # 启动生产服务器

# 代码质量
npm run lint         # 代码检查
npm run type-check   # 类型检查

# 工具
npm run verify-config    # 配置验证
npx homepage-update      # 框架更新
```

### 配置工具

```bash
# 验证配置文件
npm run verify-config

# 检查类型错误
npm run type-check

# 代码格式检查
npm run lint
```

## 🐛 故障排除

### 常见问题

#### 安装失败

```bash
# 清除缓存
npm cache clean --force

# 删除 node_modules 重新安装
rm -rf node_modules package-lock.json
npm install
```

#### 构建错误

```bash
# 检查配置文件
npm run verify-config

# 检查类型错误
npm run type-check

# 清除 Next.js 缓存
rm -rf .next
npm run build
```

#### 更新冲突

如果更新时出现冲突：

1. 检查备份文件
2. 手动合并配置
3. 运行验证工具
4. 重新构建项目

### 获取帮助

- 📖 [完整文档](https://github.com/penjc/homepage#readme)
- 🐛 [问题反馈](https://github.com/penjc/homepage/issues)
- 💬 [讨论区](https://github.com/penjc/homepage/discussions)

## 📈 最佳实践

### 版本管理

1. **定期更新**：建议每月检查一次更新
2. **渐进更新**：不要跳过太多版本
3. **备份重要文件**：更新前总是备份
4. **测试更新**：更新后进行全面测试

### 内容管理

1. **版本控制**：使用 Git 管理您的内容
2. **备份策略**：定期备份重要文件
3. **内容组织**：合理组织博客和随笔内容

### 配置优化

1. **SEO 设置**：完善 SEO 相关配置
2. **性能优化**：合理配置图片和资源
3. **社交媒体**：设置完整的社交媒体链接

---

💡 **提示**：Modern Homepage 通过 NPM 包管理让您可以轻松创建和维护个人主页，同时保护您的内容不被意外覆盖。 