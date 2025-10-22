# 🤝 贡献指南

感谢你对 Homepage 项目的关注！我们欢迎所有形式的贡献，无论是报告bug、提出功能建议、改进文档还是提交代码。

## 📋 目录

- [行为准则](#行为准则)
- [如何贡献](#如何贡献)
- [开发环境设置](#开发环境设置)
- [提交指南](#提交指南)
- [代码规范](#代码规范)
- [测试](#测试)
- [文档](#文档)

## 🤝 行为准则

参与此项目即表示你同意遵守我们的[行为准则](CODE_OF_CONDUCT.md)。请确保在所有互动中保持尊重和包容。

## 🚀 如何贡献

### 报告Bug

如果你发现了bug，请：

1. 检查[现有issues](https://github.com/Ducr/homepage/issues)确保bug未被报告
2. 使用[Bug报告模板](.github/ISSUE_TEMPLATE/bug_report.md)创建新issue
3. 提供详细的复现步骤和环境信息

### 功能建议

如果你有新功能的想法：

1. 检查[现有issues](https://github.com/Ducr/homepage/issues)确保功能未被建议
2. 使用[功能请求模板](.github/ISSUE_TEMPLATE/feature_request.md)创建新issue
3. 详细描述功能的用途和实现方式

### 提交代码

1. Fork 这个仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 进行你的更改
4. 确保代码通过所有测试
5. 提交你的更改 (`git commit -m 'Add some AmazingFeature'`)
6. 推送到分支 (`git push origin feature/AmazingFeature`)
7. 打开一个 Pull Request

## 🛠️ 开发环境设置

### 前置要求

- Node.js >= 16.0.0
- npm >= 8.0.0

### 安装步骤

```bash
# 克隆仓库
git clone https://github.com/Ducr/homepage.git
cd homepage

# 安装依赖
npm install

# 复制配置文件
cp site.config.example.ts site.config.ts

# 启动开发服务器
npm run dev
```

### 开发命令

```bash
npm run dev          # 启动开发服务器
npm run build        # 构建生产版本
npm run start        # 启动生产服务器
npm run lint         # 运行ESLint
npm run lint:fix     # 自动修复ESLint错误
npm run type-check   # TypeScript类型检查
```

## 📝 提交指南

### 提交信息格式

我们使用[约定式提交](https://www.conventionalcommits.org/)格式：

```
<类型>[可选的作用域]: <描述>

[可选的正文]

[可选的脚注]
```

### 提交类型

- `feat`: 新功能
- `fix`: bug修复
- `docs`: 文档更新
- `style`: 代码格式化
- `refactor`: 代码重构
- `perf`: 性能优化
- `test`: 测试相关
- `build`: 构建相关
- `ci`: CI相关
- `chore`: 其他杂项

### 示例

```bash
git commit -m "feat: add dark mode support"
git commit -m "fix: resolve mobile navigation issue"
git commit -m "docs: update installation guide"
```

## 🎨 代码规范

### TypeScript/JavaScript

- 使用 TypeScript 进行类型安全
- 遵循 ESLint 配置
- 使用 Prettier 进行代码格式化
- 优先使用函数式组件和 Hooks

### 样式

- 使用 Tailwind CSS 进行样式编写
- 遵循移动优先的响应式设计
- 保持一致的设计系统

### 文件命名

- 组件文件使用 PascalCase: `MyComponent.tsx`
- 工具函数使用 camelCase: `myUtility.ts`
- 页面文件使用 kebab-case: `my-page.tsx`

## 📚 文档

### 更新文档

- 为新功能更新 README.md
- 添加或更新 JSDoc 注释
- 更新类型定义
- 提供使用示例

### 文档规范

- 使用清晰简洁的语言
- 提供代码示例
- 包含截图（如适用）
- 保持文档与代码同步

## 🔍 代码审查

### 审查清单

- [ ] 代码符合项目规范
- [ ] 包含适当的测试
- [ ] 文档已更新
- [ ] 没有破坏性变更（或已明确标注）
- [ ] 性能影响已考虑
- [ ] 安全性已考虑

### 审查流程

1. 自动化检查必须通过
2. 至少一个维护者审查
3. 解决所有审查意见
4. 合并到主分支

## 🏷️ 版本发布

我们使用[语义化版本](https://semver.org/)：

- `MAJOR`: 不兼容的API变更
- `MINOR`: 向后兼容的功能新增
- `PATCH`: 向后兼容的bug修复

## 📞 获取帮助

如果你需要帮助：

- 查看[文档](docs/)
- 搜索[现有issues](https://github.com/Ducr/homepage/issues)
- 创建[问题issue](.github/ISSUE_TEMPLATE/question.md)
- 联系维护者

## 🙏 致谢

感谢所有贡献者的努力！你们的贡献让这个项目变得更好。

---

再次感谢你的贡献！🎉 