# TokenChain - Cosmos SDK区块链项目

一个完整的基于Cosmos SDK的区块链应用，包含代币铸造、用户管理、转账功能和区块浏览器，配有现代化的React前端界面。

## 🌟 项目特性

### 区块链功能
- ✅ **代币铸造**: 授权用户可以铸造新代币
- ✅ **代币转账**: 支持钱包间代币转移
- ✅ **用户管理**: 链上用户注册和信息管理
- ✅ **挖矿奖励**: 验证者奖励分配机制
- ✅ **区块浏览器**: 查看区块、交易和网络状态

### 前端功能
- 🎨 **现代化UI**: 基于Material-UI的响应式设计
- 🔐 **钱包集成**: 支持助记词导入/生成和Keplr钱包
- 📊 **实时数据**: 区块链状态实时更新
- 🔍 **搜索功能**: 支持区块、交易和地址搜索
- 📱 **移动端适配**: 完全响应式设计

## 🏗️ 技术栈

### 区块链
- **Ignite CLI v28.11.0**: 快速构建Cosmos SDK应用
- **Cosmos SDK**: 模块化区块链框架
- **CometBFT**: 拜占庭容错共识引擎
- **gRPC & REST API**: 多种接口支持

### 前端
- **React 18**: 现代化前端框架
- **TypeScript**: 类型安全的JavaScript
- **Material-UI**: Google Material Design组件库
- **CosmJS**: Cosmos生态JavaScript/TypeScript库
- **React Query**: 数据获取和状态管理
- **React Router**: 单页应用路由

## 🚀 快速开始

### 前置要求

```bash
# 安装依赖
- Node.js 18+
- Go 1.21+
- Git
```

### 1. 克隆项目

```bash
# 克隆区块链仓库
git clone https://github.com/hinatayuan/tokenchain.git
cd tokenchain

# 克隆前端仓库
git clone https://github.com/hinatayuan/tokenchain-frontend.git
cd tokenchain-frontend
```

### 2. 启动区块链

```bash
cd tokenchain

# 安装Ignite CLI
curl https://get.ignite.com/cli@v28.11.0! | bash

# 启动区块链
ignite chain serve

# 区块链将在以下端点运行:
# - RPC: http://localhost:26657
# - REST: http://localhost:1317
# - gRPC: localhost:9090
# - 水龙头: http://localhost:4500
```

### 3. 启动前端

```bash
cd tokenchain-frontend

# 安装依赖
npm install

# 启动开发服务器
npm start

# 前端将在 http://localhost:3000 运行
```

## 📖 使用指南

### 钱包连接
1. 点击"连接钱包"按钮
2. 选择导入现有钱包或创建新钱包
3. 输入助记词或生成新的助记词
4. 连接成功后即可进行交易

### 代币操作
- **查看余额**: 在仪表板或钱包页面查看
- **转账代币**: 进入转账页面，输入接收地址和金额
- **铸造代币**: 需要铸造权限，在铸造页面操作

### 用户管理
- **创建用户**: 在用户页面注册链上身份
- **查看用户**: 浏览所有注册用户
- **更新信息**: 修改用户资料

### 区块浏览器
- **查看区块**: 浏览最新区块信息
- **搜索功能**: 通过区块高度或交易哈希搜索
- **验证者信息**: 查看网络验证者状态

## 🔧 配置说明

### 环境变量 (.env)

```env
REACT_APP_CHAIN_ID=tokenchain-1
REACT_APP_CHAIN_NAME=TokenChain
REACT_APP_RPC_URL=http://localhost:26657
REACT_APP_REST_URL=http://localhost:1317
REACT_APP_FAUCET_URL=http://localhost:4500
REACT_APP_DENOM=token
REACT_APP_PREFIX=token
```

### 链配置 (config.yml)

```yaml
version: 1
accounts:
  - name: alice
    coins: ["20000token", "200000000stake"]
  - name: bob
    coins: ["10000token", "100000000stake"]
client:
  openapi:
    path: docs/static/openapi.yml
faucet:
  name: alice
  coins: ["5token", "100000stake"]
genesis:
  chain_id: tokenchain-1
validators:
  - name: alice
    bonded: 100000000stake
```

## 📁 项目结构

### 区块链项目
```
tokenchain/
├── app/                 # 应用程序配置
├── cmd/                 # CLI命令
├── docs/                # 文档和OpenAPI规范
├── proto/               # Protocol Buffer定义
├── x/                   # 自定义模块
│   ├── mint/           # 代币铸造模块
│   └── user/           # 用户管理模块
├── config.yml          # 链配置
└── readme.md
```

### 前端项目
```
tokenchain-frontend/
├── public/              # 静态资源
├── src/
│   ├── components/      # 可复用组件
│   ├── pages/          # 页面组件
│   ├── contexts/       # React Context
│   ├── services/       # API服务
│   ├── hooks/          # 自定义Hooks
│   ├── types/          # TypeScript类型
│   └── utils/          # 工具函数
├── package.json
└── README.md
```

## 🤝 贡献指南

1. Fork 项目
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开 Pull Request

## 📄 许可证

此项目使用 MIT 许可证。详情请查看 [LICENSE](LICENSE) 文件。

## 🔗 相关链接

- [Cosmos SDK 文档](https://docs.cosmos.network/)
- [Ignite CLI 文档](https://docs.ignite.com/)
- [CosmJS 文档](https://cosmos.github.io/cosmjs/)
- [Material-UI 文档](https://mui.com/)

## 📞 联系方式

如有问题或建议，请通过以下方式联系：

- 创建 [Issue](https://github.com/hinatayuan/tokenchain/issues)
- 发送邮件至：your-email@example.com

## 🙏 致谢

感谢 Cosmos 生态系统提供的优秀工具和文档，使得构建这个项目成为可能。

---

⭐ 如果这个项目对您有帮助，请给它一个星标！