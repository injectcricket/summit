# TechRef 外链资源聚合站

TechRef 是一个面向技术决策者、架构师与高级开发者的外链资源导航与归档项目。本项目不对任何第三方内容进行重发或转译，仅对分布于技术博客、官方文档、社区讨论与规格说明页面的高质量外部链接进行人工筛选、分类整理与结构化归档，旨在帮助技术团队在架构选型、故障排查、性能调优与安全合规等场景下快速定位有效信源。

TechRef 聚焦于链接的稳定性、可访问性与主题聚类。所有收录的 URL 均保留原始协议、域名与大小写，不做任何内容快照或代理转发。项目采用轻量级 Markdown 维护方式，适配静态站点生成器，支持通过 GitHub Action 实现每日链接存活检测与报告输出，适合作为团队内部技术导航页面的上游数据源。

## 功能概览

**按技术领域分类索引**：将外链按编程语言、中间件、云原生、安全审计、性能工程等维度进行一级分类，每类下再细化二级标签，便于用户按技术栈快速过滤。

**多格式链接清单导出**：支持输出为纯 Markdown 列表、JSON 结构化数据、以及适合嵌入 Confluence 或 Notion 的 CSV 格式，适配不同文档系统的批量导入需求。

**链接可用性自动化检查**：集成基于 HEAD 请求的链接存活检测流水线，每日定时运行，自动标记状态码异常或响应超时的条目，并在仓库 Issues 中生成待处理提醒。

**新增链接提案与评审流程**：采用 GitHub Pull Request 作为新增链接的唯一入口，要求提案人填写来源网站摘要、内容概述与推荐理由，经维护者评审后合并。

**历史版本追溯与变更日志**：每次链接增删或分类调整均通过 Git 提交记录留存，自动生成 CHANGELOG，支持按时间范围回溯外部资源的引入或移除决策。

**标签化全文检索支持**：为每条记录附加 3 至 5 个描述性标签，可与 Elasticsearch 或 Lunr.js 集成，实现站内模糊搜索，降低查找特定技术话题的时间成本。

## 应用场景

**技术选型阶段的竞品对比调研**：当团队需要在多个数据库中间件或消息队列之间做出选择时，TechRef 提供了通往各项目官方文档、性能基准测试报告以及社区讨论帖的直接入口，缩短信息收集周期。

**系统故障排查时的外部知识回溯**：在处理线上疑难杂症时，工程师可通过本项目快速找回之前阅读过的特定问题分析文章或官方 issue 讨论，避免重复在搜索引擎中过滤低质量内容。

**新成员入职技术栈体系建立**：技术负责人可以将 TechRef 中的特定分类链接集合作为新员工的学习路线图，覆盖从基础语法规范到高阶架构设计的外部优质资源，降低带教过程中的资料分发成本。

**安全漏洞应急响应信息检索**：当公开漏洞库发布新的 CVE 时，本项目维护的安全相关链接清单可帮助安全工程师迅速定位官方补丁公告、影响范围说明与临时缓解措施文档。

## 快速开始

以下命令演示了如何获取本项目源码、安装基础依赖并运行本地预览服务。请确保已安装 Git 与 Node.js 环境。

```bash
git clone https://github.com/techref/techref-stable.git
cd techref-stable
npm install
npm run build
npm run serve
```

完成上述步骤后，可通过浏览器访问本地端口 8080 查看归档链接的索引页面。若需更新链接元数据，可编辑 `data/links` 目录下的 JSON 文件，之后重新执行构建命令。

## 安装要求

本项目的运行环境要求较为基础，主要依赖 Node.js 运行时与包管理工具。若需运行链接可用性检查流水线，则额外依赖 Docker 容器环境。具体见下表：

| 依赖组件 | 必需版本 | 说明 |
|---|---|---|
| Node.js | 18.x 或 20.x LTS | 用于执行构建脚本、链接解析与静态页面生成 |
| npm | 9.x 或 10.x | 管理项目构建与测试依赖包 |
| Git | 2.40 及以上 | 用于克隆仓库、提交变更与追溯历史记录 |
| Docker Engine | 24.x 及以上 | 仅当需要本地运行链接健康检查容器时需要 |
| 网络环境 | 可访问公网 | 用于在构建阶段获取外部链接的响应状态（非强制） |

## 文档导航

为便于不同角色的用户快速定位所需信息，下表按文档层面、目录路径及核心问题进行组织：

| 层面 | 目录 | 回答的问题 |
|---|---|---|
| 用户手册 | `docs/user-guide/` | 如何检索现有链接、如何提交新链接提案、如何导出特定分类清单 |
| 维护者指南 | `docs/maintainer/` | 链接评审标准是什么、如何处理失效链接、如何管理标签体系 |
| 自动化流水线 | `docs/pipeline/` | 链接检测如何配置、报告如何解读、如何调整检测频率 |
| 数据模型 | `docs/schema/` | 链接条目的 JSON 结构定义、必填字段与扩展字段说明 |

## 资源列表

本批次收录的资源全部来自于 `blog.fuvxie.cn` 站点，该站点主要发布技术实践类文章，涉及后端开发、系统运维、数据库调优等多个方向。以下按原始来源归类列出全部 250 个外链地址。每个 URL 均原样呈现，未做任何协议转换、域名修正或路径改写。

### 基础文章编号段（0000 - 9999）

http://www.blog.fuvxie.cn/Article/details/027158.sHtML
http://www.blog.fuvxie.cn/Article/details/720588.sHtML
http://www.blog.fuvxie.cn/Article/details/982715.sHtML
http://www.blog.fuvxie.cn/Article/details/863104.sHtML
http://www.blog.fuvxie.cn/Article/details/8560.sHtML
http://www.blog.fuvxie.cn/Article/details/6913498.sHtML
http://www.blog.fuvxie.cn/Article/details/81736.sHtML
http://www.blog.fuvxie.cn/Article/details/0340.sHtML
http://www.blog.fuvxie.cn/Article/details/2188.sHtML
http://www.blog.fuvxie.cn/Article/details/8033728.sHtML
http://www.blog.fuvxie.cn/Article/details/6383002.sHtML
http://www.blog.fuvxie.cn/Article/details/1520272.sHtML
http://www.blog.fuvxie.cn/Article/details/4660959.sHtML
http://www.blog.fuvxie.cn/Article/details/36655.sHtML
http://www.blog.fuvxie.cn/Article/details/9475652.sHtML
http://www.blog.fuvxie.cn/Article/details/7818429.sHtML
http://www.blog.fuvxie.cn/Article/details/3236978.sHtML
http://www.blog.fuvxie.cn/Article/details/57520.sHtML
http://www.blog.fuvxie.cn/Article/details/32168.sHtML
http://www.blog.fuvxie.cn/Article/details/8461.sHtML
http://www.blog.fuvxie.cn/Article/details/42445.sHtML
http://www.blog.fuvxie.cn/Article/details/5716.sHtML
http://www.blog.fuvxie.cn/Article/details/00988.sHtML
http://www.blog.fuvxie.cn/Article/details/79180.sHtML
http://www.blog.fuvxie.cn/Article/details/9688.sHtML
http://www.blog.fuvxie.cn/Article/details/2063687.sHtML
http://www.blog.fuvxie.cn/Article/details/9644730.sHtML
http://www.blog.fuvxie.cn/Article/details/73788.sHtML
http://www.blog.fuvxie.cn/Article/details/5092.sHtML
http://www.blog.fuvxie.cn/Article/details/80438.sHtML
http://www.blog.fuvxie.cn/Article/details/06717.sHtML
http://www.blog.fuvxie.cn/Article/details/766322.sHtML
http://www.blog.fuvxie.cn/Article/details/14272.sHtML
http://www.blog.fuvxie.cn/Article/details/3735638.sHtML
http://www.blog.fuvxie.cn/Article/details/616394.sHtML
http://www.blog.fuvxie.cn/Article/details/6582.sHtML
http://www.blog.fuvxie.cn/Article/details/322255.sHtML
http://www.blog.fuvxie.cn/Article/details/9016.sHtML
http://www.blog.fuvxie.cn/Article/details/52346.sHtML
http://www.blog.fuvxie.cn/Article/details/28107.sHtML
http://www.blog.fuvxie.cn/Article/details/420587.sHtML
http://www.blog.fuvxie.cn/Article/details/5486.sHtML
http://www.blog.fuvxie.cn/Article/details/17525.sHtML
http://www.blog.fuvxie.cn/Article/details/518747.sHtML
http://www.blog.fuvxie.cn/Article/details/373881.sHtML
http://www.blog.fuvxie.cn/Article/details/73013.sHtML
http://www.blog.fuvxie.cn/Article/details/9075.sHtML
http://www.blog.fuvxie.cn/Article/details/4366.sHtML
http://www.blog.fuvxie.cn/Article/details/762671.sHtML
http://www.blog.fuvxie.cn/Article/details/918643.sHtML
http://www.blog.fuvxie.cn/Article/details/1919582.sHtML
http://www.blog.fuvxie.cn/Article/details/97734.sHtML
http://www.blog.fuvxie.cn/Article/details/66901.sHtML
http://www.blog.fuvxie.cn/Article/details/7019143.sHtML
http://www.blog.fuvxie.cn/Article/details/9099737.sHtML
http://www.blog.fuvxie.cn/Article/details/3841.sHtML
http://www.blog.fuvxie.cn/Article/details/5147826.sHtML
http://www.blog.fuvxie.cn/Article/details/6304071.sHtML
http://www.blog.fuvxie.cn/Article/details/070931.sHtML
http://www.blog.fuvxie.cn/Article/details/8295659.sHtML
http://www.blog.fuvxie.cn/Article/details/984980.sHtML
http://www.blog.fuvxie.cn/Article/details/55070.sHtML
http://www.blog.fuvxie.cn/Article/details/5439.sHtML
http://www.blog.fuvxie.cn/Article/details/3269.sHtML
http://www.blog.fuvxie.cn/Article/details/34057.sHtML
http://www.blog.fuvxie.cn/Article/details/754399.sHtML
http://www.blog.fuvxie.cn/Article/details/3756393.sHtML
http://www.blog.fuvxie.cn/Article/details/2211.sHtML
http://www.blog.fuvxie.cn/Article/details/1764977.sHtML
http://www.blog.fuvxie.cn/Article/details/6781857.sHtML
http://www.blog.fuvxie.cn/Article/details/714745.sHtML
http://www.blog.fuvxie.cn/Article/details/74628.sHtML
http://www.blog.fuvxie.cn/Article/details/6085015.sHtML
http://www.blog.fuvxie.cn/Article/details/05987.sHtML
http://www.blog.fuvxie.cn/Article/details/9431.sHtML
http://www.blog.fuvxie.cn/Article/details/44269.sHtML
http://www.blog.fuvxie.cn/Article/details/80892.sHtML
http://www.blog.fuvxie.cn/Article/details/917847.sHtML
http://www.blog.fuvxie.cn/Article/details/30061.sHtML
http://www.blog.fuvxie.cn/Article/details/0545.sHtML
http://www.blog.fuvxie.cn/Article/details/19977.sHtML
http://www.blog.fuvxie.cn/Article/details/43779.sHtML
http://www.blog.fuvxie.cn/Article/details/5223.sHtML
http://www.blog.fuvxie.cn/Article/details/90121.sHtML
http://www.blog.fuvxie.cn/Article/details/0318192.sHtML
http://www.blog.fuvxie.cn/Article/details/9779.sHtML
http://www.blog.fuvxie.cn/Article/details/0639475.sHtML
http://www.blog.fuvxie.cn/Article/details/504410.sHtML
http://www.blog.fuvxie.cn/Article/details/9146728.sHtML
http://www.blog.fuvxie.cn/Article/details/027876.sHtML
http://www.blog.fuvxie.cn/Article/details/5722.sHtML
http://www.blog.fuvxie.cn/Article/details/7264.sHtML
http://www.blog.fuvxie.cn/Article/details/1578012.sHtML
http://www.blog.fuvxie.cn/Article/details/00456.sHtML
http://www.blog.fuvxie.cn/Article/details/180544.sHtML
http://www.blog.fuvxie.cn/Article/details/2946.sHtML
http://www.blog.fuvxie.cn/Article/details/5893630.sHtML
http://www.blog.fuvxie.cn/Article/details/621731.sHtML
http://www.blog.fuvxie.cn/Article/details/73460.sHtML
http://www.blog.fuvxie.cn/Article/details/2831416.sHtML
http://www.blog.fuvxie.cn/Article/details/409642.sHtML
http://www.blog.fuvxie.cn/Article/details/020019.sHtML
http://www.blog.fuvxie.cn/Article/details/501505.sHtML
http://www.blog.fuvxie.cn/Article/details/07909.sHtML
http://www.blog.fuvxie.cn/Article/details/52871.sHtML
http://www.blog.fuvxie.cn/Article/details/81416.sHtML
http://www.blog.fuvxie.cn/Article/details/25612.sHtML
http://www.blog.fuvxie.cn/Article/details/2046.sHtML
http://www.blog.fuvxie.cn/Article/details/0629.sHtML
http://www.blog.fuvxie.cn/Article/details/122402.sHtML
http://www.blog.fuvxie.cn/Article/details/15307.sHtML
http://www.blog.fuvxie.cn/Article/details/752347.sHtML
http://www.blog.fuvxie.cn/Article/details/1161.sHtML
http://www.blog.fuvxie.cn/Article/details/7709916.sHtML
http://www.blog.fuvxie.cn/Article/details/4321562.sHtML
http://www.blog.fuvxie.cn/Article/details/7621.sHtML
http://www.blog.fuvxie.cn/Article/details/606918.sHtML
http://www.blog.fuvxie.cn/Article/details/7144587.sHtML
http://www.blog.fuvxie.cn/Article/details/185946.sHtML
http://www.blog.fuvxie.cn/Article/details/4878.sHtML
http://www.blog.fuvxie.cn/Article/details/7471935.sHtML
http://www.blog.fuvxie.cn/Article/details/3936.sHtML
http://www.blog.fuvxie.cn/Article/details/355437.sHtML
http://www.blog.fuvxie.cn/Article/details/8593818.sHtML
http://www.blog.fuvxie.cn/Article/details/4966.sHtML
http://www.blog.fuvxie.cn/Article/details/4561633.sHtML
http://www.blog.fuvxie.cn/Article/details/6765.sHtML
http://www.blog.fuvxie.cn/Article/details/15780.sHtML
http://www.blog.fuvxie.cn/Article/details/114904.sHtML
http://www.blog.fuvxie.cn/Article/details/7223.sHtML
http://www.blog.fuvxie.cn/Article/details/5791416.sHtML
http://www.blog.fuvxie.cn/Article/details/0986530.sHtML
http://www.blog.fuvxie.cn/Article/details/8721231.sHtML
http://www.blog.fuvxie.cn/Article/details/157412.sHtML
http://www.blog.fuvxie.cn/Article/details/497494.sHtML
http://www.blog.fuvxie.cn/Article/details/2586.sHtML
http://www.blog.fuvxie.cn/Article/details/03435.sHtML
http://www.blog.fuvxie.cn/Article/details/23354.sHtML
http://www.blog.fuvxie.cn/Article/details/0074.sHtML
http://www.blog.fuvxie.cn/Article/details/3285.sHtML
http://www.blog.fuvxie.cn/Article/details/4457.sHtML
http://www.blog.fuvxie.cn/Article/details/84051.sHtML
http://www.blog.fuvxie.cn/Article/details/1296.sHtML
http://www.blog.fuvxie.cn/Article/details/60883.sHtML
http://www.blog.fuvxie.cn/Article/details/86393.sHtML
http://www.blog.fuvxie.cn/Article/details/65272.sHtML
http://www.blog.fuvxie.cn/Article/details/6031.sHtML
http://www.blog.fuvxie.cn/Article/details/2823282.sHtML
http://www.blog.fuvxie.cn/Article/details/007751.sHtML
http://www.blog.fuvxie.cn/Article/details/0402625.sHtML
http://www.blog.fuvxie.cn/Article/details/4013425.sHtML
http://www.blog.fuvxie.cn/Article/details/86413.sHtML
http://www.blog.fuvxie.cn/Article/details/1948200.sHtML
http://www.blog.fuvxie.cn/Article/details/65188.sHtML
http://www.blog.fuvxie.cn/Article/details/1560.sHtML
http://www.blog.fuvxie.cn/Article/details/6995.sHtML
http://www.blog.fuvxie.cn/Article/details/145665.sHtML
http://www.blog.fuvxie.cn/Article/details/9794.sHtML
http://www.blog.fuvxie.cn/Article/details/81199.sHtML
http://www.blog.fuvxie.cn/Article/details/33928.sHtML
http://www.blog.fuvxie.cn/Article/details/1197.sHtML
http://www.blog.fuvxie.cn/Article/details/9758016.sHtML
http://www.blog.fuvxie.cn/Article/details/61191.sHtML
http://www.blog.fuvxie.cn/Article/details/8151872.sHtML
http://www.blog.fuvxie.cn/Article/details/105804.sHtML
http://www.blog.fuvxie.cn/Article/details/17999.sHtML
http://www.blog.fuvxie.cn/Article/details/5000775.sHtML
http://www.blog.fuvxie.cn/Article/details/9132364.sHtML
http://www.blog.fuvxie.cn/Article/details/9175426.sHtML
http://www.blog.fuvxie.cn/Article/details/4160.sHtML
http://www.blog.fuvxie.cn/Article/details/416901.sHtML
http://www.blog.fuvxie.cn/Article/details/3382.sHtML
http://www.blog.fuvxie.cn/Article/details/47150.sHtML
http://www.blog.fuvxie.cn/Article/details/1815579.sHtML
http://www.blog.fuvxie.cn/Article/details/991204.sHtML
http://www.blog.fuvxie.cn/Article/details/4297192.sHtML
http://www.blog.fuvxie.cn/Article/details/534579.sHtML
http://www.blog.fuvxie.cn/Article/details/2064.sHtML
http://www.blog.fuvxie.cn/Article/details/6122387.sHtML
http://www.blog.fuvxie.cn/Article/details/913297.sHtML
http://www.blog.fuvxie.cn/Article/details/6097653.sHtML
http://www.blog.fuvxie.cn/Article/details/9697.sHtML
http://www.blog.fuvxie.cn/Article/details/689605.sHtML
http://www.blog.fuvxie.cn/Article/details/6741.sHtML
http://www.blog.fuvxie.cn/Article/details/3061312.sHtML
http://www.blog.fuvxie.cn/Article/details/09070.sHtML
http://www.blog.fuvxie.cn/Article/details/220098.sHtML
http://www.blog.fuvxie.cn/Article/details/3942.sHtML
http://www.blog.fuvxie.cn/Article/details/5795.sHtML
http://www.blog.fuvxie.cn/Article/details/99514.sHtML
http://www.blog.fuvxie.cn/Article/details/3166.sHtML
http://www.blog.fuvxie.cn/Article/details/790591.sHtML
http://www.blog.fuvxie.cn/Article/details/7824575.sHtML
http://www.blog.fuvxie.cn/Article/details/8887931.sHtML
http://www.blog.fuvxie.cn/Article/details/8579865.sHtML
http://www.blog.fuvxie.cn/Article/details/6086.sHtML
http://www.blog.fuvxie.cn/Article/details/3535.sHtML
http://www.blog.fuvxie.cn/Article/details/1559.sHtML
http://www.blog.fuvxie.cn/Article/details/62962.sHtML
http://www.blog.fuvxie.cn/Article/details/415116.sHtML
http://www.blog.fuvxie.cn/Article/details/884397.sHtML
http://www.blog.fuvxie.cn/Article/details/1184.sHtML
http://www.blog.fuvxie.cn/Article/details/305821.sHtML
http://www.blog.fuvxie.cn/Article/details/2870.sHtML
http://www.blog.fuvxie.cn/Article/details/2820.sHtML
http://www.blog.fuvxie.cn/Article/details/417075.sHtML
http://www.blog.fuvxie.cn/Article/details/551405.sHtML
http://www.blog.fuvxie.cn/Article/details/526792.sHtML
http://www.blog.fuvxie.cn/Article/details/130166.sHtML
http://www.blog.fuvxie.cn/Article/details/529397.sHtML
http://www.blog.fuvxie.cn/Article/details/3975933.sHtML
http://www.blog.fuvxie.cn/Article/details/62667.sHtML
http://www.blog.fuvxie.cn/Article/details/514491.sHtML
http://www.blog.fuvxie.cn/Article/details/345575.sHtML
http://www.blog.fuvxie.cn/Article/details/9682.sHtML
http://www.blog.fuvxie.cn/Article/details/0318.sHtML
http://www.blog.fuvxie.cn/Article/details/6628068.sHtML
http://www.blog.fuvxie.cn/Article/details/7394.sHtML
http://www.blog.fuvxie.cn/Article/details/5964561.sHtML
http://www.blog.fuvxie.cn/Article/details/1360807.sHtML
http://www.blog.fuvxie.cn/Article/details/01596.sHtML
http://www.blog.fuvxie.cn/Article/details/1123.sHtML
http://www.blog.fuvxie.cn/Article/details/85438.sHtML
http://www.blog.fuvxie.cn/Article/details/5236906.sHtML
http://www.blog.fuvxie.cn/Article/details/800381.sHtML
http://www.blog.fuvxie.cn/Article/details/242516.sHtML
http://www.blog.fuvxie.cn/Article/details/73221.sHtML
http://www.blog.fuvxie.cn/Article/details/9541941.sHtML
http://www.blog.fuvxie.cn/Article/details/3326600.sHtML
http://www.blog.fuvxie.cn/Article/details/680916.sHtML
http://www.blog.fuvxie.cn/Article/details/350588.sHtML
http://www.blog.fuvxie.cn/Article/details/8062593.sHtML
http://www.blog.fuvxie.cn/Article/details/34866.sHtML
http://www.blog.fuvxie.cn/Article/details/4352.sHtML
http://www.blog.fuvxie.cn/Article/details/609888.sHtML
http://www.blog.fuvxie.cn/Article/details/419854.sHtML
http://www.blog.fuvxie.cn/Article/details/4790930.sHtML
http://www.blog.fuvxie.cn/Article/details/074723.sHtML
http://www.blog.fuvxie.cn/Article/details/909768.sHtML
http://www.blog.fuvxie.cn/Article/details/61571.sHtML
http://www.blog.fuvxie.cn/Article/details/49960.sHtML
http://www.blog.fuvxie.cn/Article/details/3056.sHtML
http://www.blog.fuvxie.cn/Article/details/1506393.sHtML
http://www.blog.fuvxie.cn/Article/details/175481.sHtML
http://www.blog.fuvxie.cn/Article/details/762972.sHtML
http://www.blog.fuvxie.cn/Article/details/15313.sHtML
http://www.blog.fuvxie.cn/Article/details/0512308.sHtML
http://www.blog.fuvxie.cn/Article/details/06134.sHtML
http://www.blog.fuvxie.cn/Article/details/632182.sHtML
http://www.blog.fuvxie.cn/Article/details/1606.sHtML

## 项目结构

项目采用分层目录设计，将数据定义、构建逻辑、文档与流水线配置清晰分离。下方 ASCII 目录树展示了核心目录与文件，并附带注释说明其职责。

```
techref-stable/
├── data/
│   ├── links/                         # 链接数据源，按分类存放 JSON 文件
│   │   ├── database.json              # 数据库相关链接（MySQL, PostgreSQL, Redis）
│   │   ├── language-runtime.json      # 编程语言与运行时（Go, Java, Node.js）
│   │   ├── infrastructure.json        # 基础设施与云原生（Docker, K8s, Terraform）
│   │   ├── security.json              # 安全审计与加密协议
│   │   └── performance.json           # 性能压测与调优工具
│   ├── tags/                          # 标签体系定义，含同义词与层级关系
│   │   └── tag-graph.json
│   └── sources/                       # 来源站点白名单与可信度评级
│       └── trust-level.yaml
├── scripts/
│   ├── build/                         # 构建相关脚本，负责生成静态索引
│   │   ├── generate-index.js
│   │   └── validate-schema.js
│   ├── pipeline/                      # 自动化流水线脚本
│   │   ├── link-checker/             # 链接存活检测主程序（基于 Puppeteer）
│   │   ├── report-generator.js
│   │   └── issue-creator.js
│   └── migrate/                       # 数据迁移与格式升级工具
│       └── v2-to-v3-converter.js
├── docs/
│   ├── user-guide/                    # 用户手册，含检索与提案流程
│   ├── maintainer/                    # 维护者指南，含评审标准与标签管理
│   ├── pipeline/                      # 流水线配置说明与故障排除
│   └── schema/                        # JSON Schema 定义与示例
├── .github/
│   └── workflows/                     # GitHub Actions 工作流定义
│       ├── daily-link-check.yml      # 每日链接检测
│       └── pr-validator.yml          # PR 新增链接格式校验
├── output/                            # 构建输出目录（不纳入版本控制）
│   ├── index.html
│   ├── links.json
│   └── links.csv
├── package.json                       # Node.js 项目清单与依赖声明
├── README.md                          # 项目主文档（本文件）
└── LICENSE                            # MIT 许可证文本
```

## 贡献指南

本项目鼓励外部贡献者以标准开源协作方式参与链接库的扩充与维护。所有贡献需遵循以下步骤：

1. 复刻本项目至个人命名空间，并在本地新建功能分支。分支命名建议采用 `feat/add-{category}-links` 或 `fix/update-{source}-url` 格式，以便维护者快速识别变更意图。

2. 在 `data/links` 下对应分类的 JSON 文件中新增链接条目。每条记录必须包含 `url`、`title`、`description`、`tags` 与 `source` 五个必填字段，并确保 `url` 值使用原始大小写与协议，禁止进行任何格式转换。

3. 提交变更前，在本地运行 `npm run validate` 以校验新增条目的数据结构是否符合 Schema 定义，同时运行 `npm run check-duplicates` 检测是否存在重复或高度相似的链接。

4. 发起 Pull Request 到主仓库的 `main` 分支，并在 PR 描述中逐一说明新增链接的推荐理由、适用技术场景以及原文的大致发布时间。若为更新失效链接，需提供替换前后的访问测试结果。

5. 等待维护者评审。评审通过后，PR 将被合并，同时自动化流水线将触发增量构建，更新线上索引页面。若 PR 涉及大规模链接增删（超过 50 条），需在 PR 标题中添加 `[BULK]` 前缀以触发额外的人工审核流程。

## 常见问题

**问：为什么不对收录的外部链接做内容镜像或网页存档？**

本项目定位为导航与索引工具，而非内容托管平台。做内容镜像会涉及版权合规风险，同时大幅增加存储与带宽成本。用户访问原始链接可以获得最新的内容版本，包括作者后续的勘误与更新，这对技术决策场景至关重要。我们通过每日链接检测尽量保证列表中的 URL 可访问，但不对第三方内容的持续可用性承担保证责任。

**问：提交新链接时，如何判断应该放在哪个分类 JSON 文件中？**

分类判断以链接核心主题为准。如果一篇文章同时涉及数据库与容器编排，优先归入 `infrastructure.json`。若无法确定，可在 PR 描述中标注 `category: unsure`，维护者在评审时会根据标签体系进行二次归类。归类决策记录在 PR 评论中，供后续贡献者参考。

**问：链接检测流水线报告显示某个链接返回 403 或 429 状态码，应该如何处理？**

这类状态码通常表示目标站点启用了访问频率限制或反爬机制。流水线会连续三天在不同时段（UTC 0 时、6 时、12 时）重试三次。若所有重试均失败，流水线会在仓库 Issue 中生成一条待处理提醒。处理方式包括：手动访问验证链接是否确实失效、在链接记录中添加 `notes` 字段说明限制情况，或替换为站内镜像链接（若有官方提供）。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:26:27
