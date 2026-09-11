# sky-takeout-admin

外卖平台后台管理系统的前端应用，对接管理端接口，覆盖员工、分类、菜品、套餐、订单与营业数据统计。

## 技术栈

Vue 2.6 · TypeScript · Vue CLI 3 · Element UI · Vuex · Vue Router · ECharts · Axios

## 功能模块

| 页面 | 目录 | 说明 |
|---|---|---|
| 登录 | `src/views/login` | 账号密码登录 |
| 工作台 | `src/views/dashboard` | 今日运营数据概览 |
| 数据统计 | `src/views/statistics` | 营业额、订单量、用户量趋势图表 |
| 员工管理 | `src/views/employee` | 员工增删改查、启用/禁用 |
| 分类管理 | `src/views/category` | 菜品分类与套餐分类 |
| 菜品管理 | `src/views/dish` | 菜品维护、起售/停售、图片上传 |
| 套餐管理 | `src/views/setmeal` | 套餐组合与维护 |
| 订单管理 | `src/views/orderDetails` | 订单查询与状态流转 |
| 分类图表 | `src/views/chart` | 数据可视化 |

## 目录结构

```
├── public/            静态资源
├── src/
│   ├── api/           接口封装
│   ├── components/    通用组件（图表、上传、分页等）
│   ├── layout/        页面框架布局
│   ├── store/         Vuex 状态管理
│   ├── styles/        全局样式
│   ├── utils/         axios 封装、通用工具
│   └── views/         业务页面
└── tests/             单元测试与 E2E 测试
```

## 环境变量

后端地址在 `.env.development` / `.env.production` 中配置：

```
VUE_APP_URL = 'http://localhost:8080/admin'
```

## 运行

```bash
npm install
npm run serve       # 开发模式
npm run build       # 生产构建
npm run build:uat   # UAT 构建
npm run lint        # 代码检查
npm run test:unit   # 单元测试
```

## 说明

界面框架基于开源项目 [vue-typescript-admin-template](https://github.com/Armour/vue-typescript-admin-template)（MIT License，版权声明见仓库根目录 `LICENSE`），业务页面与接口对接在此基础上开发。
