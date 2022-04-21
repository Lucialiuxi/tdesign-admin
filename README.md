
### 项目简介

该项目是基于TDesign React Starter魔改， [TDesign React Starter](https://tdesign.tencent.com/starter/docs/react/get-started)是一个基于 [tdesign-react](https://tdesign.tencent.com/react/overview)，使用 `React`、`Vite2`开发，可进行个性化主题配置.


### 特性

- 内置多种常用的中后台页面
- 完善的目录结构
- 完善的代码规范配置
- 支持暗黑模式
- 自定义主题颜色
- 多种空间布局
- 内置 Mock 数据方案

### 开发
环境要求:  node版本>=12.2.0

```bash

## 安装依赖
npm install

## 启动项目
npm run dev

## mock方式启动项目
npm run dev:mock
```

### 构建

```bash
## 构建正式环境
npm run build

## 构建测试环境
npm run build:test
```

### 其他

```bash
## 预览构建产物
npm run preview

## 代码格式检查
npm run lint

## 代码格式检查与自动修复
npm run lint:fix

```

### 分支说明
1. **开发阶段**： 
    - 分支名：姓名-需求描述-创建分支日期 feature/Lucia-create-project-description-20220406
    - 操作：一般情况下以master为开发的基准分支拉取代码创建需求开发分支 

2. **测试阶段**：
    - 分支名：**dev**
    - 操作：从需求分支把代码合并到dev测试分支，dev关联测试环境

3. **回归阶段**：
    - 分支名： **release**
    - 操作：需求测试通过后，把代码从需求分支合并到release分支，release关联测试环境，在测试环境回归测试

4. **上线阶段**：
    - 分支： **master**
    - 操作：
        - 回归测试通过后，合并到master分支准备上线包;
        - 完成上线以后，打上版本tag做标记;
        - 删除已经上线了的开发需求分支

### 项目结构
```
├── README.md                         # 说明文档
├── commitlint.config.js              # commintlint 规范
├── index.html                        # 主 html 文件
├── jsx.d.ts
├── mock                              # mock 目录
│     └── index.ts
├── node_modules                      # 项目依赖
├── package-lock.json
├── package.json
├── public
│     └── favicon.ico
├── src                               # 页面代码
├── tsconfig.json
└── vite.config.js                    # vite 配置文件
```

### 页面代码结构
```
src
├── assets                            # 静态资源
├── components                        # 公共组件
├── config                            # 配置层
│     ├── global.ts                      # 全局常量配置
│     ├── color.ts                       # 主题色彩配置
│     ├── host.ts                       # 接口host配置
│
├── layouts                            # 布局层
│
├── modules                            # redux 数据层
│     ├── index.ts
│     └── global
│           └── index.ts
│
├── pages                              # 页面层
│     ├── Board                           # 一个页面组件
│     │     ├── index.module.less             # 样式文件
│     │     └── index.tsx                     # 页面入口文件
│     └── ...
│ 
├── router                            # 路由配置
│ 
├── services                          # API
│ 
├── styles                            # 公共样式
│     └── index.less
└── utils                                 # 工具层
      └── request.ts                        # 请求工具

```
