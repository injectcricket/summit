# TechRef Navigator

TechRef Navigator 是一个面向开发者与架构师的技术资源导航与外链聚合工具。项目定位于系统化收集、分类、索引高质量技术文章、博客笔记与工程实践内容，帮助技术团队快速检索特定主题的深度解析文章，降低信息分散带来的检索成本。

本项目不对文章内容进行二次加工，仅提供结构化索引与本地快速启动环境，适用于希望建立内部技术知识库、搭建技术文档门户或维护学习资源清单的团队与个人。通过本导航系统，用户可按分类浏览、按关键词检索、按热度排序，快速定位目标资源。

## 功能概览

- **分类浏览体系** 按技术领域、难度等级、文章类型对资源进行多维度分类，支持快速过滤。
- **全文检索支持** 基于标题与摘要字段提供轻量级关键词检索，不依赖外部搜索引擎。
- **本地离线启动** 提供完整的克隆、安装、运行流程，可在内网或本地环境独立部署。
- **资源状态监控** 周期性检测链接可访问性，对失效链接进行标记与告警。
- **访问热度统计** 记录用户点击行为，生成热门文章排行，辅助团队发现高价值内容。
- **标签系统** 支持为每条记录打上自定义标签，便于按项目、主题或阶段进行分组管理。
- **导入导出接口** 提供 JSON 与 CSV 格式的批量导入导出功能，方便与其他知识管理工具对接。
- **响应式界面** 适配桌面与移动端浏览，确保在不同设备上的阅读体验一致。

## 应用场景

**团队内部技术文档门户**  
技术团队可将本导航部署为内部文档入口，聚合组内产出的各类技术博客、故障复盘报告、设计文档，使新成员能快速了解团队知识沉淀。

**个人学习路线管理**  
开发者可将日常阅读的技术文章、教程视频、开源项目文档统一收录，按学习阶段或技能树组织，形成个人专属学习资源库。

**技术社区内容精选**  
社区运营者或开源项目维护者可使用本导航整理社区优质投稿，按版本或主题分类，方便社区成员查阅历史精华内容。

**离线知识备份与检索**  
在网络受限或需要长期保存技术资料的场景下，本导航可作为本地索引前端，配合离线存储机制，确保核心文档在无外网环境时依然可被检索。

## 快速开始

以下命令可在 Ubuntu 22.04 / macOS 13 及以上环境中完成项目部署。

```bash
# 克隆代码仓库
git clone https://github.com/techref-navigator/techref-navigator.git
cd techref-navigator

# 安装依赖（使用 npm）
npm install

# 启动开发服务器
npm run dev
```

生产环境构建与启动命令：

```bash
npm run build
npm start
```

## 安装要求

| 依赖组件 | 必需版本 | 说明 |
|---|---|---|
| Node.js | v18.17.0 或更高 | 运行时环境，建议使用 LTS 版本 |
| npm | v9.0.0 或更高 | 包管理器，用于安装项目依赖 |
| SQLite3 | 系统自带或 v3.35.0+ | 默认本地数据库引擎，无需额外配置 |
| 操作系统 | Linux / macOS / Windows WSL2 | 支持主流操作系统，Windows 推荐使用 WSL2 环境 |
| 浏览器 | Chrome 90+ / Firefox 88+ / Edge 90+ | 前端界面浏览器兼容性要求 |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|---|---|---|
| 用户手册 | /docs/user-guide/ | 如何浏览分类、检索文章、查看热度排行、导入导出数据 |
| 部署指南 | /docs/deployment/ | 如何在不同操作系统上部署生产环境，配置反向代理与数据库 |
| 开发指南 | /docs/development/ | 项目架构说明、前端组件设计、后端 API 接口规范、如何新增功能 |
| 维护手册 | /docs/maintenance/ | 如何更新资源列表、检查链接有效性、备份与恢复数据库 |

## 资源列表

本批次收录资源共计 250 条，涵盖技术博客、工程实践笔记、架构设计讨论等类别。所有链接来自第三方站点，按收录时间顺序排列。

### 通用技术文章

http://www.blog.cmcvrr.cn/Article/details/6180.sHtML

http://www.blog.cmcvrr.cn/Article/details/91037.sHtML

http://www.blog.cmcvrr.cn/Article/details/6188988.sHtML

http://www.blog.cmcvrr.cn/Article/details/26987.sHtML

http://www.blog.cmcvrr.cn/Article/details/8910.sHtML

http://www.blog.cmcvrr.cn/Article/details/7032.sHtML

http://www.blog.cmcvrr.cn/Article/details/745004.sHtML

http://www.blog.cmcvrr.cn/Article/details/31693.sHtML

http://www.blog.cmcvrr.cn/Article/details/4640.sHtML

http://www.blog.cmcvrr.cn/Article/details/0547.sHtML

http://www.blog.cmcvrr.cn/Article/details/72338.sHtML

http://www.blog.cmcvrr.cn/Article/details/4336.sHtML

http://www.blog.cmcvrr.cn/Article/details/9208186.sHtML

http://www.blog.cmcvrr.cn/Article/details/39802.sHtML

http://www.blog.cmcvrr.cn/Article/details/31558.sHtML

http://www.blog.cmcvrr.cn/Article/details/0003583.sHtML

http://www.blog.cmcvrr.cn/Article/details/593020.sHtML

http://www.blog.cmcvrr.cn/Article/details/377348.sHtML

http://www.blog.cmcvrr.cn/Article/details/80939.sHtML

http://www.blog.cmcvrr.cn/Article/details/4859797.sHtML

http://www.blog.cmcvrr.cn/Article/details/22439.sHtML

http://www.blog.cmcvrr.cn/Article/details/00629.sHtML

http://www.blog.cmcvrr.cn/Article/details/6614.sHtML

http://www.blog.cmcvrr.cn/Article/details/7560617.sHtML

http://www.blog.cmcvrr.cn/Article/details/786164.sHtML

http://www.blog.cmcvrr.cn/Article/details/3479.sHtML

http://www.blog.cmcvrr.cn/Article/details/68059.sHtML

http://www.blog.cmcvrr.cn/Article/details/319948.sHtML

http://www.blog.cmcvrr.cn/Article/details/2636.sHtML

http://www.blog.cmcvrr.cn/Article/details/8659144.sHtML

http://www.blog.cmcvrr.cn/Article/details/83669.sHtML

http://www.blog.cmcvrr.cn/Article/details/28403.sHtML

http://www.blog.cmcvrr.cn/Article/details/98228.sHtML

http://www.blog.cmcvrr.cn/Article/details/51876.sHtML

http://www.blog.cmcvrr.cn/Article/details/3450.sHtML

http://www.blog.cmcvrr.cn/Article/details/21237.sHtML

http://www.blog.cmcvrr.cn/Article/details/72358.sHtML

http://www.blog.cmcvrr.cn/Article/details/1463123.sHtML

http://www.blog.cmcvrr.cn/Article/details/721501.sHtML

http://www.blog.cmcvrr.cn/Article/details/81923.sHtML

http://www.blog.cmcvrr.cn/Article/details/7739.sHtML

http://www.blog.cmcvrr.cn/Article/details/8622659.sHtML

http://www.blog.cmcvrr.cn/Article/details/2481.sHtML

http://www.blog.cmcvrr.cn/Article/details/7879.sHtML

http://www.blog.cmcvrr.cn/Article/details/0900.sHtML

http://www.blog.cmcvrr.cn/Article/details/4199.sHtML

http://www.blog.cmcvrr.cn/Article/details/3455799.sHtML

http://www.blog.cmcvrr.cn/Article/details/6398673.sHtML

http://www.blog.cmcvrr.cn/Article/details/5588046.sHtML

http://www.blog.cmcvrr.cn/Article/details/3715.sHtML

http://www.blog.cmcvrr.cn/Article/details/4278.sHtML

http://www.blog.cmcvrr.cn/Article/details/2011.sHtML

http://www.blog.cmcvrr.cn/Article/details/44309.sHtML

http://www.blog.cmcvrr.cn/Article/details/8256.sHtML

http://www.blog.cmcvrr.cn/Article/details/2649496.sHtML

http://www.blog.cmcvrr.cn/Article/details/906216.sHtML

http://www.blog.cmcvrr.cn/Article/details/9054570.sHtML

http://www.blog.cmcvrr.cn/Article/details/40447.sHtML

http://www.blog.cmcvrr.cn/Article/details/12470.sHtML

http://www.blog.cmcvrr.cn/Article/details/0035.sHtML

http://www.blog.cmcvrr.cn/Article/details/620669.sHtML

http://www.blog.cmcvrr.cn/Article/details/468219.sHtML

http://www.blog.cmcvrr.cn/Article/details/14290.sHtML

http://www.blog.cmcvrr.cn/Article/details/0991186.sHtML

http://www.blog.cmcvrr.cn/Article/details/59906.sHtML

http://www.blog.cmcvrr.cn/Article/details/9945.sHtML

http://www.blog.cmcvrr.cn/Article/details/626254.sHtML

http://www.blog.cmcvrr.cn/Article/details/2593613.sHtML

http://www.blog.cmcvrr.cn/Article/details/875352.sHtML

http://www.blog.cmcvrr.cn/Article/details/89149.sHtML

http://www.blog.cmcvrr.cn/Article/details/1464935.sHtML

http://www.blog.cmcvrr.cn/Article/details/66633.sHtML

http://www.blog.cmcvrr.cn/Article/details/049969.sHtML

http://www.blog.cmcvrr.cn/Article/details/4610.sHtML

http://www.blog.cmcvrr.cn/Article/details/34761.sHtML

http://www.blog.cmcvrr.cn/Article/details/3561.sHtML

http://www.blog.cmcvrr.cn/Article/details/8038844.sHtML

http://www.blog.cmcvrr.cn/Article/details/912824.sHtML

http://www.blog.cmcvrr.cn/Article/details/407187.sHtML

http://www.blog.cmcvrr.cn/Article/details/97601.sHtML

http://www.blog.cmcvrr.cn/Article/details/972284.sHtML

http://www.blog.cmcvrr.cn/Article/details/050459.sHtML

http://www.blog.cmcvrr.cn/Article/details/7770946.sHtML

http://www.blog.cmcvrr.cn/Article/details/7060.sHtML

http://www.blog.cmcvrr.cn/Article/details/4412.sHtML

http://www.blog.cmcvrr.cn/Article/details/38049.sHtML

http://www.blog.cmcvrr.cn/Article/details/1289.sHtML

http://www.blog.cmcvrr.cn/Article/details/8836.sHtML

http://www.blog.cmcvrr.cn/Article/details/3845456.sHtML

http://www.blog.cmcvrr.cn/Article/details/814074.sHtML

http://www.blog.cmcvrr.cn/Article/details/351713.sHtML

http://www.blog.cmcvrr.cn/Article/details/98475.sHtML

http://www.blog.cmcvrr.cn/Article/details/4309718.sHtML

http://www.blog.cmcvrr.cn/Article/details/9873877.sHtML

http://www.blog.cmcvrr.cn/Article/details/4770.sHtML

http://www.blog.cmcvrr.cn/Article/details/619950.sHtML

http://www.blog.cmcvrr.cn/Article/details/421861.sHtML

http://www.blog.cmcvrr.cn/Article/details/57616.sHtML

http://www.blog.cmcvrr.cn/Article/details/00642.sHtML

http://www.blog.cmcvrr.cn/Article/details/0155907.sHtML

http://www.blog.cmcvrr.cn/Article/details/95487.sHtML

http://www.blog.cmcvrr.cn/Article/details/0577.sHtML

http://www.blog.cmcvrr.cn/Article/details/0935959.sHtML

http://www.blog.cmcvrr.cn/Article/details/2019.sHtML

http://www.blog.cmcvrr.cn/Article/details/8106019.sHtML

http://www.blog.cmcvrr.cn/Article/details/44359.sHtML

http://www.blog.cmcvrr.cn/Article/details/6759.sHtML

http://www.blog.cmcvrr.cn/Article/details/5766.sHtML

http://www.blog.cmcvrr.cn/Article/details/134557.sHtML

http://www.blog.cmcvrr.cn/Article/details/309713.sHtML

http://www.blog.cmcvrr.cn/Article/details/5507333.sHtML

http://www.blog.cmcvrr.cn/Article/details/0811.sHtML

http://www.blog.cmcvrr.cn/Article/details/930863.sHtML

http://www.blog.cmcvrr.cn/Article/details/46351.sHtML

http://www.blog.cmcvrr.cn/Article/details/621430.sHtML

http://www.blog.cmcvrr.cn/Article/details/007222.sHtML

http://www.blog.cmcvrr.cn/Article/details/02532.sHtML

http://www.blog.cmcvrr.cn/Article/details/0363753.sHtML

http://www.blog.cmcvrr.cn/Article/details/64493.sHtML

http://www.blog.cmcvrr.cn/Article/details/76556.sHtML

http://www.blog.cmcvrr.cn/Article/details/83461.sHtML

http://www.blog.cmcvrr.cn/Article/details/08024.sHtML

http://www.blog.cmcvrr.cn/Article/details/8908158.sHtML

http://www.blog.cmcvrr.cn/Article/details/9564644.sHtML

http://www.blog.cmcvrr.cn/Article/details/776760.sHtML

http://www.blog.cmcvrr.cn/Article/details/390720.sHtML

http://www.blog.cmcvrr.cn/Article/details/78003.sHtML

http://www.blog.cmcvrr.cn/Article/details/1323.sHtML

http://www.blog.cmcvrr.cn/Article/details/93311.sHtML

http://www.blog.cmcvrr.cn/Article/details/8499.sHtML

http://www.blog.cmcvrr.cn/Article/details/8247001.sHtML

http://www.blog.cmcvrr.cn/Article/details/712257.sHtML

http://www.blog.cmcvrr.cn/Article/details/87689.sHtML

http://www.blog.cmcvrr.cn/Article/details/94392.sHtML

http://www.blog.cmcvrr.cn/Article/details/26157.sHtML

http://www.blog.cmcvrr.cn/Article/details/24842.sHtML

http://www.blog.cmcvrr.cn/Article/details/531896.sHtML

http://www.blog.cmcvrr.cn/Article/details/7572.sHtML

http://www.blog.cmcvrr.cn/Article/details/13759.sHtML

http://www.blog.cmcvrr.cn/Article/details/705209.sHtML

http://www.blog.cmcvrr.cn/Article/details/5518.sHtML

http://www.blog.cmcvrr.cn/Article/details/060451.sHtML

http://www.blog.cmcvrr.cn/Article/details/066501.sHtML

http://www.blog.cmcvrr.cn/Article/details/561270.sHtML

http://www.blog.cmcvrr.cn/Article/details/9380.sHtML

http://www.blog.cmcvrr.cn/Article/details/0880.sHtML

http://www.blog.cmcvrr.cn/Article/details/082253.sHtML

http://www.blog.cmcvrr.cn/Article/details/101771.sHtML

http://www.blog.cmcvrr.cn/Article/details/269326.sHtML

http://www.blog.cmcvrr.cn/Article/details/45390.sHtML

http://www.blog.cmcvrr.cn/Article/details/6136484.sHtML

http://www.blog.cmcvrr.cn/Article/details/6711533.sHtML

http://www.blog.cmcvrr.cn/Article/details/69238.sHtML

http://www.blog.cmcvrr.cn/Article/details/669872.sHtML

http://www.blog.cmcvrr.cn/Article/details/01567.sHtML

http://www.blog.cmcvrr.cn/Article/details/8886.sHtML

http://www.blog.cmcvrr.cn/Article/details/6525080.sHtML

http://www.blog.cmcvrr.cn/Article/details/989339.sHtML

http://www.blog.cmcvrr.cn/Article/details/1511.sHtML

http://www.blog.cmcvrr.cn/Article/details/2526319.sHtML

http://www.blog.cmcvrr.cn/Article/details/30511.sHtML

http://www.blog.cmcvrr.cn/Article/details/44112.sHtML

http://www.blog.cmcvrr.cn/Article/details/21656.sHtML

http://www.blog.cmcvrr.cn/Article/details/8873777.sHtML

http://www.blog.cmcvrr.cn/Article/details/8995.sHtML

http://www.blog.cmcvrr.cn/Article/details/6697.sHtML

http://www.blog.cmcvrr.cn/Article/details/9552.sHtML

http://www.blog.cmcvrr.cn/Article/details/6384135.sHtML

http://www.blog.cmcvrr.cn/Article/details/1896581.sHtML

http://www.blog.cmcvrr.cn/Article/details/5301.sHtML

http://www.blog.cmcvrr.cn/Article/details/1720974.sHtML

http://www.blog.cmcvrr.cn/Article/details/87311.sHtML

http://www.blog.cmcvrr.cn/Article/details/2973518.sHtML

http://www.blog.cmcvrr.cn/Article/details/14262.sHtML

http://www.blog.cmcvrr.cn/Article/details/71826.sHtML

http://www.blog.cmcvrr.cn/Article/details/8805.sHtML

http://www.blog.cmcvrr.cn/Article/details/0586.sHtML

http://www.blog.cmcvrr.cn/Article/details/6647.sHtML

http://www.blog.cmcvrr.cn/Article/details/846239.sHtML

http://www.blog.cmcvrr.cn/Article/details/143286.sHtML

http://www.blog.cmcvrr.cn/Article/details/769064.sHtML

http://www.blog.cmcvrr.cn/Article/details/47619.sHtML

http://www.blog.cmcvrr.cn/Article/details/004086.sHtML

http://www.blog.cmcvrr.cn/Article/details/4627.sHtML

http://www.blog.cmcvrr.cn/Article/details/62891.sHtML

http://www.blog.cmcvrr.cn/Article/details/377538.sHtML

http://www.blog.cmcvrr.cn/Article/details/2837.sHtML

http://www.blog.cmcvrr.cn/Article/details/766927.sHtML

http://www.blog.cmcvrr.cn/Article/details/58626.sHtML

http://www.blog.cmcvrr.cn/Article/details/397438.sHtML

http://www.blog.cmcvrr.cn/Article/details/258926.sHtML

http://www.blog.cmcvrr.cn/Article/details/50076.sHtML

http://www.blog.cmcvrr.cn/Article/details/2674.sHtML

http://www.blog.cmcvrr.cn/Article/details/151987.sHtML

http://www.blog.cmcvrr.cn/Article/details/918151.sHtML

http://www.blog.cmcvrr.cn/Article/details/48553.sHtML

http://www.blog.cmcvrr.cn/Article/details/664313.sHtML

http://www.blog.cmcvrr.cn/Article/details/744144.sHtML

http://www.blog.cmcvrr.cn/Article/details/4353460.sHtML

http://www.blog.cmcvrr.cn/Article/details/1392.sHtML

http://www.blog.cmcvrr.cn/Article/details/0171.sHtML

http://www.blog.cmcvrr.cn/Article/details/2496399.sHtML

http://www.blog.cmcvrr.cn/Article/details/4839830.sHtML

http://www.blog.cmcvrr.cn/Article/details/0753268.sHtML

http://www.blog.cmcvrr.cn/Article/details/8619003.sHtML

http://www.blog.cmcvrr.cn/Article/details/0754.sHtML

http://www.blog.cmcvrr.cn/Article/details/0801325.sHtML

http://www.blog.cmcvrr.cn/Article/details/7694.sHtML

http://www.blog.cmcvrr.cn/Article/details/8102.sHtML

http://www.blog.cmcvrr.cn/Article/details/014361.sHtML

http://www.blog.cmcvrr.cn/Article/details/166015.sHtML

http://www.blog.cmcvrr.cn/Article/details/5489.sHtML

http://www.blog.cmcvrr.cn/Article/details/6510843.sHtML

http://www.blog.cmcvrr.cn/Article/details/70402.sHtML

http://www.blog.cmcvrr.cn/Article/details/800717.sHtML

http://www.blog.cmcvrr.cn/Article/details/58736.sHtML

http://www.blog.cmcvrr.cn/Article/details/840530.sHtML

http://www.blog.cmcvrr.cn/Article/details/83485.sHtML

http://www.blog.cmcvrr.cn/Article/details/103959.sHtML

http://www.blog.cmcvrr.cn/Article/details/17656.sHtML

http://www.blog.cmcvrr.cn/Article/details/8291915.sHtML

http://www.blog.cmcvrr.cn/Article/details/087225.sHtML

http://www.blog.cmcvrr.cn/Article/details/19351.sHtML

http://www.blog.cmcvrr.cn/Article/details/639866.sHtML

http://www.blog.cmcvrr.cn/Article/details/903386.sHtML

http://www.blog.cmcvrr.cn/Article/details/3847.sHtML

http://www.blog.cmcvrr.cn/Article/details/413377.sHtML

http://www.blog.cmcvrr.cn/Article/details/638902.sHtML

http://www.blog.cmcvrr.cn/Article/details/4420597.sHtML

http://www.blog.cmcvrr.cn/Article/details/9498.sHtML

http://www.blog.cmcvrr.cn/Article/details/0258.sHtML

http://www.blog.cmcvrr.cn/Article/details/65652.sHtML

http://www.blog.cmcvrr.cn/Article/details/6162.sHtML

http://www.blog.cmcvrr.cn/Article/details/638220.sHtML

http://www.blog.cmcvrr.cn/Article/details/46908.sHtML

http://www.blog.cmcvrr.cn/Article/details/488419.sHtML

http://www.blog.cmcvrr.cn/Article/details/8564.sHtML

http://www.blog.cmcvrr.cn/Article/details/565970.sHtML

http://www.blog.cmcvrr.cn/Article/details/9272361.sHtML

http://www.blog.cmcvrr.cn/Article/details/9793.sHtML

http://www.blog.cmcvrr.cn/Article/details/8480.sHtML

http://www.blog.cmcvrr.cn/Article/details/85219.sHtML

http://www.blog.cmcvrr.cn/Article/details/1805335.sHtML

http://www.blog.cmcvrr.cn/Article/details/64190.sHtML

http://www.blog.cmcvrr.cn/Article/details/3619.sHtML

http://www.blog.cmcvrr.cn/Article/details/564433.sHtML

http://www.blog.cmcvrr.cn/Article/details/0565396.sHtML

http://www.blog.cmcvrr.cn/Article/details/869825.sHtML

http://www.blog.cmcvrr.cn/Article/details/8101.sHtML

http://www.blog.cmcvrr.cn/Article/details/94156.sHtML

## 项目结构

```
techref-navigator/
├── backend/                        # 后端服务目录
│   ├── src/
│   │   ├── api/                    # RESTful API 路由定义
│   │   │   ├── articles.js         # 文章资源相关接口
│   │   │   ├── categories.js       # 分类管理接口
│   │   │   └── stats.js            # 访问统计接口
│   │   ├── core/                   # 核心业务逻辑
│   │   │   ├── crawler.js          # 链接状态检测模块
│   │   │   ├── indexer.js          # 索引构建与更新模块
│   │   │   └── validator.js        # 数据校验与清洗模块
│   │   ├── models/                 # 数据模型定义
│   │   │   ├── article.js          # 文章实体模型
│   │   │   ├── tag.js              # 标签实体模型
│   │   │   └── user.js             # 用户实体模型
│   │   └── utils/                  # 工具函数
│   │       ├── db.js               # 数据库连接与操作封装
│   │       └── logger.js           # 日志记录工具
│   ├── tests/                      # 单元测试与集成测试
│   └── package.json                # 后端依赖配置
├── frontend/                       # 前端应用目录
│   ├── public/                     # 静态资源文件
│   │   └── index.html              # 入口 HTML 文件
│   ├── src/
│   │   ├── components/             # Vue / React 组件
│   │   │   ├── ArticleList.vue     # 文章列表组件
│   │   │   ├── SearchBar.vue       # 搜索栏组件
│   │   │   └── CategoryNav.vue     # 分类导航组件
│   │   ├── pages/                  # 页面级组件
│   │   │   ├── Home.vue            # 主页
│   │   │   ├── Detail.vue          # 文章详情页
│   │   │   └── Admin.vue           # 管理后台页面
│   │   ├── store/                  # 状态管理
│   │   │   └── index.js            # Vuex / Pinia 配置
│   │   ├── styles/                 # 全局样式表
│   │   │   └── main.css
│   │   └── utils/                  # 前端工具函数
│   │       └── request.js          # HTTP 请求封装
│   ├── package.json                # 前端依赖配置
│   └── vite.config.js              # 构建工具配置
├── data/                           # 数据存储目录
│   ├── database.sqlite             # SQLite 数据库文件
│   └── seeds/                      # 初始数据种子文件
│       └── initial_articles.json   # 首批资源导入数据
├── docs/                           # 项目文档
│   ├── user-guide/
│   ├── deployment/
│   ├── development/
│   └── maintenance/
├── scripts/                        # 运维与辅助脚本
│   ├── health-check.sh             # 服务健康检查脚本
│   ├── backup-db.sh                # 数据库备份脚本
│   └── import-resources.js         # 资源批量导入脚本
├── .env.example                    # 环境变量示例文件
├── docker-compose.yml              # Docker Compose 编排文件
├── Dockerfile                      # 容器构建文件
├── LICENSE                         # MIT 许可证
└── README.md                       # 项目说明文档
```

## 贡献指南

本项目欢迎外部贡献者参与资源补充、功能改进与文档优化。请遵循以下步骤提交贡献。

1. 在 GitHub 上 Fork 本仓库，并克隆到本地开发环境中。确保本地 Node.js 版本满足安装要求。
2. 新建功能分支或修复分支，分支命名遵循 `feature/功能名称` 或 `fix/问题简述` 格式。避免在主干分支直接修改。
3. 完成代码或文档修改后，请运行测试套件确保现有功能未被破坏。若新增功能，需补充对应的单元测试或集成测试。
4. 提交 Pull Request 至主干分支，并在 PR 描述中清晰说明改动内容、关联 Issue 编号以及测试覆盖情况。提交信息采用 Conventional Commits 规范。
5. 项目维护者将在三个工作日内进行 Code Review。如有修改意见，贡献者需在五天内响应并更新代码。合并后，贡献者名称将列入项目致谢名单。

## 常见问题

**Q：部署后首次启动，前端页面无法加载资源列表，提示“数据库连接失败”，应如何排查？**

A：请按以下顺序检查。首先确认 SQLite3 已正确安装且版本不低于 3.35.0。其次检查项目根目录下的 `.env` 文件是否存在且 `DATABASE_PATH` 变量指向正确的数据库文件路径。最后确保运行用户对 `data/` 目录拥有读写权限。若使用 Docker 部署，需确认宿主机目录已正确挂载至容器内 `/app/data`。

**Q：导入外部 JSON 资源列表时，部分记录因字段缺失导致导入失败，如何处理？**

A：项目提供了数据校验模块（`backend/src/core/validator.js`）。导入前建议使用 `scripts/validate-resources.js` 脚本对 JSON 文件进行预校验。该脚本会输出缺失字段的具体位置和字段名。修正后重新导入即可。若需批量修正，可使用 `scripts/fix-resources.js` 自动补全默认值。

**Q：如何定期自动更新资源链接的可访问性状态？**

A：项目内置了链接状态检测模块（`backend/src/core/crawler.js`）。您可通过系统 cron 任务或 CI 流水线定时触发检测脚本。例如每日凌晨 2 点执行 `npm run check:links`，检测结果会自动更新至数据库 `articles` 表的 `status` 字段，并在前端界面以图标形式展示。如需邮件告警，可在 `.env` 中配置 `SMTP_*` 相关变量。

## 许可证

MIT License

Copyright (c) 2026 TechRef Navigator Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

> 外链数量: 250 | 生成时间: 2026-07-05 16:28:03
