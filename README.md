# Monorepo Demo Project

这是一个使用 pnpm workspace 搭建的 monorepo 演示项目。

## 项目结构

```
.
├── packages/          # 子包目录
│   └── vant/         # vant 包
│   └── vitepress/    # VitePress 相关包（计划中）
├── docs/             # 文档目录（计划中）
├── package.json      # 工作空间配置
└── pnpm-workspace.yaml   # pnpm 工作空间配置
```

## 技术栈

- 包管理器：pnpm (>= 10.12.1)
- 代码规范：
  - ESLint：代码质量检查
  - Prettier：代码格式化
  - Husky：Git hooks 管理
  - Commitlint：提交信息规范检查

## 开发计划

- [x] 基础 monorepo 结构搭建
- [x] 代码规范工具链配置
- [ ] VitePress 文档站点
- [ ] Vant 组件库开发

## 开发指南

### 环境要求

- Node.js
- pnpm >= 10.12.1

### 安装依赖

```bash
pnpm install
```

### 开发命令

```bash
# 开发模式
pnpm dev

# 构建
pnpm build

# 构建站点
pnpm build:site

# 代码检查
pnpm lint
```

### Git 提交规范

本项目使用严格的提交信息规范，基于 [@commitlint/config-conventional](https://github.com/conventional-changelog/commitlint/tree/master/@commitlint/config-conventional)。

#### 提交信息格式

```
type(scope?): subject

[body]

[footer]
```

#### 提交类型（type）

- `feat`: 新增功能
- `fix`: Bug 修复
- `docs`: 文档更新
- `style`: 不影响程序逻辑的代码修改(修改空白字符，格式缩进，补全缺失的分号等)
- `refactor`: 重构代码(既没有新增功能，也没有修复 bug)
- `perf`: 性能、体验优化
- `test`: 新增测试用例或是更新现有测试
- `build`: 修改项目构建系统(例如 gulp，webpack，rollup 的配置等)的提交
- `workflow`: 修改项目继续集成流程(例如 Travis，Jenkins，GitLab CI，Circle等)的提交
- `chore`: 其他类型，比如构建流程、依赖管理
- `revert`: 回滚某个更早之前的提交
- `version`: 改变 package.json 版本
- `release`: 发布新版本

#### 规则说明

- header 部分不能超过 108 个字符
- subject 和 type 不能为空
- body 前必须有空行
- footer 前建议有空行

#### 示例

```bash
# 新功能
feat(user): add user login feature

# Bug修复
fix(auth): correct the token validation logic

# 文档更新
docs: update API documentation

# 性能优化
perf(rendering): improve list rendering performance
```

### 工作空间结构

项目使用 pnpm workspace 管理多个包：

- `packages/*`: 主要功能包
- `packages/vitepress/*`: VitePress 相关包（计划中）
- `docs/*`: 文档目录（计划中）

## 许可证

ISC