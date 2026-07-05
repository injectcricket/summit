# Cmcvrr Article Gateway

Cmcvrr Article Gateway 是一个轻量级的技术文章聚合与导航系统，专注于对 Cmcvrr 博客平台海量历史技术文档进行索引、分类检索与快速访问。项目定位为技术资料外链汇总站，服务于开发者、运维工程师与技术研究人员，帮助其从大量历史文章中快速定位到特定主题的实践案例与深度解析。

本项目不提供文章内容的重写或转储，而是通过结构化的目录体系与关键词标签，将分散的 URL 资源组织为可高效浏览的知识地图。目标用户包括需要查阅遗留系统文档的维护人员、进行技术选型调研的架构师，以及希望从过往案例中学习最佳实践的初学者。

## 功能概览

**按技术领域分类索引** 依据文章所涉及的技术栈、框架或工具链进行一级分类，便于按专业方向筛选。

**按发布时间排序浏览** 提供按时间倒序或正序排列文章列表的能力，适合追踪特定时间窗口内的技术演变。

**关键词全文检索** 对文章标题与摘要元数据进行关键词匹配，支持布尔运算符与短语精确查询。

**ID 直接定位访问** 支持通过文章唯一数字 ID 进行精准跳转，适用于已知文章编号的内部引用场景。

**URL 规范化校验** 自动检测并提示不符合标准的 URL 格式，防止因链接拼写错误导致的访问失败。

**访问量统计与热门排序** 记录每篇文章的点击次数，提供热门文章排行，辅助发现高价值内容。

**响应式目录渲染** 在桌面端与移动端均提供清晰的文章列表与详情页布局，适配不同屏幕尺寸。

**外部链接安全警告** 对非本站域名的外部链接进行提示，降低跳转至不可信站点的风险。

## 应用场景

**遗留系统文档查阅** 当团队需要维护一个数年前上线的老系统时，可以通过本网关按时间范围筛选出该系统开发周期内的所有相关技术笔记与故障处理记录，快速了解当时的决策背景与实现细节。

**技术选型参考调研** 在进行中间件选型或框架升级前，通过关键词检索如“消息队列”“容器编排”等，收集过往项目中同类技术的实际使用体验、性能调优参数与踩坑总结，为选型会议提供数据支撑。

**新人入职知识补全** 新加入团队的开发人员可通过浏览热门文章排行与分类目录，在短时间内接触团队沉淀的高频问题解决方案与编码规范讨论，加速融入现有技术体系。

**故障复盘历史追溯** 当线上发生与过去类似的事故时，运维人员可通过精确 ID 或时间段快速定位历史故障报告，对比当前日志与过往根因分析，缩短故障定位时间。

## 快速开始

以下步骤将在本地环境中启动 Cmcvrr Article Gateway 服务。

```bash
# 克隆项目仓库至本地
git clone https://github.com/your-org/cmcvrr-gateway.git

# 进入项目根目录
cd cmcvrr-gateway

# 安装项目依赖（使用 npm）
npm install

# 启动开发服务器，默认监听 3000 端口
npm run dev
```

服务启动后，访问控制台输出的本地地址（如 http://localhost:3000）即可开始浏览文章索引。

## 安装要求

| 依赖组件 | 必需版本 | 说明 |
|---------|---------|------|
| Node.js | >= 18.0.0 | JavaScript 运行时环境，用于执行服务端代码与构建脚本 |
| npm | >= 9.0.0 | 包管理器，用于安装项目声明的全部第三方依赖 |
| PostgreSQL | >= 14.0 | 关系型数据库，用于存储文章元数据、索引与访问统计 |
| Redis | >= 6.2 | 内存缓存服务，用于提升热门文章列表与检索结果的响应速度 |
| Nginx | >= 1.20 | 反向代理服务器（生产环境推荐），用于负载均衡与静态资源缓存 |

## 文档导航

| 层面 | 目录/文档 | 回答的问题 |
|------|----------|-----------|
| 用户指南 | docs/user-guide.md | 如何使用分类浏览、检索和 ID 定位功能？热门排行如何计算与更新？ |
| 部署手册 | docs/deployment.md | 如何配置 PostgreSQL 连接池、Redis 缓存策略以及 Nginx 反向代理规则？ |
| 开发规范 | docs/development.md | 新增文章分类的流程是什么？检索索引的更新机制如何扩展？ |
| API 参考 | docs/api-reference.md | 对外提供哪些 RESTful 接口？请求参数、响应格式与状态码如何定义？ |

## 资源列表

### 平台根地址

http://www.blog.cmcvrr.cn

### 文章详情页（按 ID 升序排列）

http://www.blog.cmcvrr.cn/Article/details/0030.sHtML
http://www.blog.cmcvrr.cn/Article/details/0054.sHtML
http://www.blog.cmcvrr.cn/Article/details/01810.sHtML
http://www.blog.cmcvrr.cn/Article/details/018528.sHtML
http://www.blog.cmcvrr.cn/Article/details/01962.sHtML
http://www.blog.cmcvrr.cn/Article/details/0221.sHtML
http://www.blog.cmcvrr.cn/Article/details/028644.sHtML
http://www.blog.cmcvrr.cn/Article/details/032914.sHtML
http://www.blog.cmcvrr.cn/Article/details/0399.sHtML
http://www.blog.cmcvrr.cn/Article/details/041531.sHtML
http://www.blog.cmcvrr.cn/Article/details/0446.sHtML
http://www.blog.cmcvrr.cn/Article/details/0454609.sHtML
http://www.blog.cmcvrr.cn/Article/details/0651402.sHtML
http://www.blog.cmcvrr.cn/Article/details/073791.sHtML
http://www.blog.cmcvrr.cn/Article/details/074497.sHtML
http://www.blog.cmcvrr.cn/Article/details/0751140.sHtML
http://www.blog.cmcvrr.cn/Article/details/076404.sHtML
http://www.blog.cmcvrr.cn/Article/details/07674.sHtML
http://www.blog.cmcvrr.cn/Article/details/0862.sHtML
http://www.blog.cmcvrr.cn/Article/details/0875.sHtML
http://www.blog.cmcvrr.cn/Article/details/08893.sHtML
http://www.blog.cmcvrr.cn/Article/details/0892.sHtML
http://www.blog.cmcvrr.cn/Article/details/0926824.sHtML
http://www.blog.cmcvrr.cn/Article/details/0930.sHtML
http://www.blog.cmcvrr.cn/Article/details/0977.sHtML
http://www.blog.cmcvrr.cn/Article/details/0012061.sHtML
http://www.blog.cmcvrr.cn/Article/details/0018544.sHtML
http://www.blog.cmcvrr.cn/Article/details/016456.sHtML
http://www.blog.cmcvrr.cn/Article/details/021208.sHtML
http://www.blog.cmcvrr.cn/Article/details/000526.sHtML
http://www.blog.cmcvrr.cn/Article/details/104247.sHtML
http://www.blog.cmcvrr.cn/Article/details/1118909.sHtML
http://www.blog.cmcvrr.cn/Article/details/1129.sHtML
http://www.blog.cmcvrr.cn/Article/details/113164.sHtML
http://www.blog.cmcvrr.cn/Article/details/133503.sHtML
http://www.blog.cmcvrr.cn/Article/details/1464512.sHtML
http://www.blog.cmcvrr.cn/Article/details/1467.sHtML
http://www.blog.cmcvrr.cn/Article/details/1468.sHtML
http://www.blog.cmcvrr.cn/Article/details/1472375.sHtML
http://www.blog.cmcvrr.cn/Article/details/1491364.sHtML
http://www.blog.cmcvrr.cn/Article/details/15753.sHtML
http://www.blog.cmcvrr.cn/Article/details/1598.sHtML
http://www.blog.cmcvrr.cn/Article/details/16163.sHtML
http://www.blog.cmcvrr.cn/Article/details/16767.sHtML
http://www.blog.cmcvrr.cn/Article/details/1689.sHtML
http://www.blog.cmcvrr.cn/Article/details/1741618.sHtML
http://www.blog.cmcvrr.cn/Article/details/1743.sHtML
http://www.blog.cmcvrr.cn/Article/details/17578.sHtML
http://www.blog.cmcvrr.cn/Article/details/18337.sHtML
http://www.blog.cmcvrr.cn/Article/details/1839884.sHtML
http://www.blog.cmcvrr.cn/Article/details/190356.sHtML
http://www.blog.cmcvrr.cn/Article/details/1941.sHtML
http://www.blog.cmcvrr.cn/Article/details/21947.sHtML
http://www.blog.cmcvrr.cn/Article/details/2209473.sHtML
http://www.blog.cmcvrr.cn/Article/details/2213625.sHtML
http://www.blog.cmcvrr.cn/Article/details/2282559.sHtML
http://www.blog.cmcvrr.cn/Article/details/2284.sHtML
http://www.blog.cmcvrr.cn/Article/details/2323.sHtML
http://www.blog.cmcvrr.cn/Article/details/2352.sHtML
http://www.blog.cmcvrr.cn/Article/details/24759.sHtML
http://www.blog.cmcvrr.cn/Article/details/25014.sHtML
http://www.blog.cmcvrr.cn/Article/details/252202.sHtML
http://www.blog.cmcvrr.cn/Article/details/252660.sHtML
http://www.blog.cmcvrr.cn/Article/details/2556337.sHtML
http://www.blog.cmcvrr.cn/Article/details/25750.sHtML
http://www.blog.cmcvrr.cn/Article/details/25965.sHtML
http://www.blog.cmcvrr.cn/Article/details/2599.sHtML
http://www.blog.cmcvrr.cn/Article/details/26563.sHtML
http://www.blog.cmcvrr.cn/Article/details/2666080.sHtML
http://www.blog.cmcvrr.cn/Article/details/27293.sHtML
http://www.blog.cmcvrr.cn/Article/details/2775244.sHtML
http://www.blog.cmcvrr.cn/Article/details/2783.sHtML
http://www.blog.cmcvrr.cn/Article/details/279709.sHtML
http://www.blog.cmcvrr.cn/Article/details/28623.sHtML
http://www.blog.cmcvrr.cn/Article/details/288903.sHtML
http://www.blog.cmcvrr.cn/Article/details/3070.sHtML
http://www.blog.cmcvrr.cn/Article/details/3205685.sHtML
http://www.blog.cmcvrr.cn/Article/details/3255863.sHtML
http://www.blog.cmcvrr.cn/Article/details/333189.sHtML
http://www.blog.cmcvrr.cn/Article/details/333807.sHtML
http://www.blog.cmcvrr.cn/Article/details/3354621.sHtML
http://www.blog.cmcvrr.cn/Article/details/33905.sHtML
http://www.blog.cmcvrr.cn/Article/details/3499.sHtML
http://www.blog.cmcvrr.cn/Article/details/35095.sHtML
http://www.blog.cmcvrr.cn/Article/details/3514.sHtML
http://www.blog.cmcvrr.cn/Article/details/3546.sHtML
http://www.blog.cmcvrr.cn/Article/details/3551445.sHtML
http://www.blog.cmcvrr.cn/Article/details/35651.sHtML
http://www.blog.cmcvrr.cn/Article/details/3574908.sHtML
http://www.blog.cmcvrr.cn/Article/details/357530.sHtML
http://www.blog.cmcvrr.cn/Article/details/357746.sHtML
http://www.blog.cmcvrr.cn/Article/details/3604.sHtML
http://www.blog.cmcvrr.cn/Article/details/3654440.sHtML
http://www.blog.cmcvrr.cn/Article/details/3703984.sHtML
http://www.blog.cmcvrr.cn/Article/details/371382.sHtML
http://www.blog.cmcvrr.cn/Article/details/3741607.sHtML
http://www.blog.cmcvrr.cn/Article/details/3763573.sHtML
http://www.blog.cmcvrr.cn/Article/details/3784096.sHtML
http://www.blog.cmcvrr.cn/Article/details/38450.sHtML
http://www.blog.cmcvrr.cn/Article/details/3906.sHtML
http://www.blog.cmcvrr.cn/Article/details/39187.sHtML
http://www.blog.cmcvrr.cn/Article/details/3951.sHtML
http://www.blog.cmcvrr.cn/Article/details/395496.sHtML
http://www.blog.cmcvrr.cn/Article/details/399193.sHtML
http://www.blog.cmcvrr.cn/Article/details/4040078.sHtML
http://www.blog.cmcvrr.cn/Article/details/40422.sHtML
http://www.blog.cmcvrr.cn/Article/details/4107.sHtML
http://www.blog.cmcvrr.cn/Article/details/4113918.sHtML
http://www.blog.cmcvrr.cn/Article/details/4260.sHtML
http://www.blog.cmcvrr.cn/Article/details/4330.sHtML
http://www.blog.cmcvrr.cn/Article/details/4334.sHtML
http://www.blog.cmcvrr.cn/Article/details/4343.sHtML
http://www.blog.cmcvrr.cn/Article/details/4347591.sHtML
http://www.blog.cmcvrr.cn/Article/details/435168.sHtML
http://www.blog.cmcvrr.cn/Article/details/4393940.sHtML
http://www.blog.cmcvrr.cn/Article/details/4449.sHtML
http://www.blog.cmcvrr.cn/Article/details/445566.sHtML
http://www.blog.cmcvrr.cn/Article/details/4510.sHtML
http://www.blog.cmcvrr.cn/Article/details/45128.sHtML
http://www.blog.cmcvrr.cn/Article/details/45427.sHtML
http://www.blog.cmcvrr.cn/Article/details/4543200.sHtML
http://www.blog.cmcvrr.cn/Article/details/45500.sHtML
http://www.blog.cmcvrr.cn/Article/details/455883.sHtML
http://www.blog.cmcvrr.cn/Article/details/4647.sHtML
http://www.blog.cmcvrr.cn/Article/details/4650.sHtML
http://www.blog.cmcvrr.cn/Article/details/46741.sHtML
http://www.blog.cmcvrr.cn/Article/details/4737.sHtML
http://www.blog.cmcvrr.cn/Article/details/490920.sHtML
http://www.blog.cmcvrr.cn/Article/details/4916697.sHtML
http://www.blog.cmcvrr.cn/Article/details/501944.sHtML
http://www.blog.cmcvrr.cn/Article/details/50289.sHtML
http://www.blog.cmcvrr.cn/Article/details/5108788.sHtML
http://www.blog.cmcvrr.cn/Article/details/51962.sHtML
http://www.blog.cmcvrr.cn/Article/details/52671.sHtML
http://www.blog.cmcvrr.cn/Article/details/5327843.sHtML
http://www.blog.cmcvrr.cn/Article/details/53962.sHtML
http://www.blog.cmcvrr.cn/Article/details/540052.sHtML
http://www.blog.cmcvrr.cn/Article/details/54595.sHtML
http://www.blog.cmcvrr.cn/Article/details/5566.sHtML
http://www.blog.cmcvrr.cn/Article/details/5707471.sHtML
http://www.blog.cmcvrr.cn/Article/details/581643.sHtML
http://www.blog.cmcvrr.cn/Article/details/5843737.sHtML
http://www.blog.cmcvrr.cn/Article/details/585282.sHtML
http://www.blog.cmcvrr.cn/Article/details/591818.sHtML
http://www.blog.cmcvrr.cn/Article/details/592202.sHtML
http://www.blog.cmcvrr.cn/Article/details/5960811.sHtML
http://www.blog.cmcvrr.cn/Article/details/598719.sHtML
http://www.blog.cmcvrr.cn/Article/details/5993.sHtML
http://www.blog.cmcvrr.cn/Article/details/61170.sHtML
http://www.blog.cmcvrr.cn/Article/details/6132597.sHtML
http://www.blog.cmcvrr.cn/Article/details/61456.sHtML
http://www.blog.cmcvrr.cn/Article/details/6158633.sHtML
http://www.blog.cmcvrr.cn/Article/details/619155.sHtML
http://www.blog.cmcvrr.cn/Article/details/6330.sHtML
http://www.blog.cmcvrr.cn/Article/details/63338.sHtML
http://www.blog.cmcvrr.cn/Article/details/6334265.sHtML
http://www.blog.cmcvrr.cn/Article/details/6360166.sHtML
http://www.blog.cmcvrr.cn/Article/details/6422843.sHtML
http://www.blog.cmcvrr.cn/Article/details/66251.sHtML
http://www.blog.cmcvrr.cn/Article/details/6720.sHtML
http://www.blog.cmcvrr.cn/Article/details/67402.sHtML
http://www.blog.cmcvrr.cn/Article/details/67686.sHtML
http://www.blog.cmcvrr.cn/Article/details/67916.sHtML
http://www.blog.cmcvrr.cn/Article/details/681287.sHtML
http://www.blog.cmcvrr.cn/Article/details/682461.sHtML
http://www.blog.cmcvrr.cn/Article/details/684469.sHtML
http://www.blog.cmcvrr.cn/Article/details/68465.sHtML
http://www.blog.cmcvrr.cn/Article/details/6884398.sHtML
http://www.blog.cmcvrr.cn/Article/details/68942.sHtML
http://www.blog.cmcvrr.cn/Article/details/6898015.sHtML
http://www.blog.cmcvrr.cn/Article/details/6915709.sHtML
http://www.blog.cmcvrr.cn/Article/details/7024956.sHtML
http://www.blog.cmcvrr.cn/Article/details/7056.sHtML
http://www.blog.cmcvrr.cn/Article/details/7067488.sHtML
http://www.blog.cmcvrr.cn/Article/details/71201.sHtML
http://www.blog.cmcvrr.cn/Article/details/71397.sHtML
http://www.blog.cmcvrr.cn/Article/details/71908.sHtML
http://www.blog.cmcvrr.cn/Article/details/7216627.sHtML
http://www.blog.cmcvrr.cn/Article/details/72209.sHtML
http://www.blog.cmcvrr.cn/Article/details/7305.sHtML
http://www.blog.cmcvrr.cn/Article/details/7319.sHtML
http://www.blog.cmcvrr.cn/Article/details/7320.sHtML
http://www.blog.cmcvrr.cn/Article/details/7330.sHtML
http://www.blog.cmcvrr.cn/Article/details/7336.sHtML
http://www.blog.cmcvrr.cn/Article/details/7378038.sHtML
http://www.blog.cmcvrr.cn/Article/details/74017.sHtML
http://www.blog.cmcvrr.cn/Article/details/7408129.sHtML
http://www.blog.cmcvrr.cn/Article/details/740932.sHtML
http://www.blog.cmcvrr.cn/Article/details/7526.sHtML
http://www.blog.cmcvrr.cn/Article/details/7530821.sHtML
http://www.blog.cmcvrr.cn/Article/details/7587.sHtML
http://www.blog.cmcvrr.cn/Article/details/7669565.sHtML
http://www.blog.cmcvrr.cn/Article/details/771501.sHtML
http://www.blog.cmcvrr.cn/Article/details/7774.sHtML
http://www.blog.cmcvrr.cn/Article/details/7805.sHtML
http://www.blog.cmcvrr.cn/Article/details/781846.sHtML
http://www.blog.cmcvrr.cn/Article/details/7821757.sHtML
http://www.blog.cmcvrr.cn/Article/details/78304.sHtML
http://www.blog.cmcvrr.cn/Article/details/788680.sHtML
http://www.blog.cmcvrr.cn/Article/details/7901.sHtML
http://www.blog.cmcvrr.cn/Article/details/7901554.sHtML
http://www.blog.cmcvrr.cn/Article/details/7985208.sHtML
http://www.blog.cmcvrr.cn/Article/details/80951.sHtML
http://www.blog.cmcvrr.cn/Article/details/818932.sHtML
http://www.blog.cmcvrr.cn/Article/details/8221433.sHtML
http://www.blog.cmcvrr.cn/Article/details/822649.sHtML
http://www.blog.cmcvrr.cn/Article/details/82478.sHtML
http://www.blog.cmcvrr.cn/Article/details/82665.sHtML
http://www.blog.cmcvrr.cn/Article/details/8307296.sHtML
http://www.blog.cmcvrr.cn/Article/details/83315.sHtML
http://www.blog.cmcvrr.cn/Article/details/8346.sHtML
http://www.blog.cmcvrr.cn/Article/details/837837.sHtML
http://www.blog.cmcvrr.cn/Article/details/83997.sHtML
http://www.blog.cmcvrr.cn/Article/details/85627.sHtML
http://www.blog.cmcvrr.cn/Article/details/8608118.sHtML
http://www.blog.cmcvrr.cn/Article/details/8633228.sHtML
http://www.blog.cmcvrr.cn/Article/details/8645685.sHtML
http://www.blog.cmcvrr.cn/Article/details/87560.sHtML
http://www.blog.cmcvrr.cn/Article/details/8778.sHtML
http://www.blog.cmcvrr.cn/Article/details/878552.sHtML
http://www.blog.cmcvrr.cn/Article/details/88170.sHtML
http://www.blog.cmcvrr.cn/Article/details/885791.sHtML
http://www.blog.cmcvrr.cn/Article/details/8858123.sHtML
http://www.blog.cmcvrr.cn/Article/details/887344.sHtML
http://www.blog.cmcvrr.cn/Article/details/8922051.sHtML
http://www.blog.cmcvrr.cn/Article/details/89321.sHtML
http://www.blog.cmcvrr.cn/Article/details/8941729.sHtML
http://www.blog.cmcvrr.cn/Article/details/8968773.sHtML
http://www.blog.cmcvrr.cn/Article/details/8972421.sHtML
http://www.blog.cmcvrr.cn/Article/details/90022.sHtML
http://www.blog.cmcvrr.cn/Article/details/901884.sHtML
http://www.blog.cmcvrr.cn/Article/details/9022142.sHtML
http://www.blog.cmcvrr.cn/Article/details/9064.sHtML
http://www.blog.cmcvrr.cn/Article/details/906517.sHtML
http://www.blog.cmcvrr.cn/Article/details/91097.sHtML
http://www.blog.cmcvrr.cn/Article/details/9183232.sHtML
http://www.blog.cmcvrr.cn/Article/details/92063.sHtML
http://www.blog.cmcvrr.cn/Article/details/921638.sHtML
http://www.blog.cmcvrr.cn/Article/details/92404.sHtML
http://www.blog.cmcvrr.cn/Article/details/926685.sHtML
http://www.blog.cmcvrr.cn/Article/details/93173.sHtML
http://www.blog.cmcvrr.cn/Article/details/94115.sHtML
http://www.blog.cmcvrr.cn/Article/details/9488891.sHtML
http://www.blog.cmcvrr.cn/Article/details/952280.sHtML
http://www.blog.cmcvrr.cn/Article/details/959888.sHtML
http://www.blog.cmcvrr.cn/Article/details/962381.sHtML
http://www.blog.cmcvrr.cn/Article/details/9639.sHtML
http://www.blog.cmcvrr.cn/Article/details/9681210.sHtML
http://www.blog.cmcvrr.cn/Article/details/981730.sHtML
http://www.blog.cmcvrr.cn/Article/details/9883.sHtML

## 项目结构

```
cmcvrr-gateway/
├── src/
│   ├── controllers/               # 请求控制器，处理路由入参校验与响应封装
│   │   ├── articleController.js   # 文章详情、列表、检索、统计接口
│   │   └── categoryController.js  # 分类目录树与标签聚合接口
│   ├── services/                  # 业务逻辑层，封装数据库查询与缓存策略
│   │   ├── articleService.js      # 文章元数据获取、热度计算、ID解析
│   │   └── searchService.js       # 全文检索词法分析、索引匹配与排序
│   ├── models/                    # 数据模型定义，对应 PostgreSQL 表结构
│   │   ├── Article.js             # 文章实体：id, title, url, category, publish_date
│   │   ├── ClickLog.js            # 点击日志：article_id, timestamp, user_agent
│   │   └── Tag.js                 # 标签实体：id, name, article_count
│   ├── middleware/                # 请求拦截器，包含日志、鉴权与错误处理
│   │   ├── auth.js                # 简单 API Key 鉴权（可选）
│   │   ├── logger.js              # 访问日志记录（请求路径、耗时、状态码）
│   │   └── validator.js           # URL 参数与请求体格式校验
│   ├── routes/                    # 路由定义，挂载控制器方法至具体路径
│   │   ├── api.js                 # RESTful API 路由聚合
│   │   └── web.js                 # 服务端渲染页面路由（管理后台）
│   ├── utils/                     # 工具函数库，无业务状态的纯函数
│   │   ├── urlNormalizer.js       # URL 协议补全、尾部斜杠移除、域名校验
│   │   ├── cacheHelper.js         # Redis 连接池管理与键值序列化
│   │   └── dateFormatter.js       # 时间戳与标准日期字符串互转
│   └── app.js                     # Express 应用实例，注册中间件与路由
├── config/
│   ├── database.js                # 数据库连接配置（host, port, user, password）
│   ├── redis.js                   # Redis 连接配置与默认过期时间
│   └── appConfig.js               # 服务端口、环境变量、日志级别配置
├── docs/                          # 完整文档目录，涵盖用户手册与开发者指南
│   ├── user-guide.md
│   ├── deployment.md
│   ├── development.md
│   └── api-reference.md
├── scripts/
│   ├── initDb.sql                 # 数据库初始化脚本（建表、索引、主键）
│   └── seedArticles.js            # 从原始 URL 列表批量导入文章元数据
├── public/                        # 静态资源，由 Nginx 在生产环境托管
│   ├── css/                       # 样式表（基于 Tailwind CSS 构建）
│   ├── js/                        # 前端交互脚本（检索防抖、列表分页）
│   └── images/                    # 项目 Logo 与占位图
├── tests/                         # 单元测试与集成测试用例
│   ├── unit/                      # 工具函数与模型方法的单元测试
│   └── integration/               # API 接口端到端测试（使用 Supertest）
├── .env.example                   # 环境变量模板，供本地开发复制为 .env
├── package.json                   # npm 项目清单，声明依赖与脚本命令
└── README.md                      # 本文件
```

## 贡献指南

1. 查阅 issue 列表或自行提交新 issue，描述您希望修复的缺陷或新增的功能。在开始编码前等待维护者确认需求，避免无效劳动。

2. 从主分支（main）签出新的特性分支，分支命名遵循 feat/功能简述 或 fix/缺陷简述 格式。确保分支基于最新的主分支代码。

3. 编写或更新对应的单元测试与集成测试，确保新增代码的测试覆盖率达到 80% 以上。所有测试用例须通过后方可提交。

4. 提交代码时遵循约定式提交规范（Conventional Commits），提交信息格式为 type(scope): description，如 feat(search): add fuzzy match support。

5. 发起 Pull Request 至主分支，在 PR 描述中关联对应的 issue 编号，并简要说明实现思路与测试结果。等待至少一名维护者进行代码审查。

## 常见问题

**Q: 启动服务后，访问文章详情页返回 404，但文章 ID 在资源列表中确实存在，是什么原因？**

A: 请检查 PostgreSQL 数据库中的 articles 表是否已执行 seedArticles.js 脚本完成数据初始化。该项目不会自动从外部 URL 抓取内容，所有文章元数据需预先导入。运行 npm run seed 可触发批量导入流程。

**Q: 检索功能返回的结果不完整，部分明显包含关键词的文章未被召回，如何调整？**

A: 默认的全文检索引擎基于 PostgreSQL 的 tsvector 与 tsquery 实现，支持词干提取与停用词过滤。若需更精确的匹配，可在 config/appConfig.js 中调整 search.minTokenLength 参数（默认为 2），或修改 search.stopWords 列表移除特定停用词。调整后需重建索引（执行 npm run reindex）。

**Q: 生产环境部署后，热门文章排行长时间不更新，访问量统计似乎停滞。**

A: 请确认 Redis 缓存服务是否正常运行，以及 config/redis.js 中的连接参数是否正确。热门排行默认每 5 分钟从 ClickLog 表聚合一次并写入 Redis，若 Redis 不可用，系统会降级为实时查询但会显著增加数据库负载。可检查 logs/access.log 中是否有 Redis 连接超时错误。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:28:08
