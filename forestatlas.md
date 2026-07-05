# WebIndex Core

WebIndex Core 是一个面向技术开发者与架构师设计的轻量化外链资源聚合与导航系统。项目定位于将散落在技术博客、官方文档与社区讨论中的高质量深度文章、教程与参考手册，通过结构化索引的方式进行集中管理和分类呈现。系统本身不存储文章内容，仅提供元数据抓取、标签化分类与全文检索入口，帮助技术团队在信息过载的环境中快速定位到所需的技术方案与最佳实践。

本项目特别适用于需要维护内部技术知识库的团队、需要定期跟进技术动态的架构师，以及希望建立个人技术阅读工作流的开发者。通过统一的资源收录标准和多维度检索能力，WebIndex Core 能够显著降低技术信息筛选的时间成本，提升知识复用的效率。

## 功能概览

**资源自动收录** 系统通过配置化的爬虫策略，对指定的技术博客与文章站点进行定期扫描，自动提取文章标题、发布时间、摘要与标签信息，形成标准化的资源条目。

**多维度标签分类** 每一条收录的资源均可通过编程接口或管理后台赋予多个分类标签，支持按照技术栈、难度等级、应用场景等维度进行筛选与聚合。

**全文检索与过滤** 基于倒排索引机制，提供对资源标题、摘要和关键词的全文检索能力，同时支持按照日期范围、标签组合与来源域名进行过滤。

**资源状态监控** 对已收录的 URL 进行定期的可用性检查，自动标记失效链接与内容变更节点，保证索引库的鲜活度和可靠性。

**自定义元数据扩展** 允许用户为每一条资源附加自定义字段，如阅读优先级、内部备注、关联项目编号等，满足企业级知识管理的个性化需求。

**导入导出接口** 提供标准化的 JSON 与 CSV 格式数据导入导出功能，便于与其他知识管理工具或数据分析平台进行对接。

**访问统计与分析** 记录资源条目的点击次数与访问来源，生成简单的热度趋势报表，辅助团队识别高价值内容。

**权限分级管理** 内置基于角色的访问控制模型，支持管理员、编辑者、只读用户三级权限划分，适用于团队协作场景。

## 应用场景

技术团队内部知识库建设：团队可以将日常踩坑记录、技术复盘文档和外部优质教程统一收录到 WebIndex Core 中，通过标签体系按项目或技术领域进行分类，新成员入职时可直接通过检索快速了解团队所用技术栈的周边生态与常见问题解决方案。

技术选型与方案调研：架构师在进行技术选型时，可通过系统检索特定技术关键词，快速聚合来自不同来源的评测文章、性能对比报告和实际落地案例，大幅缩短调研周期并提高决策依据的全面性。

个人技术阅读工作流管理：开发者可将系统作为个人 RSS 阅读器的补充，定期浏览新收录的资源，对自己感兴趣的文章标记优先级，形成可持续的技术输入管道，避免因信息分散而遗漏重要更新。

自动化文档监控：运维或 DevOps 团队可配置监控规则，对官方发布日志、安全公告等特定来源的资源进行重点追踪，当收录到新的版本发布或漏洞修复文章时，系统可通过 Webhook 触发通知，确保关键信息及时触达相关人员。

## 快速开始

以下步骤将指导您在本地环境中快速启动 WebIndex Core 服务。

```bash
# 克隆项目仓库至本地
git clone https://github.com/webindex/core.git webindex-core

# 进入项目目录
cd webindex-core

# 安装项目依赖（使用 pip 配合 requirements.txt）
pip install -r requirements.txt

# 初始化数据库并创建默认管理员账户
python manage.py initdb --admin-email admin@example.com

# 启动开发服务器
python manage.py runserver --host 0.0.0.0 --port 8080
```

服务启动后，访问 http://localhost:8080 即可进入系统管理界面。默认管理员密码将在初始化时输出至终端日志，首次登录后请及时修改。

## 安装要求

| 依赖组件 | 必需版本 | 说明 |
|---|---|---|
| Python | 3.9 及以上 | 核心运行环境，建议使用 3.10 LTS 版本以获得更好的性能与稳定性 |
| PostgreSQL | 13.0 及以上 | 主数据存储引擎，用于存放资源元数据、用户信息和分类标签 |
| Elasticsearch | 7.17 或 8.x | 全文检索引擎，负责资源标题与摘要的索引构建与查询响应 |
| Redis | 6.0 及以上 | 缓存中间件，用于加速高频查询和存储会话数据 |
| Node.js | 16.0 及以上 | 仅在前端构建任务时需要，生产环境运行时无需安装 |
| Nginx | 1.20 及以上 | 生产环境推荐反向代理服务器，用于负载均衡和静态资源服务 |
| Supervisor | 4.0 及以上 | 进程管理工具，用于生产环境下保证服务进程的持续运行与自动重启 |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|---|---|---|
| 入门指南 | docs/quickstart.md | 如何在一小时内完成安装部署并录入第一条资源？ |
| 管理员手册 | docs/admin-guide.md | 如何配置爬虫策略、管理用户权限和查看系统统计？ |
| 开发者文档 | docs/developer-guide.md | 如何扩展自定义解析器、增加新的标签分类逻辑或集成外部 API？ |
| API 参考 | docs/api-reference.md | 系统提供了哪些 RESTful 接口？请求与响应的数据格式是怎样的？ |
| 部署运维 | docs/deployment.md | 如何在生产环境中配置高可用架构、备份恢复数据以及进行性能调优？ |
| 常见问题 | docs/faq.md | 遇到检索结果不准确、爬虫被屏蔽或数据迁移失败时该如何排查？ |

## 资源列表

技术文章收录源（按文章 ID 排序）

http://www.blog.hcbezg.cn/Article/details/1207.sHtML
http://www.blog.hcbezg.cn/Article/details/5832.sHtML
http://www.blog.hcbezg.cn/Article/details/59926.sHtML
http://www.blog.hcbezg.cn/Article/details/39477.sHtML
http://www.blog.hcbezg.cn/Article/details/12209.sHtML
http://www.blog.hcbezg.cn/Article/details/8562.sHtML
http://www.blog.hcbezg.cn/Article/details/31883.sHtML
http://www.blog.hcbezg.cn/Article/details/2828.sHtML
http://www.blog.hcbezg.cn/Article/details/1579959.sHtML
http://www.blog.hcbezg.cn/Article/details/54841.sHtML
http://www.blog.hcbezg.cn/Article/details/3925780.sHtML
http://www.blog.hcbezg.cn/Article/details/27447.sHtML
http://www.blog.hcbezg.cn/Article/details/47487.sHtML
http://www.blog.hcbezg.cn/Article/details/75993.sHtML
http://www.blog.hcbezg.cn/Article/details/871047.sHtML
http://www.blog.hcbezg.cn/Article/details/004591.sHtML
http://www.blog.hcbezg.cn/Article/details/88716.sHtML
http://www.blog.hcbezg.cn/Article/details/1831090.sHtML
http://www.blog.hcbezg.cn/Article/details/729126.sHtML
http://www.blog.hcbezg.cn/Article/details/12954.sHtML
http://www.blog.hcbezg.cn/Article/details/6378149.sHtML
http://www.blog.hcbezg.cn/Article/details/8173767.sHtML
http://www.blog.hcbezg.cn/Article/details/44668.sHtML
http://www.blog.hcbezg.cn/Article/details/2538190.sHtML
http://www.blog.hcbezg.cn/Article/details/201569.sHtML
http://www.blog.hcbezg.cn/Article/details/0542518.sHtML
http://www.blog.hcbezg.cn/Article/details/07383.sHtML
http://www.blog.hcbezg.cn/Article/details/228668.sHtML
http://www.blog.hcbezg.cn/Article/details/69154.sHtML
http://www.blog.hcbezg.cn/Article/details/101426.sHtML
http://www.blog.hcbezg.cn/Article/details/9502.sHtML
http://www.blog.hcbezg.cn/Article/details/63149.sHtML
http://www.blog.hcbezg.cn/Article/details/3219.sHtML
http://www.blog.hcbezg.cn/Article/details/8046070.sHtML
http://www.blog.hcbezg.cn/Article/details/018946.sHtML
http://www.blog.hcbezg.cn/Article/details/33060.sHtML
http://www.blog.hcbezg.cn/Article/details/757950.sHtML
http://www.blog.hcbezg.cn/Article/details/6153.sHtML
http://www.blog.hcbezg.cn/Article/details/35884.sHtML
http://www.blog.hcbezg.cn/Article/details/2643.sHtML
http://www.blog.hcbezg.cn/Article/details/107148.sHtML
http://www.blog.hcbezg.cn/Article/details/04095.sHtML
http://www.blog.hcbezg.cn/Article/details/44962.sHtML
http://www.blog.hcbezg.cn/Article/details/85632.sHtML
http://www.blog.hcbezg.cn/Article/details/92190.sHtML
http://www.blog.hcbezg.cn/Article/details/8569288.sHtML
http://www.blog.hcbezg.cn/Article/details/1958799.sHtML
http://www.blog.hcbezg.cn/Article/details/8181193.sHtML
http://www.blog.hcbezg.cn/Article/details/51421.sHtML
http://www.blog.hcbezg.cn/Article/details/1199595.sHtML
http://www.blog.hcbezg.cn/Article/details/96844.sHtML
http://www.blog.hcbezg.cn/Article/details/36745.sHtML
http://www.blog.hcbezg.cn/Article/details/62273.sHtML
http://www.blog.hcbezg.cn/Article/details/53945.sHtML
http://www.blog.hcbezg.cn/Article/details/943818.sHtML
http://www.blog.hcbezg.cn/Article/details/8551.sHtML
http://www.blog.hcbezg.cn/Article/details/7447246.sHtML
http://www.blog.hcbezg.cn/Article/details/2416.sHtML
http://www.blog.hcbezg.cn/Article/details/3065620.sHtML
http://www.blog.hcbezg.cn/Article/details/3195709.sHtML
http://www.blog.hcbezg.cn/Article/details/89796.sHtML
http://www.blog.hcbezg.cn/Article/details/0612079.sHtML
http://www.blog.hcbezg.cn/Article/details/81151.sHtML
http://www.blog.hcbezg.cn/Article/details/967338.sHtML
http://www.blog.hcbezg.cn/Article/details/631218.sHtML
http://www.blog.hcbezg.cn/Article/details/08617.sHtML
http://www.blog.hcbezg.cn/Article/details/2511.sHtML
http://www.blog.hcbezg.cn/Article/details/5081063.sHtML
http://www.blog.hcbezg.cn/Article/details/8655527.sHtML
http://www.blog.hcbezg.cn/Article/details/338991.sHtML
http://www.blog.hcbezg.cn/Article/details/08520.sHtML
http://www.blog.hcbezg.cn/Article/details/537012.sHtML
http://www.blog.hcbezg.cn/Article/details/2339483.sHtML
http://www.blog.hcbezg.cn/Article/details/1070.sHtML
http://www.blog.hcbezg.cn/Article/details/2380692.sHtML
http://www.blog.hcbezg.cn/Article/details/40647.sHtML
http://www.blog.hcbezg.cn/Article/details/58638.sHtML
http://www.blog.hcbezg.cn/Article/details/1537089.sHtML
http://www.blog.hcbezg.cn/Article/details/0824484.sHtML
http://www.blog.hcbezg.cn/Article/details/0621808.sHtML
http://www.blog.hcbezg.cn/Article/details/5649.sHtML
http://www.blog.hcbezg.cn/Article/details/5632.sHtML
http://www.blog.hcbezg.cn/Article/details/71922.sHtML
http://www.blog.hcbezg.cn/Article/details/8150.sHtML
http://www.blog.hcbezg.cn/Article/details/0435.sHtML
http://www.blog.hcbezg.cn/Article/details/3288.sHtML
http://www.blog.hcbezg.cn/Article/details/25481.sHtML
http://www.blog.hcbezg.cn/Article/details/2222575.sHtML
http://www.blog.hcbezg.cn/Article/details/4864196.sHtML
http://www.blog.hcbezg.cn/Article/details/5204851.sHtML
http://www.blog.hcbezg.cn/Article/details/5530.sHtML
http://www.blog.hcbezg.cn/Article/details/902513.sHtML
http://www.blog.hcbezg.cn/Article/details/96755.sHtML
http://www.blog.hcbezg.cn/Article/details/9890285.sHtML
http://www.blog.hcbezg.cn/Article/details/739071.sHtML
http://www.blog.hcbezg.cn/Article/details/245302.sHtML
http://www.blog.hcbezg.cn/Article/details/29749.sHtML
http://www.blog.hcbezg.cn/Article/details/81182.sHtML
http://www.blog.hcbezg.cn/Article/details/4190356.sHtML
http://www.blog.hcbezg.cn/Article/details/425358.sHtML
http://www.blog.hcbezg.cn/Article/details/951718.sHtML
http://www.blog.hcbezg.cn/Article/details/0445.sHtML
http://www.blog.hcbezg.cn/Article/details/612259.sHtML
http://www.blog.hcbezg.cn/Article/details/409859.sHtML
http://www.blog.hcbezg.cn/Article/details/913992.sHtML
http://www.blog.hcbezg.cn/Article/details/2937.sHtML
http://www.blog.hcbezg.cn/Article/details/1736694.sHtML
http://www.blog.hcbezg.cn/Article/details/8210.sHtML
http://www.blog.hcbezg.cn/Article/details/5604.sHtML
http://www.blog.hcbezg.cn/Article/details/25804.sHtML
http://www.blog.hcbezg.cn/Article/details/61988.sHtML
http://www.blog.hcbezg.cn/Article/details/3091922.sHtML
http://www.blog.hcbezg.cn/Article/details/3851034.sHtML
http://www.blog.hcbezg.cn/Article/details/404813.sHtML
http://www.blog.hcbezg.cn/Article/details/8041.sHtML
http://www.blog.hcbezg.cn/Article/details/31036.sHtML
http://www.blog.hcbezg.cn/Article/details/102781.sHtML
http://www.blog.hcbezg.cn/Article/details/67094.sHtML
http://www.blog.hcbezg.cn/Article/details/2204934.sHtML
http://www.blog.hcbezg.cn/Article/details/7942.sHtML
http://www.blog.hcbezg.cn/Article/details/2092532.sHtML
http://www.blog.hcbezg.cn/Article/details/1831348.sHtML
http://www.blog.hcbezg.cn/Article/details/8353259.sHtML
http://www.blog.hcbezg.cn/Article/details/857263.sHtML
http://www.blog.hcbezg.cn/Article/details/5625192.sHtML
http://www.blog.hcbezg.cn/Article/details/6063.sHtML
http://www.blog.hcbezg.cn/Article/details/0888128.sHtML
http://www.blog.hcbezg.cn/Article/details/4247578.sHtML
http://www.blog.hcbezg.cn/Article/details/430472.sHtML
http://www.blog.hcbezg.cn/Article/details/231191.sHtML
http://www.blog.hcbezg.cn/Article/details/4785469.sHtML
http://www.blog.hcbezg.cn/Article/details/4960858.sHtML
http://www.blog.hcbezg.cn/Article/details/6366763.sHtML
http://www.blog.hcbezg.cn/Article/details/08009.sHtML
http://www.blog.hcbezg.cn/Article/details/4860673.sHtML
http://www.blog.hcbezg.cn/Article/details/6623.sHtML
http://www.blog.hcbezg.cn/Article/details/38164.sHtML
http://www.blog.hcbezg.cn/Article/details/0775.sHtML
http://www.blog.hcbezg.cn/Article/details/337074.sHtML
http://www.blog.hcbezg.cn/Article/details/3797.sHtML
http://www.blog.hcbezg.cn/Article/details/4404.sHtML
http://www.blog.hcbezg.cn/Article/details/013575.sHtML
http://www.blog.hcbezg.cn/Article/details/1957.sHtML
http://www.blog.hcbezg.cn/Article/details/5665588.sHtML
http://www.blog.hcbezg.cn/Article/details/88597.sHtML
http://www.blog.hcbezg.cn/Article/details/363370.sHtML
http://www.blog.hcbezg.cn/Article/details/45719.sHtML
http://www.blog.hcbezg.cn/Article/details/80265.sHtML
http://www.blog.hcbezg.cn/Article/details/380222.sHtML
http://www.blog.hcbezg.cn/Article/details/36834.sHtML
http://www.blog.hcbezg.cn/Article/details/1888.sHtML
http://www.blog.hcbezg.cn/Article/details/4357072.sHtML
http://www.blog.hcbezg.cn/Article/details/644823.sHtML
http://www.blog.hcbezg.cn/Article/details/9260.sHtML
http://www.blog.hcbezg.cn/Article/details/2815881.sHtML
http://www.blog.hcbezg.cn/Article/details/831739.sHtML
http://www.blog.hcbezg.cn/Article/details/1972.sHtML
http://www.blog.hcbezg.cn/Article/details/091712.sHtML
http://www.blog.hcbezg.cn/Article/details/093457.sHtML
http://www.blog.hcbezg.cn/Article/details/642587.sHtML
http://www.blog.hcbezg.cn/Article/details/350867.sHtML
http://www.blog.hcbezg.cn/Article/details/663207.sHtML
http://www.blog.hcbezg.cn/Article/details/652642.sHtML
http://www.blog.hcbezg.cn/Article/details/738669.sHtML
http://www.blog.hcbezg.cn/Article/details/5079719.sHtML
http://www.blog.hcbezg.cn/Article/details/3236.sHtML
http://www.blog.hcbezg.cn/Article/details/5494848.sHtML
http://www.blog.hcbezg.cn/Article/details/5865737.sHtML
http://www.blog.hcbezg.cn/Article/details/04697.sHtML
http://www.blog.hcbezg.cn/Article/details/6160.sHtML
http://www.blog.hcbezg.cn/Article/details/16889.sHtML
http://www.blog.hcbezg.cn/Article/details/970137.sHtML
http://www.blog.hcbezg.cn/Article/details/1916577.sHtML
http://www.blog.hcbezg.cn/Article/details/3505.sHtML
http://www.blog.hcbezg.cn/Article/details/8116771.sHtML
http://www.blog.hcbezg.cn/Article/details/3172.sHtML
http://www.blog.hcbezg.cn/Article/details/30101.sHtML
http://www.blog.hcbezg.cn/Article/details/59921.sHtML
http://www.blog.hcbezg.cn/Article/details/90918.sHtML
http://www.blog.hcbezg.cn/Article/details/8346167.sHtML
http://www.blog.hcbezg.cn/Article/details/6267315.sHtML
http://www.blog.hcbezg.cn/Article/details/035011.sHtML
http://www.blog.hcbezg.cn/Article/details/35330.sHtML
http://www.blog.hcbezg.cn/Article/details/4672.sHtML
http://www.blog.hcbezg.cn/Article/details/043452.sHtML
http://www.blog.hcbezg.cn/Article/details/7783936.sHtML
http://www.blog.hcbezg.cn/Article/details/54385.sHtML
http://www.blog.hcbezg.cn/Article/details/33884.sHtML
http://www.blog.hcbezg.cn/Article/details/41258.sHtML
http://www.blog.hcbezg.cn/Article/details/797457.sHtML
http://www.blog.hcbezg.cn/Article/details/1544.sHtML
http://www.blog.hcbezg.cn/Article/details/8496.sHtML
http://www.blog.hcbezg.cn/Article/details/2363236.sHtML
http://www.blog.hcbezg.cn/Article/details/25720.sHtML
http://www.blog.hcbezg.cn/Article/details/2841.sHtML
http://www.blog.hcbezg.cn/Article/details/8824761.sHtML
http://www.blog.hcbezg.cn/Article/details/4905812.sHtML
http://www.blog.hcbezg.cn/Article/details/3907.sHtML
http://www.blog.hcbezg.cn/Article/details/07380.sHtML
http://www.blog.hcbezg.cn/Article/details/3302394.sHtML
http://www.blog.hcbezg.cn/Article/details/3506.sHtML
http://www.blog.hcbezg.cn/Article/details/64647.sHtML
http://www.blog.hcbezg.cn/Article/details/503900.sHtML
http://www.blog.hcbezg.cn/Article/details/548883.sHtML
http://www.blog.hcbezg.cn/Article/details/8801852.sHtML
http://www.blog.hcbezg.cn/Article/details/812487.sHtML
http://www.blog.hcbezg.cn/Article/details/3829.sHtML
http://www.blog.hcbezg.cn/Article/details/0471837.sHtML
http://www.blog.hcbezg.cn/Article/details/6274097.sHtML
http://www.blog.hcbezg.cn/Article/details/727663.sHtML
http://www.blog.hcbezg.cn/Article/details/8991882.sHtML
http://www.blog.hcbezg.cn/Article/details/5039.sHtML
http://www.blog.hcbezg.cn/Article/details/7639.sHtML
http://www.blog.hcbezg.cn/Article/details/0496.sHtML
http://www.blog.hcbezg.cn/Article/details/4161.sHtML
http://www.blog.hcbezg.cn/Article/details/5873402.sHtML
http://www.blog.hcbezg.cn/Article/details/0619.sHtML
http://www.blog.hcbezg.cn/Article/details/78428.sHtML
http://www.blog.hcbezg.cn/Article/details/1801.sHtML
http://www.blog.hcbezg.cn/Article/details/2530.sHtML
http://www.blog.hcbezg.cn/Article/details/4296.sHtML
http://www.blog.hcbezg.cn/Article/details/45423.sHtML
http://www.blog.hcbezg.cn/Article/details/1176536.sHtML
http://www.blog.hcbezg.cn/Article/details/0945323.sHtML
http://www.blog.hcbezg.cn/Article/details/2392.sHtML
http://www.blog.hcbezg.cn/Article/details/82587.sHtML
http://www.blog.hcbezg.cn/Article/details/6891805.sHtML
http://www.blog.hcbezg.cn/Article/details/3181694.sHtML
http://www.blog.hcbezg.cn/Article/details/984608.sHtML
http://www.blog.hcbezg.cn/Article/details/5138090.sHtML
http://www.blog.hcbezg.cn/Article/details/50453.sHtML
http://www.blog.hcbezg.cn/Article/details/0696.sHtML
http://www.blog.hcbezg.cn/Article/details/34168.sHtML
http://www.blog.hcbezg.cn/Article/details/829034.sHtML
http://www.blog.hcbezg.cn/Article/details/742220.sHtML
http://www.blog.hcbezg.cn/Article/details/24098.sHtML
http://www.blog.hcbezg.cn/Article/details/6284376.sHtML
http://www.blog.hcbezg.cn/Article/details/670510.sHtML
http://www.blog.hcbezg.cn/Article/details/2320.sHtML
http://www.blog.hcbezg.cn/Article/details/5197056.sHtML
http://www.blog.hcbezg.cn/Article/details/7535410.sHtML
http://www.blog.hcbezg.cn/Article/details/924631.sHtML
http://www.blog.hcbezg.cn/Article/details/7186.sHtML
http://www.blog.hcbezg.cn/Article/details/3532.sHtML
http://www.blog.hcbezg.cn/Article/details/78631.sHtML
http://www.blog.hcbezg.cn/Article/details/6055730.sHtML
http://www.blog.hcbezg.cn/Article/details/393453.sHtML
http://www.blog.hcbezg.cn/Article/details/867441.sHtML
http://www.blog.hcbezg.cn/Article/details/544113.sHtML
http://www.blog.hcbezg.cn/Article/details/91003.sHtML

## 项目结构

```
webindex-core/
├── manage.py                 # 项目统一管理入口，包含 initdb、runserver 等命令
├── requirements.txt          # Python 生产环境依赖清单，锁定主要库版本
├── config/
│   ├── settings.py           # 主配置文件，包含数据库连接、缓存、ES 索引参数
│   ├── crawler_rules.yaml    # 爬虫规则配置，定义目标站点、请求间隔与解析模板
│   └── logging.conf          # 日志分级输出配置，按日切割并保留 30 天
├── core/
│   ├── __init__.py
│   ├── models.py             # SQLAlchemy 数据模型定义，包含 Resource、Tag、User 等表
│   ├── schema.py             # Pydantic 校验模型，用于 API 请求与响应的数据验证
│   ├── indexer.py            # Elasticsearch 索引管理模块，负责创建映射与重建索引
│   └── utils.py              # 通用工具函数，包含日期格式化、URL 规范化与哈希计算
├── crawler/
│   ├── __init__.py
│   ├── base.py               # 爬虫基类，定义 fetch、parse、save 抽象方法
│   ├── hcbezg_parser.py      # 针对 blog.hcbezg.cn 的专用解析器，提取标题、正文摘要与标签
│   └── scheduler.py          # 基于 APScheduler 的定时调度器，管理爬虫的执行周期
├── api/
│   ├── __init__.py
│   ├── v1/
│   │   ├── endpoints.py      # FastAPI 路由定义，包含资源 CRUD、检索与统计接口
│   │   ├── dependencies.py   # 依赖注入声明，包含数据库会话与身份认证校验
│   │   └── responses.py      # 统一响应结构封装，包含分页、错误码与数据封装
│   └── middleware.py         # 全局中间件，包含请求日志记录与跨域资源共享配置
├── frontend/                 # 管理后台前端源码（Vue 3 + Vite）
│   ├── index.html
│   ├── package.json
│   ├── src/
│   │   ├── main.js           # 应用入口，挂载根组件并注册全局路由
│   │   ├── App.vue           # 根组件，包含布局骨架与路由出口
│   │   ├── views/            # 页面级组件，包含仪表盘、资源列表、分类管理、系统设置
│   │   └── api/              # 封装的后端 API 调用模块，基于 Axios 实例
│   └── dist/                 # 前端构建产物目录，由 CI 流程自动生成
├── tests/
│   ├── unit/                 # 单元测试，覆盖模型方法、工具函数与解析器逻辑
│   ├── integration/          # 集成测试，验证数据库读写、ES 查询与 API 端到端流程
│   └── conftest.py           # pytest 全局夹具，包含测试数据库与测试客户端
├── scripts/
│   ├── backup.sh             # 数据库与索引备份脚本，配合 cron 每日执行
│   ├── restore.sh            # 从备份文件恢复数据的环境准备与执行脚本
│   └── migrate_tags.py       # 标签体系迁移工具，用于版本升级时的数据转换
├── docker/
│   ├── Dockerfile            # 基于 Python 3.10-slim 的生产镜像构建定义
│   ├── docker-compose.yml    # 本地开发环境编排，包含 PostgreSQL、ES、Redis 服务
│   └── nginx.conf            # 生产环境 Nginx 配置模板，包含 gzip 与静态缓存策略
└── README.md                 # 项目概览文档，即本文档
```

## 贡献指南

我们欢迎并鼓励社区开发者以多种形式参与 WebIndex Core 项目的改进与完善。请遵循以下步骤提交您的贡献：

1. 在 GitHub 上 fork 本仓库至您的个人账户，并 clone 到本地开发环境。确保您的开发环境满足安装要求章节中列出的所有依赖版本。

2. 创建新的功能分支，分支命名应遵循 `feature/描述` 或 `fix/描述` 的格式，描述部分使用英文简写。例如 `feature/add-rss-output` 或 `fix/parser-encoding-issue`。

3. 在提交代码之前，请确保所有单元测试和集成测试均通过，且新代码的测试覆盖率达到 80% 以上。运行 `pytest tests/` 命令进行全量测试验证。同时，请使用 `black` 和 `isort` 工具对 Python 代码进行格式化，使用 `eslint` 和 `prettier` 处理前端代码。

4. 提交 pull request 至本仓库的 main 分支，并在描述中清晰说明本次变更的目的、实现方式以及影响范围。如果本次提交解决了某个已记录的 issue，请使用 `Closes #issue编号` 的语法进行关联。

5. 项目维护者将在 7 个工作日内对 pull request 进行 review，可能会提出修改意见。请保持关注并及时响应。合并后，您的贡献将被列入项目贡献者列表。

## 常见问题

**问：系统可以同时管理多个不同来源的博客吗？**

可以。系统设计上支持配置多个独立的爬虫规则，每个规则可指定不同的域名、路径匹配模式和解析模板。您可以在 `config/crawler_rules.yaml` 文件中新增条目，并指定对应的解析器类。系统调度器会按照每个规则独立配置的间隔时间执行抓取任务。

**问：如果目标文章页面结构发生变化，导致解析失败怎么办？**

系统内置了异常捕获与重试机制。当解析器遇到预期外的 HTML 结构时，会记录错误日志并将该任务标记为失败状态，在下一个调度周期会自动重试。如果连续失败超过三次，系统会将该 URL 置入待人工审核队列，并通过管理后台的告警面板进行提示。管理员可以在后台手动编辑资源的元数据，或调整解析器的选择器配置后重新触发抓取。

**问：如何将现有系统中的资源数据迁移到 WebIndex Core？**

系统提供了一组导入命令，支持从 CSV、JSON Lines 和 OPML 格式的文件中批量导入资源数据。您需要按照导入模板的字段要求准备数据文件，然后执行 `python manage.py import --format csv --file resources.csv` 命令。对于大型数据集（超过 1 万条），建议使用 `--batch-size` 参数控制分批导入的数量，以避免数据库事务超时。详细的字段映射说明请参考 `docs/import-export.md` 文档。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:26:28
