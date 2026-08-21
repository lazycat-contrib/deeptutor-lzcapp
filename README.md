# DeepTutor - LazyCat 应用包

DeepTutor 是一个智能体原生个性化辅导工作空间，将辅导、问题解决、测验生成、研究和精通练习连接在一个可扩展的系统中。

## 版本

- 当前版本: 1.5.15
- 上游镜像: `ghcr.io/hkuds/deeptutor:1.5.15`

## 发布到喵喵商店

### 前提条件

1. 配置 GitHub Secrets:
   - `APPSTORE_URL` - 喵喵商店 API 地址
   - `APPSTORE_TOKEN` - 喵喵商店 API Token
   - `APP_ID` - 应用 ID（可选）
   - `PRIVATE_STORE_GROUP_CODES` - 私有商店分组码（可选）

2. 确保 `lzc-cli` 已安装:
   ```bash
   npm install -g @lazycatcloud/lzc-cli
   ```

### 手动构建

```bash
lzc-cli project release -o dist/community.lazycat.app.deeptutor.lpk
```

### 自动发布

GitHub Actions 每天早上自动检查上游镜像更新，有新版本时自动构建并发布到喵喵商店。

## 项目结构

```
.
├── package.yml           # 包元数据
├── lzc-manifest.yml      # 运行配置
├── lzc-build.yml         # 构建配置
├── lzc-deploy-params.yml # 部署参数
├── icon.png              # 应用图标
├── .github/
│   ├── lazycat-action.yml       # LazyCat Action 配置
│   └── workflows/lazycat.yml    # GitHub 工作流
└── README.md
```

## 许可证

MIT - 上游项目: [HKUDS/DeepTutor](https://github.com/HKUDS/DeepTutor)