# WebLink Navigator

WebLink Navigator 是一个面向开发者、技术研究人员与信息分析师的轻量级外链资源聚合与导航工具。该项目通过结构化方式收集并分类整理来自互联网公开渠道的技术文章、代码示例、系统运维记录与开发日志，旨在帮助技术从业者快速定位具有参考价值的实践文档与问题解决方案。

该项目定位于个人知识库补充与企业内部技术文档索引系统的中间层，不对原始内容进行二次编辑或转载，仅提供稳定、可校验的原始链接出处。WebLink Navigator 适用于需要批量管理外部技术引用、建立团队共享书签库或构建自动化文档采集管道的场景。

## 功能概览

**批量外链导入** 支持通过文本列表或 CSV 格式批量导入外部 URL，自动去重并校验可访问性。

**分类标签管理** 允许用户为每个链接赋予多个自定义标签，支持按标签筛选、合并与重命名。

**链接状态监控** 定期对已收录链接进行 HTTP 状态检查，标记失效或重定向的条目，并提供离线快照提醒。

**全文元数据提取** 自动抓取目标页面的标题、描述、发布时间及正文摘要，用于快速预览与检索。

**多级目录组织** 支持创建无限层级的文件夹结构，便于按项目、技术栈或业务域进行分层管理。

**只读模式与审计日志** 提供只读视图用于生产环境展示，同时记录所有增删改操作，便于追溯变更历史。

**Markdown 格式导出** 支持将选中链接或整个分类导出为 Markdown 列表或表格，方便集成至技术文档与 README。

**私有化部署支持** 项目基于纯静态前端与轻量后端设计，可运行于内网服务器，无需依赖外部 SaaS 服务。

## 应用场景

**技术团队内部知识库索引** 开发团队可将日常遇到的优秀技术博客、官方文档入口与问题修复记录统一收录，通过 WebLink Navigator 建立可共享的团队书签库，减少重复搜索时间。

**开源项目依赖文档归档** 开源维护者可将项目所引用的第三方库文档、设计规范与兼容性说明集中管理，确保新贡献者能快速找到所有参考资料，降低入门门槛。

**技术调研与竞品分析** 产品经理与技术分析师可批量收集竞品的技术实现文章、性能测试报告与用户反馈帖，通过标签分类进行横向对比，支撑决策报告撰写。

**自动化采集管道的中转站** 运维工程师可将定时爬虫获取的链接导入 WebLink Navigator，作为原始数据暂存区，经人工审核后再推送至主数据库或知识库系统。

## 快速开始

以下命令演示如何从 GitHub 克隆项目、安装依赖并启动开发服务器。

```bash
git clone https://github.com/weblink-navigator/weblink-navigator.git
cd weblink-navigator
npm install
npm run dev
```

执行完毕后，访问控制台输出的本地地址即可开始使用。生产环境部署请参考 `docs/deployment.md` 中的说明，使用 `npm run build` 生成静态文件并结合 Nginx 或 Caddy 提供服务。

## 安装要求

| 依赖 | 必需版本 | 说明 |
|------|----------|------|
| Node.js | 18.x 或更高 | 运行时环境，用于执行构建工具与后端服务 |
| npm | 9.x 或更高 | 包管理器，用于安装项目依赖 |
| SQLite | 3.35 或更高 | 默认嵌入式数据库，用于存储链接元数据与标签 |
| Git | 2.30 或更高 | 用于克隆仓库及版本管理 |
| curl | 7.68 或更高 | 用于链接状态监控模块的 HTTP 探测 |
| jq | 1.6 或更高 | 可选，用于命令行下解析 JSON 格式的导出数据 |
| redis | 6.2 或更高 | 可选，用于多实例部署时的缓存与任务队列 |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|------|------|------------|
| 入门 | docs/quick-start.md | 如何在一分钟内完成安装并添加第一个链接？ |
| 管理 | docs/category-management.md | 如何创建分类、移动链接以及合并重复条目？ |
| 运维 | docs/monitoring-config.md | 如何调整链接健康检查的频率与超时阈值？ |
| 开发 | docs/api-reference.md | 后端 RESTful API 的路由、请求格式与鉴权方式是什么？ |
| 扩展 | docs/webhook-integration.md | 如何配置新增链接时的回调通知，对接钉钉或飞书？ |

## 资源列表

本批次收录共计 250 个来自 blog.hcbezg.cn 的技术文章链接，按编号范围分组如下。

### 第一批次（编号 0001 - 0050）

http://www.blog.hcbezg.cn/Article/details/7092841.sHtML
http://www.blog.hcbezg.cn/Article/details/8744.sHtML
http://www.blog.hcbezg.cn/Article/details/4229641.sHtML
http://www.blog.hcbezg.cn/Article/details/6240.sHtML
http://www.blog.hcbezg.cn/Article/details/950068.sHtML
http://www.blog.hcbezg.cn/Article/details/832047.sHtML
http://www.blog.hcbezg.cn/Article/details/15632.sHtML
http://www.blog.hcbezg.cn/Article/details/947648.sHtML
http://www.blog.hcbezg.cn/Article/details/0713.sHtML
http://www.blog.hcbezg.cn/Article/details/1744.sHtML
http://www.blog.hcbezg.cn/Article/details/4524.sHtML
http://www.blog.hcbezg.cn/Article/details/536708.sHtML
http://www.blog.hcbezg.cn/Article/details/52976.sHtML
http://www.blog.hcbezg.cn/Article/details/80199.sHtML
http://www.blog.hcbezg.cn/Article/details/6640029.sHtML
http://www.blog.hcbezg.cn/Article/details/8435.sHtML
http://www.blog.hcbezg.cn/Article/details/603311.sHtML
http://www.blog.hcbezg.cn/Article/details/271008.sHtML
http://www.blog.hcbezg.cn/Article/details/5971.sHtML
http://www.blog.hcbezg.cn/Article/details/4780797.sHtML

### 第二批次（编号 0051 - 0100）

http://www.blog.hcbezg.cn/Article/details/7053.sHtML
http://www.blog.hcbezg.cn/Article/details/475005.sHtML
http://www.blog.hcbezg.cn/Article/details/146819.sHtML
http://www.blog.hcbezg.cn/Article/details/74530.sHtML
http://www.blog.hcbezg.cn/Article/details/363018.sHtML
http://www.blog.hcbezg.cn/Article/details/8928.sHtML
http://www.blog.hcbezg.cn/Article/details/001244.sHtML
http://www.blog.hcbezg.cn/Article/details/66410.sHtML
http://www.blog.hcbezg.cn/Article/details/5934404.sHtML
http://www.blog.hcbezg.cn/Article/details/27808.sHtML
http://www.blog.hcbezg.cn/Article/details/5903.sHtML
http://www.blog.hcbezg.cn/Article/details/04758.sHtML
http://www.blog.hcbezg.cn/Article/details/878288.sHtML
http://www.blog.hcbezg.cn/Article/details/641823.sHtML
http://www.blog.hcbezg.cn/Article/details/7536.sHtML
http://www.blog.hcbezg.cn/Article/details/5431319.sHtML
http://www.blog.hcbezg.cn/Article/details/010677.sHtML
http://www.blog.hcbezg.cn/Article/details/8426026.sHtML
http://www.blog.hcbezg.cn/Article/details/035660.sHtML
http://www.blog.hcbezg.cn/Article/details/846105.sHtML
http://www.blog.hcbezg.cn/Article/details/680611.sHtML
http://www.blog.hcbezg.cn/Article/details/494358.sHtML
http://www.blog.hcbezg.cn/Article/details/78331.sHtML
http://www.blog.hcbezg.cn/Article/details/19285.sHtML
http://www.blog.hcbezg.cn/Article/details/5471798.sHtML
http://www.blog.hcbezg.cn/Article/details/09157.sHtML
http://www.blog.hcbezg.cn/Article/details/75543.sHtML
http://www.blog.hcbezg.cn/Article/details/2068947.sHtML
http://www.blog.hcbezg.cn/Article/details/438390.sHtML
http://www.blog.hcbezg.cn/Article/details/6262382.sHtML
http://www.blog.hcbezg.cn/Article/details/292350.sHtML
http://www.blog.hcbezg.cn/Article/details/24624.sHtML
http://www.blog.hcbezg.cn/Article/details/8254397.sHtML
http://www.blog.hcbezg.cn/Article/details/399152.sHtML
http://www.blog.hcbezg.cn/Article/details/47090.sHtML
http://www.blog.hcbezg.cn/Article/details/495843.sHtML
http://www.blog.hcbezg.cn/Article/details/3866445.sHtML
http://www.blog.hcbezg.cn/Article/details/18259.sHtML
http://www.blog.hcbezg.cn/Article/details/743547.sHtML
http://www.blog.hcbezg.cn/Article/details/324641.sHtML
http://www.blog.hcbezg.cn/Article/details/7361.sHtML
http://www.blog.hcbezg.cn/Article/details/66888.sHtML
http://www.blog.hcbezg.cn/Article/details/97994.sHtML
http://www.blog.hcbezg.cn/Article/details/9430.sHtML
http://www.blog.hcbezg.cn/Article/details/725467.sHtML
http://www.blog.hcbezg.cn/Article/details/0730503.sHtML
http://www.blog.hcbezg.cn/Article/details/5387111.sHtML
http://www.blog.hcbezg.cn/Article/details/9875.sHtML
http://www.blog.hcbezg.cn/Article/details/0611.sHtML

### 第三批次（编号 0101 - 0150）

http://www.blog.hcbezg.cn/Article/details/4038274.sHtML
http://www.blog.hcbezg.cn/Article/details/751953.sHtML
http://www.blog.hcbezg.cn/Article/details/986907.sHtML
http://www.blog.hcbezg.cn/Article/details/871134.sHtML
http://www.blog.hcbezg.cn/Article/details/1424.sHtML
http://www.blog.hcbezg.cn/Article/details/3591.sHtML
http://www.blog.hcbezg.cn/Article/details/4003.sHtML
http://www.blog.hcbezg.cn/Article/details/920214.sHtML
http://www.blog.hcbezg.cn/Article/details/210745.sHtML
http://www.blog.hcbezg.cn/Article/details/7475.sHtML
http://www.blog.hcbezg.cn/Article/details/2898788.sHtML
http://www.blog.hcbezg.cn/Article/details/5462.sHtML
http://www.blog.hcbezg.cn/Article/details/8675.sHtML
http://www.blog.hcbezg.cn/Article/details/3535496.sHtML
http://www.blog.hcbezg.cn/Article/details/99797.sHtML
http://www.blog.hcbezg.cn/Article/details/935178.sHtML
http://www.blog.hcbezg.cn/Article/details/9589093.sHtML
http://www.blog.hcbezg.cn/Article/details/8927.sHtML
http://www.blog.hcbezg.cn/Article/details/12120.sHtML
http://www.blog.hcbezg.cn/Article/details/603125.sHtML
http://www.blog.hcbezg.cn/Article/details/199309.sHtML
http://www.blog.hcbezg.cn/Article/details/1107218.sHtML
http://www.blog.hcbezg.cn/Article/details/54910.sHtML
http://www.blog.hcbezg.cn/Article/details/7471548.sHtML
http://www.blog.hcbezg.cn/Article/details/5570465.sHtML
http://www.blog.hcbezg.cn/Article/details/877718.sHtML
http://www.blog.hcbezg.cn/Article/details/0410.sHtML
http://www.blog.hcbezg.cn/Article/details/1334.sHtML
http://www.blog.hcbezg.cn/Article/details/431926.sHtML
http://www.blog.hcbezg.cn/Article/details/2091.sHtML
http://www.blog.hcbezg.cn/Article/details/52835.sHtML
http://www.blog.hcbezg.cn/Article/details/058941.sHtML
http://www.blog.hcbezg.cn/Article/details/5275900.sHtML
http://www.blog.hcbezg.cn/Article/details/5940.sHtML
http://www.blog.hcbezg.cn/Article/details/8716561.sHtML
http://www.blog.hcbezg.cn/Article/details/547755.sHtML
http://www.blog.hcbezg.cn/Article/details/42615.sHtML
http://www.blog.hcbezg.cn/Article/details/970703.sHtML
http://www.blog.hcbezg.cn/Article/details/072578.sHtML
http://www.blog.hcbezg.cn/Article/details/702087.sHtML
http://www.blog.hcbezg.cn/Article/details/7097.sHtML
http://www.blog.hcbezg.cn/Article/details/4064.sHtML
http://www.blog.hcbezg.cn/Article/details/26219.sHtML
http://www.blog.hcbezg.cn/Article/details/3483633.sHtML
http://www.blog.hcbezg.cn/Article/details/76286.sHtML
http://www.blog.hcbezg.cn/Article/details/613599.sHtML
http://www.blog.hcbezg.cn/Article/details/82962.sHtML
http://www.blog.hcbezg.cn/Article/details/1904674.sHtML
http://www.blog.hcbezg.cn/Article/details/8256.sHtML
http://www.blog.hcbezg.cn/Article/details/2001.sHtML

### 第四批次（编号 0151 - 0200）

http://www.blog.hcbezg.cn/Article/details/9023811.sHtML
http://www.blog.hcbezg.cn/Article/details/7729021.sHtML
http://www.blog.hcbezg.cn/Article/details/3671551.sHtML
http://www.blog.hcbezg.cn/Article/details/3570882.sHtML
http://www.blog.hcbezg.cn/Article/details/8314.sHtML
http://www.blog.hcbezg.cn/Article/details/2635567.sHtML
http://www.blog.hcbezg.cn/Article/details/6380809.sHtML
http://www.blog.hcbezg.cn/Article/details/536106.sHtML
http://www.blog.hcbezg.cn/Article/details/09621.sHtML
http://www.blog.hcbezg.cn/Article/details/2205.sHtML
http://www.blog.hcbezg.cn/Article/details/7424.sHtML
http://www.blog.hcbezg.cn/Article/details/983807.sHtML
http://www.blog.hcbezg.cn/Article/details/4095035.sHtML
http://www.blog.hcbezg.cn/Article/details/4252.sHtML
http://www.blog.hcbezg.cn/Article/details/561285.sHtML
http://www.blog.hcbezg.cn/Article/details/45173.sHtML
http://www.blog.hcbezg.cn/Article/details/8057720.sHtML
http://www.blog.hcbezg.cn/Article/details/40199.sHtML
http://www.blog.hcbezg.cn/Article/details/874998.sHtML
http://www.blog.hcbezg.cn/Article/details/4906152.sHtML
http://www.blog.hcbezg.cn/Article/details/4546.sHtML
http://www.blog.hcbezg.cn/Article/details/347425.sHtML
http://www.blog.hcbezg.cn/Article/details/7430.sHtML
http://www.blog.hcbezg.cn/Article/details/8353361.sHtML
http://www.blog.hcbezg.cn/Article/details/98472.sHtML
http://www.blog.hcbezg.cn/Article/details/6349.sHtML
http://www.blog.hcbezg.cn/Article/details/1508779.sHtML
http://www.blog.hcbezg.cn/Article/details/7488.sHtML
http://www.blog.hcbezg.cn/Article/details/9419.sHtML
http://www.blog.hcbezg.cn/Article/details/1238303.sHtML
http://www.blog.hcbezg.cn/Article/details/98899.sHtML
http://www.blog.hcbezg.cn/Article/details/26455.sHtML
http://www.blog.hcbezg.cn/Article/details/79286.sHtML
http://www.blog.hcbezg.cn/Article/details/57901.sHtML
http://www.blog.hcbezg.cn/Article/details/387790.sHtML
http://www.blog.hcbezg.cn/Article/details/10863.sHtML
http://www.blog.hcbezg.cn/Article/details/98493.sHtML
http://www.blog.hcbezg.cn/Article/details/5759524.sHtML
http://www.blog.hcbezg.cn/Article/details/4855.sHtML
http://www.blog.hcbezg.cn/Article/details/148003.sHtML
http://www.blog.hcbezg.cn/Article/details/2620522.sHtML
http://www.blog.hcbezg.cn/Article/details/8226.sHtML
http://www.blog.hcbezg.cn/Article/details/4006081.sHtML
http://www.blog.hcbezg.cn/Article/details/593988.sHtML
http://www.blog.hcbezg.cn/Article/details/56150.sHtML
http://www.blog.hcbezg.cn/Article/details/4705228.sHtML
http://www.blog.hcbezg.cn/Article/details/9867595.sHtML
http://www.blog.hcbezg.cn/Article/details/169047.sHtML
http://www.blog.hcbezg.cn/Article/details/9324.sHtML
http://www.blog.hcbezg.cn/Article/details/1628.sHtML

### 第五批次（编号 0201 - 0250）

http://www.blog.hcbezg.cn/Article/details/6498897.sHtML
http://www.blog.hcbezg.cn/Article/details/1421438.sHtML
http://www.blog.hcbezg.cn/Article/details/08695.sHtML
http://www.blog.hcbezg.cn/Article/details/8580932.sHtML
http://www.blog.hcbezg.cn/Article/details/7815247.sHtML
http://www.blog.hcbezg.cn/Article/details/4782.sHtML
http://www.blog.hcbezg.cn/Article/details/533286.sHtML
http://www.blog.hcbezg.cn/Article/details/713213.sHtML
http://www.blog.hcbezg.cn/Article/details/97093.sHtML
http://www.blog.hcbezg.cn/Article/details/8447602.sHtML
http://www.blog.hcbezg.cn/Article/details/6590.sHtML
http://www.blog.hcbezg.cn/Article/details/07264.sHtML
http://www.blog.hcbezg.cn/Article/details/2080235.sHtML
http://www.blog.hcbezg.cn/Article/details/01631.sHtML
http://www.blog.hcbezg.cn/Article/details/192452.sHtML
http://www.blog.hcbezg.cn/Article/details/50063.sHtML
http://www.blog.hcbezg.cn/Article/details/655689.sHtML
http://www.blog.hcbezg.cn/Article/details/4173736.sHtML
http://www.blog.hcbezg.cn/Article/details/9790.sHtML
http://www.blog.hcbezg.cn/Article/details/627807.sHtML
http://www.blog.hcbezg.cn/Article/details/2324.sHtML
http://www.blog.hcbezg.cn/Article/details/81765.sHtML
http://www.blog.hcbezg.cn/Article/details/3339098.sHtML
http://www.blog.hcbezg.cn/Article/details/6979818.sHtML
http://www.blog.hcbezg.cn/Article/details/64000.sHtML
http://www.blog.hcbezg.cn/Article/details/5320026.sHtML
http://www.blog.hcbezg.cn/Article/details/94660.sHtML
http://www.blog.hcbezg.cn/Article/details/095117.sHtML
http://www.blog.hcbezg.cn/Article/details/0793112.sHtML
http://www.blog.hcbezg.cn/Article/details/161379.sHtML
http://www.blog.hcbezg.cn/Article/details/3798.sHtML
http://www.blog.hcbezg.cn/Article/details/7111663.sHtML
http://www.blog.hcbezg.cn/Article/details/5271.sHtML
http://www.blog.hcbezg.cn/Article/details/0322765.sHtML
http://www.blog.hcbezg.cn/Article/details/005328.sHtML
http://www.blog.hcbezg.cn/Article/details/47269.sHtML
http://www.blog.hcbezg.cn/Article/details/59368.sHtML
http://www.blog.hcbezg.cn/Article/details/5071.sHtML
http://www.blog.hcbezg.cn/Article/details/0626542.sHtML
http://www.blog.hcbezg.cn/Article/details/033098.sHtML
http://www.blog.hcbezg.cn/Article/details/38614.sHtML
http://www.blog.hcbezg.cn/Article/details/679660.sHtML
http://www.blog.hcbezg.cn/Article/details/155929.sHtML
http://www.blog.hcbezg.cn/Article/details/15122.sHtML
http://www.blog.hcbezg.cn/Article/details/2289894.sHtML
http://www.blog.hcbezg.cn/Article/details/3752.sHtML
http://www.blog.hcbezg.cn/Article/details/0933938.sHtML
http://www.blog.hcbezg.cn/Article/details/4045.sHtML
http://www.blog.hcbezg.cn/Article/details/3084409.sHtML
http://www.blog.hcbezg.cn/Article/details/0688.sHtML
http://www.blog.hcbezg.cn/Article/details/8635834.sHtML
http://www.blog.hcbezg.cn/Article/details/1332583.sHtML
http://www.blog.hcbezg.cn/Article/details/1903.sHtML
http://www.blog.hcbezg.cn/Article/details/88057.sHtML
http://www.blog.hcbezg.cn/Article/details/642701.sHtML
http://www.blog.hcbezg.cn/Article/details/43197.sHtML
http://www.blog.hcbezg.cn/Article/details/92685.sHtML
http://www.blog.hcbezg.cn/Article/details/4709129.sHtML
http://www.blog.hcbezg.cn/Article/details/4227039.sHtML
http://www.blog.hcbezg.cn/Article/details/6749908.sHtML
http://www.blog.hcbezg.cn/Article/details/7235.sHtML
http://www.blog.hcbezg.cn/Article/details/6463942.sHtML
http://www.blog.hcbezg.cn/Article/details/86342.sHtML
http://www.blog.hcbezg.cn/Article/details/17018.sHtML
http://www.blog.hcbezg.cn/Article/details/812370.sHtML
http://www.blog.hcbezg.cn/Article/details/9837.sHtML
http://www.blog.hcbezg.cn/Article/details/8925592.sHtML
http://www.blog.hcbezg.cn/Article/details/717818.sHtML
http://www.blog.hcbezg.cn/Article/details/17081.sHtML
http://www.blog.hcbezg.cn/Article/details/2744.sHtML
http://www.blog.hcbezg.cn/Article/details/26649.sHtML
http://www.blog.hcbezg.cn/Article/details/21296.sHtML
http://www.blog.hcbezg.cn/Article/details/96054.sHtML
http://www.blog.hcbezg.cn/Article/details/0588522.sHtML
http://www.blog.hcbezg.cn/Article/details/801143.sHtML
http://www.blog.hcbezg.cn/Article/details/65054.sHtML
http://www.blog.hcbezg.cn/Article/details/411402.sHtML
http://www.blog.hcbezg.cn/Article/details/3075.sHtML
http://www.blog.hcbezg.cn/Article/details/9779.sHtML
http://www.blog.hcbezg.cn/Article/details/5524.sHtML
http://www.blog.hcbezg.cn/Article/details/4333.sHtML

## 项目结构

```
weblink-navigator/
├── backend/
│   ├── src/
│   │   ├── controllers/          # 路由控制器，处理链接与分类的 CRUD
│   │   ├── models/               # SQLite 数据模型定义与迁移脚本
│   │   ├── services/             # 链接检查、元数据抓取等核心业务逻辑
│   │   ├── workers/              # 后台任务队列，如定时监控与邮件通知
│   │   └── utils/                # 通用工具函数（日志、验证、加密）
│   ├── tests/                    # 单元测试与集成测试用例
│   └── package.json              # 后端依赖声明与脚本入口
├── frontend/
│   ├── src/
│   │   ├── components/           # Vue/React 组件库（导航树、链接列表）
│   │   ├── pages/                # 路由页面（首页、分类视图、设置页）
│   │   ├── stores/               # 状态管理（链接缓存、过滤条件）
│   │   └── assets/               # 静态资源（CSS、图标、字体）
│   ├── public/                   # 构建入口与 favicon
│   └── vite.config.js            # 前端构建工具配置
├── docs/
│   ├── quick-start.md            # 快速入门指南
│   ├── category-management.md    # 分类管理详细说明
│   ├── monitoring-config.md      # 监控模块配置参数
│   ├── api-reference.md          # RESTful API 完整文档
│   └── webhook-integration.md    # 第三方通知集成指南
├── scripts/
│   ├── import-csv.js             # 批量导入 CSV 链接数据的脚本
│   ├── export-markdown.js        # 导出当前数据为 Markdown 格式的工具
│   └── health-check.js           # 手动触发全量链接状态检查的 CLI 工具
├── data/
│   ├── weblink.db                # SQLite 主数据库文件（首次启动时自动生成）
│   └── snapshots/                # 失效链接的离线页面快照存储目录
├── .env.example                  # 环境变量配置示例（含数据库路径与端口）
├── .gitignore                    # 版本控制忽略规则
├── docker-compose.yml            # 容器化编排配置（含 Redis 可选依赖）
├── Dockerfile                    # 多阶段构建镜像定义
├── LICENSE                       # MIT 许可证文本
└── README.md                     # 本文件
```

## 贡献指南

欢迎并感谢任何形式的贡献，包括但不限于提交问题报告、功能请求、代码修复与文档改进。请遵循以下步骤：

1. 在 GitHub 上 fork 本仓库，并在本地 clone 已 fork 的副本。建议在开发前运行 `npm install` 与 `npm run test` 确保现有环境通过所有测试用例。

2. 对于缺陷修复，请先在 Issues 中搜索是否已有类似报告；若无，则新建一个 Issue 详细描述复现步骤、预期行为与实际结果。对于新功能，建议先通过 Issue 与维护者讨论设计方向，避免大规模提交被拒绝。

3. 代码提交时请遵循项目的 ESLint 与 Prettier 配置，确保代码风格一致。所有新增功能必须包含对应的单元测试或集成测试，且测试覆盖率不得低于现有基线。

4. 提交 Pull Request 时请填写清晰的变更描述，并关联相关的 Issue 编号。PR 标题应使用 `<type>(<scope>): <summary>` 格式，例如 `feat(monitor): add retry policy for failed checks`。

5. 文档更新同样视为有效贡献，例如修正 README 中的错误链接、补充 API 示例或翻译其他语言版本。文档变更无需测试用例，但需确保 Markdown 语法正确且无拼写错误。

## 常见问题

**问：收录的链接如果失效了，系统会自动处理吗？**

答：系统内置的监控服务会按照可配置的周期（默认每 24 小时）对所有链接发送 HEAD 请求以检查可用性。失效链接会在界面上以特殊标记显示，并记录首次检测到失效的时间。系统不会自动删除失效链接，以便用户自行判断是否更新地址或移除。用户可在设置中配置失效链接的保留策略或启用邮件告警。

**问：能否将 WebLink Navigator 部署在完全离线的内网环境中？**

答：可以。项目所有依赖均在 `node_modules` 中完整打包，数据库使用嵌入式 SQLite，无需外部网络连接。唯一需要网络的是链接状态监控模块，但在离线环境下该模块可被禁用或配置为跳过检查。前端静态文件可直接通过 Nginx 托管，后端服务监听本地端口即可。内网部署时建议使用 Docker 镜像以简化环境一致性管理。

**问：导入大量链接时，如何避免重复条目？**

答：系统在导入时会根据 URL 字符串进行精确去重，同时支持配置模糊去重规则，例如移除末尾斜杠、统一协议（http/https）或忽略查询参数。默认策略为精确匹配，用户可在导入界面的高级选项中选择“忽略协议差异”或“忽略尾部斜杠”。去重结果会在导入预览中展示，用户确认后再执行实际写入，避免误覆盖。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:26:28
