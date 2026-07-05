# TechBlog Archive Bridge

TechBlog Archive Bridge 是一个面向技术研究人员、开发者和内容聚合者的轻量级博文索引与导航工具。该项目不对原始内容做任何二次加工或转载，而是以结构化目录和快速检索的方式，将散落在技术博客站点中的历史文章进行系统性归集，帮助用户在海量技术笔记中快速定位到具体主题的讨论、代码示例或故障排查记录。

项目定位为“技术博文外链索引站”，不存储任何文章正文或图片，仅保留原始链接及元信息。目标用户包括需要查阅旧版技术方案实现细节的工程师、进行技术史资料整理的研究人员，以及希望从大量博文中筛选有效信息的初学者。通过本项目的目录索引和关键词映射，用户可以绕过站点内部搜索功能的局限，直接访问到对应文章页面。

## 功能概览

**按主题分类索引**：所有收录链接按文章内容涉及的技术领域、语言框架或问题类型进行一级分类，便于用户按方向浏览。

**原始链接直出**：每个条目保留原始 URL 的完整路径、文件名和扩展名，不做任何重定向、缩短或协议转换，确保链接可被脚本批量处理。

**批量导入与增量更新**：支持通过 CSV 或 JSON 格式批量导入新链接，并自动合并至现有索引结构中，适合持续维护的大规模资源池。

**多级标签过滤**：每条记录附带多个标签（如“数据库”、“性能优化”、“前端工程化”），支持组合筛选，缩小检索范围。

**全文标题检索**：基于文章标题和摘要片段提供简单的关键词匹配检索，无需依赖外部搜索引擎即可快速定位。

**链接可用性检查**：内置基本的 HTTP 状态码检测模块，可标记失效链接并生成报告，方便维护者定期清理。

**导出为 Markdown 列表**：支持将当前索引内容按指定分类导出为 Markdown 格式的无序列表，便于嵌入其他文档或 Wiki。

**命令行交互界面**：提供轻量级的 CLI 工具，支持查询、添加、删除和导出操作，无需图形界面即可完成日常维护。

## 应用场景

**技术文档撰写时的参考资料查找**：当开发者撰写技术方案或故障复盘报告时，可以通过本项目的分类索引快速找到与特定报错码或配置参数相关的历史博文，作为技术决策的参考依据。

**遗留系统维护中的问题定位**：维护老旧系统的工程师经常需要查阅数年前的技术讨论。本项目索引了大量历史文章，涵盖已被现代框架取代的旧版本库的使用细节，帮助维护者理解原始设计意图。

**技术博客站点的流量引导**：对于运营技术博客的团队，可以将本站作为外链引流渠道之一。通过将散落的文章链接集中展示，降低新访客的内容发现成本，提升长尾文章的曝光率。

**数据备份前的链接归档**：在备份个人技术笔记或公司知识库时，可以使用本项目的导出功能生成完整的链接清单，配合 wget 或 curl 脚本进行批量存档。

## 快速开始

以下命令演示如何从代码仓库克隆项目、安装依赖并启动本地索引服务。

```bash
git clone https://github.com/techblog-archive/archive-bridge.git
cd archive-bridge
pip install -r requirements.txt
python cli.py serve --port 8080
```

执行上述命令后，CLI 服务将在本地的 8080 端口启动，提供基础的索引查询接口。如需导入初始数据，请将 URL 列表保存为 `links.txt` 后执行：

```bash
python cli.py import --file links.txt --category techblog
```

## 安装要求

| 依赖组件 | 必需版本 | 说明 |
|---|---|---|
| Python | 3.8 及以上 | 核心运行环境，用于 CLI 工具和 HTTP 服务 |
| pip | 20.0 及以上 | Python 包管理工具，用于安装依赖库 |
| requests | 2.25.0 及以上 | 用于发送 HTTP 请求以检查链接可用性 |
| click | 8.0.0 及以上 | CLI 命令行交互框架，提供子命令解析能力 |
| flask | 2.0.0 及以上 | 可选依赖，仅在启动 Web 可视化界面时需要 |
| pytest | 6.0.0 及以上 | 开发测试依赖，运行单元测试时使用 |
| black | 22.0.0 及以上 | 代码格式化工具，仅开发阶段使用 |
| mypy | 0.900 及以上 | 静态类型检查工具，仅开发阶段使用 |

## 文档导航

| 层面 | 目录/文档 | 回答的问题 |
|---|---|---|
| 入门指南 | docs/quickstart.md | 如何在一分钟内启动本地服务并导入第一批链接；首次使用的推荐工作流 |
| 索引规范 | docs/indexing-schema.md | 链接的元数据字段定义、分类标签命名规则以及 JSON 导入格式说明 |
| 维护手册 | docs/maintenance.md | 如何批量更新链接状态、处理失效链接以及生成可用性报告 |
| 开发参考 | docs/development.md | 项目的代码组织结构、新增 CLI 命令的方法以及提交 PR 的流程要求 |

## 资源列表

基础技术文章索引

http://www.blog.jnjpgf.cn/Article/details/5079736.sHtML
http://www.blog.jnjpgf.cn/Article/details/54169.sHtML
http://www.blog.jnjpgf.cn/Article/details/46602.sHtML
http://www.blog.jnjpgf.cn/Article/details/8774.sHtML
http://www.blog.jnjpgf.cn/Article/details/8959101.sHtML
http://www.blog.jnjpgf.cn/Article/details/428579.sHtML
http://www.blog.jnjpgf.cn/Article/details/527514.sHtML
http://www.blog.jnjpgf.cn/Article/details/517672.sHtML
http://www.blog.jnjpgf.cn/Article/details/66893.sHtML
http://www.blog.jnjpgf.cn/Article/details/9684.sHtML
http://www.blog.jnjpgf.cn/Article/details/689884.sHtML
http://www.blog.jnjpgf.cn/Article/details/2245.sHtML
http://www.blog.jnjpgf.cn/Article/details/083918.sHtML
http://www.blog.jnjpgf.cn/Article/details/6544592.sHtML
http://www.blog.jnjpgf.cn/Article/details/7406612.sHtML
http://www.blog.jnjpgf.cn/Article/details/80899.sHtML
http://www.blog.jnjpgf.cn/Article/details/82538.sHtML
http://www.blog.jnjpgf.cn/Article/details/852397.sHtML
http://www.blog.jnjpgf.cn/Article/details/90790.sHtML
http://www.blog.jnjpgf.cn/Article/details/3251119.sHtML
http://www.blog.jnjpgf.cn/Article/details/03825.sHtML
http://www.blog.jnjpgf.cn/Article/details/305461.sHtML
http://www.blog.jnjpgf.cn/Article/details/1590278.sHtML
http://www.blog.jnjpgf.cn/Article/details/22056.sHtML
http://www.blog.jnjpgf.cn/Article/details/53689.sHtML
http://www.blog.jnjpgf.cn/Article/details/0583.sHtML
http://www.blog.jnjpgf.cn/Article/details/84104.sHtML
http://www.blog.jnjpgf.cn/Article/details/8167608.sHtML
http://www.blog.jnjpgf.cn/Article/details/9500.sHtML
http://www.blog.jnjpgf.cn/Article/details/5686088.sHtML
http://www.blog.jnjpgf.cn/Article/details/9912286.sHtML
http://www.blog.jnjpgf.cn/Article/details/8571.sHtML
http://www.blog.jnjpgf.cn/Article/details/6092012.sHtML
http://www.blog.jnjpgf.cn/Article/details/8362.sHtML
http://www.blog.jnjpgf.cn/Article/details/3458906.sHtML
http://www.blog.jnjpgf.cn/Article/details/4610.sHtML
http://www.blog.jnjpgf.cn/Article/details/57486.sHtML
http://www.blog.jnjpgf.cn/Article/details/6472.sHtML
http://www.blog.jnjpgf.cn/Article/details/09543.sHtML
http://www.blog.jnjpgf.cn/Article/details/4512.sHtML
http://www.blog.jnjpgf.cn/Article/details/454590.sHtML
http://www.blog.jnjpgf.cn/Article/details/6036.sHtML
http://www.blog.jnjpgf.cn/Article/details/4387.sHtML
http://www.blog.jnjpgf.cn/Article/details/5124063.sHtML
http://www.blog.jnjpgf.cn/Article/details/886171.sHtML
http://www.blog.jnjpgf.cn/Article/details/9699548.sHtML
http://www.blog.jnjpgf.cn/Article/details/6417908.sHtML
http://www.blog.jnjpgf.cn/Article/details/89507.sHtML
http://www.blog.jnjpgf.cn/Article/details/1714.sHtML
http://www.blog.jnjpgf.cn/Article/details/9085285.sHtML
http://www.blog.jnjpgf.cn/Article/details/17588.sHtML
http://www.blog.jnjpgf.cn/Article/details/3127.sHtML
http://www.blog.jnjpgf.cn/Article/details/4351497.sHtML
http://www.blog.jnjpgf.cn/Article/details/854732.sHtML
http://www.blog.jnjpgf.cn/Article/details/7881.sHtML
http://www.blog.jnjpgf.cn/Article/details/8851.sHtML
http://www.blog.jnjpgf.cn/Article/details/9474.sHtML
http://www.blog.jnjpgf.cn/Article/details/0961.sHtML
http://www.blog.jnjpgf.cn/Article/details/4429.sHtML
http://www.blog.jnjpgf.cn/Article/details/73888.sHtML
http://www.blog.jnjpgf.cn/Article/details/756400.sHtML
http://www.blog.jnjpgf.cn/Article/details/052676.sHtML
http://www.blog.jnjpgf.cn/Article/details/951529.sHtML
http://www.blog.jnjpgf.cn/Article/details/920831.sHtML
http://www.blog.jnjpgf.cn/Article/details/4826.sHtML
http://www.blog.jnjpgf.cn/Article/details/09029.sHtML
http://www.blog.jnjpgf.cn/Article/details/3416.sHtML
http://www.blog.jnjpgf.cn/Article/details/553830.sHtML
http://www.blog.jnjpgf.cn/Article/details/518106.sHtML
http://www.blog.jnjpgf.cn/Article/details/926410.sHtML
http://www.blog.jnjpgf.cn/Article/details/540350.sHtML
http://www.blog.jnjpgf.cn/Article/details/5791.sHtML
http://www.blog.jnjpgf.cn/Article/details/1973.sHtML
http://www.blog.jnjpgf.cn/Article/details/6688457.sHtML
http://www.blog.jnjpgf.cn/Article/details/1660648.sHtML
http://www.blog.jnjpgf.cn/Article/details/7071.sHtML
http://www.blog.jnjpgf.cn/Article/details/34077.sHtML
http://www.blog.jnjpgf.cn/Article/details/9804.sHtML
http://www.blog.jnjpgf.cn/Article/details/252488.sHtML
http://www.blog.jnjpgf.cn/Article/details/1127425.sHtML
http://www.blog.jnjpgf.cn/Article/details/408492.sHtML
http://www.blog.jnjpgf.cn/Article/details/256278.sHtML
http://www.blog.jnjpgf.cn/Article/details/25884.sHtML
http://www.blog.jnjpgf.cn/Article/details/7955.sHtML
http://www.blog.jnjpgf.cn/Article/details/4566787.sHtML
http://www.blog.jnjpgf.cn/Article/details/3557220.sHtML
http://www.blog.jnjpgf.cn/Article/details/3562582.sHtML
http://www.blog.jnjpgf.cn/Article/details/7487.sHtML
http://www.blog.jnjpgf.cn/Article/details/991096.sHtML
http://www.blog.jnjpgf.cn/Article/details/466579.sHtML
http://www.blog.jnjpgf.cn/Article/details/97446.sHtML
http://www.blog.jnjpgf.cn/Article/details/804306.sHtML
http://www.blog.jnjpgf.cn/Article/details/85805.sHtML
http://www.blog.jnjpgf.cn/Article/details/238549.sHtML
http://www.blog.jnjpgf.cn/Article/details/819011.sHtML
http://www.blog.jnjpgf.cn/Article/details/8803729.sHtML
http://www.blog.jnjpgf.cn/Article/details/4532.sHtML
http://www.blog.jnjpgf.cn/Article/details/7559045.sHtML
http://www.blog.jnjpgf.cn/Article/details/705932.sHtML
http://www.blog.jnjpgf.cn/Article/details/5056828.sHtML
http://www.blog.jnjpgf.cn/Article/details/72628.sHtML
http://www.blog.jnjpgf.cn/Article/details/0861.sHtML
http://www.blog.jnjpgf.cn/Article/details/4148.sHtML
http://www.blog.jnjpgf.cn/Article/details/100330.sHtML
http://www.blog.jnjpgf.cn/Article/details/9955.sHtML
http://www.blog.jnjpgf.cn/Article/details/3943.sHtML
http://www.blog.jnjpgf.cn/Article/details/5297405.sHtML
http://www.blog.jnjpgf.cn/Article/details/4020756.sHtML
http://www.blog.jnjpgf.cn/Article/details/099830.sHtML
http://www.blog.jnjpgf.cn/Article/details/5608.sHtML
http://www.blog.jnjpgf.cn/Article/details/6496579.sHtML
http://www.blog.jnjpgf.cn/Article/details/8014580.sHtML
http://www.blog.jnjpgf.cn/Article/details/859356.sHtML
http://www.blog.jnjpgf.cn/Article/details/22270.sHtML
http://www.blog.jnjpgf.cn/Article/details/2414.sHtML
http://www.blog.jnjpgf.cn/Article/details/561073.sHtML
http://www.blog.jnjpgf.cn/Article/details/98306.sHtML
http://www.blog.jnjpgf.cn/Article/details/832306.sHtML
http://www.blog.jnjpgf.cn/Article/details/4869.sHtML
http://www.blog.jnjpgf.cn/Article/details/455302.sHtML
http://www.blog.jnjpgf.cn/Article/details/1335964.sHtML
http://www.blog.jnjpgf.cn/Article/details/1451.sHtML
http://www.blog.jnjpgf.cn/Article/details/586160.sHtML
http://www.blog.jnjpgf.cn/Article/details/5482.sHtML
http://www.blog.jnjpgf.cn/Article/details/217407.sHtML
http://www.blog.jnjpgf.cn/Article/details/17999.sHtML
http://www.blog.jnjpgf.cn/Article/details/1787586.sHtML
http://www.blog.jnjpgf.cn/Article/details/994015.sHtML
http://www.blog.jnjpgf.cn/Article/details/61026.sHtML
http://www.blog.jnjpgf.cn/Article/details/330344.sHtML
http://www.blog.jnjpgf.cn/Article/details/1211962.sHtML
http://www.blog.jnjpgf.cn/Article/details/0604.sHtML
http://www.blog.jnjpgf.cn/Article/details/797966.sHtML
http://www.blog.jnjpgf.cn/Article/details/0375310.sHtML
http://www.blog.jnjpgf.cn/Article/details/543558.sHtML
http://www.blog.jnjpgf.cn/Article/details/375739.sHtML
http://www.blog.jnjpgf.cn/Article/details/26728.sHtML
http://www.blog.jnjpgf.cn/Article/details/4119.sHtML
http://www.blog.jnjpgf.cn/Article/details/343452.sHtML
http://www.blog.jnjpgf.cn/Article/details/096255.sHtML
http://www.blog.jnjpgf.cn/Article/details/80343.sHtML
http://www.blog.jnjpgf.cn/Article/details/495202.sHtML
http://www.blog.jnjpgf.cn/Article/details/08378.sHtML
http://www.blog.jnjpgf.cn/Article/details/643665.sHtML
http://www.blog.jnjpgf.cn/Article/details/54568.sHtML
http://www.blog.jnjpgf.cn/Article/details/8752618.sHtML
http://www.blog.jnjpgf.cn/Article/details/2918390.sHtML
http://www.blog.jnjpgf.cn/Article/details/0935.sHtML
http://www.blog.jnjpgf.cn/Article/details/0658328.sHtML
http://www.blog.jnjpgf.cn/Article/details/12809.sHtML
http://www.blog.jnjpgf.cn/Article/details/1822835.sHtML
http://www.blog.jnjpgf.cn/Article/details/9862.sHtML
http://www.blog.jnjpgf.cn/Article/details/1281507.sHtML
http://www.blog.jnjpgf.cn/Article/details/660829.sHtML
http://www.blog.jnjpgf.cn/Article/details/70179.sHtML
http://www.blog.jnjpgf.cn/Article/details/35551.sHtML
http://www.blog.jnjpgf.cn/Article/details/5844732.sHtML
http://www.blog.jnjpgf.cn/Article/details/741468.sHtML
http://www.blog.jnjpgf.cn/Article/details/8448.sHtML
http://www.blog.jnjpgf.cn/Article/details/0049.sHtML
http://www.blog.jnjpgf.cn/Article/details/0866.sHtML
http://www.blog.jnjpgf.cn/Article/details/18237.sHtML
http://www.blog.jnjpgf.cn/Article/details/1614.sHtML
http://www.blog.jnjpgf.cn/Article/details/753609.sHtML
http://www.blog.jnjpgf.cn/Article/details/13389.sHtML
http://www.blog.jnjpgf.cn/Article/details/1295207.sHtML
http://www.blog.jnjpgf.cn/Article/details/8927242.sHtML
http://www.blog.jnjpgf.cn/Article/details/95348.sHtML
http://www.blog.jnjpgf.cn/Article/details/23116.sHtML
http://www.blog.jnjpgf.cn/Article/details/551011.sHtML
http://www.blog.jnjpgf.cn/Article/details/4703619.sHtML
http://www.blog.jnjpgf.cn/Article/details/85595.sHtML
http://www.blog.jnjpgf.cn/Article/details/5135.sHtML
http://www.blog.jnjpgf.cn/Article/details/7783640.sHtML
http://www.blog.jnjpgf.cn/Article/details/52279.sHtML
http://www.blog.jnjpgf.cn/Article/details/92763.sHtML
http://www.blog.jnjpgf.cn/Article/details/2942.sHtML
http://www.blog.jnjpgf.cn/Article/details/579930.sHtML
http://www.blog.jnjpgf.cn/Article/details/080696.sHtML
http://www.blog.jnjpgf.cn/Article/details/2043952.sHtML
http://www.blog.jnjpgf.cn/Article/details/8570483.sHtML
http://www.blog.jnjpgf.cn/Article/details/7421.sHtML
http://www.blog.jnjpgf.cn/Article/details/35091.sHtML
http://www.blog.jnjpgf.cn/Article/details/28991.sHtML
http://www.blog.jnjpgf.cn/Article/details/0221221.sHtML
http://www.blog.jnjpgf.cn/Article/details/6882.sHtML
http://www.blog.jnjpgf.cn/Article/details/793776.sHtML
http://www.blog.jnjpgf.cn/Article/details/140456.sHtML
http://www.blog.jnjpgf.cn/Article/details/06146.sHtML
http://www.blog.jnjpgf.cn/Article/details/152776.sHtML
http://www.blog.jnjpgf.cn/Article/details/322534.sHtML
http://www.blog.jnjpgf.cn/Article/details/0530878.sHtML
http://www.blog.jnjpgf.cn/Article/details/8189.sHtML
http://www.blog.jnjpgf.cn/Article/details/8505.sHtML
http://www.blog.jnjpgf.cn/Article/details/2985.sHtML
http://www.blog.jnjpgf.cn/Article/details/15058.sHtML
http://www.blog.jnjpgf.cn/Article/details/31483.sHtML
http://www.blog.jnjpgf.cn/Article/details/5206888.sHtML
http://www.blog.jnjpgf.cn/Article/details/278531.sHtML
http://www.blog.jnjpgf.cn/Article/details/79384.sHtML
http://www.blog.jnjpgf.cn/Article/details/987894.sHtML
http://www.blog.jnjpgf.cn/Article/details/8223993.sHtML
http://www.blog.jnjpgf.cn/Article/details/1185471.sHtML
http://www.blog.jnjpgf.cn/Article/details/701722.sHtML
http://www.blog.jnjpgf.cn/Article/details/2157123.sHtML
http://www.blog.jnjpgf.cn/Article/details/70847.sHtML
http://www.blog.jnjpgf.cn/Article/details/3124782.sHtML
http://www.blog.jnjpgf.cn/Article/details/177529.sHtML
http://www.blog.jnjpgf.cn/Article/details/8889220.sHtML
http://www.blog.jnjpgf.cn/Article/details/862403.sHtML
http://www.blog.jnjpgf.cn/Article/details/1888.sHtML
http://www.blog.jnjpgf.cn/Article/details/7505.sHtML
http://www.blog.jnjpgf.cn/Article/details/1758.sHtML
http://www.blog.jnjpgf.cn/Article/details/41446.sHtML
http://www.blog.jnjpgf.cn/Article/details/5129.sHtML
http://www.blog.jnjpgf.cn/Article/details/630566.sHtML
http://www.blog.jnjpgf.cn/Article/details/40053.sHtML
http://www.blog.jnjpgf.cn/Article/details/0000.sHtML
http://www.blog.jnjpgf.cn/Article/details/3429.sHtML
http://www.blog.jnjpgf.cn/Article/details/054449.sHtML
http://www.blog.jnjpgf.cn/Article/details/5830233.sHtML
http://www.blog.jnjpgf.cn/Article/details/1851392.sHtML
http://www.blog.jnjpgf.cn/Article/details/0190.sHtML
http://www.blog.jnjpgf.cn/Article/details/764646.sHtML
http://www.blog.jnjpgf.cn/Article/details/4083.sHtML
http://www.blog.jnjpgf.cn/Article/details/56589.sHtML
http://www.blog.jnjpgf.cn/Article/details/02680.sHtML
http://www.blog.jnjpgf.cn/Article/details/0146.sHtML
http://www.blog.jnjpgf.cn/Article/details/979552.sHtML
http://www.blog.jnjpgf.cn/Article/details/75853.sHtML
http://www.blog.jnjpgf.cn/Article/details/5116017.sHtML
http://www.blog.jnjpgf.cn/Article/details/5877253.sHtML
http://www.blog.jnjpgf.cn/Article/details/7405895.sHtML
http://www.blog.jnjpgf.cn/Article/details/5756.sHtML
http://www.blog.jnjpgf.cn/Article/details/61749.sHtML
http://www.blog.jnjpgf.cn/Article/details/27428.sHtML
http://www.blog.jnjpgf.cn/Article/details/7552606.sHtML
http://www.blog.jnjpgf.cn/Article/details/76171.sHtML
http://www.blog.jnjpgf.cn/Article/details/8813.sHtML
http://www.blog.jnjpgf.cn/Article/details/156952.sHtML
http://www.blog.jnjpgf.cn/Article/details/0660635.sHtML
http://www.blog.jnjpgf.cn/Article/details/023619.sHtML
http://www.blog.jnjpgf.cn/Article/details/0341666.sHtML
http://www.blog.jnjpgf.cn/Article/details/5091.sHtML
http://www.blog.jnjpgf.cn/Article/details/5149094.sHtML
http://www.blog.jnjpgf.cn/Article/details/6791.sHtML
http://www.blog.jnjpgf.cn/Article/details/062771.sHtML
http://www.blog.jnjpgf.cn/Article/details/6185968.sHtML
http://www.blog.jnjpgf.cn/Article/details/2681452.sHtML
http://www.blog.jnjpgf.cn/Article/details/9493002.sHtML

## 项目结构

```
archive-bridge/
├── cli.py                      # CLI 入口，注册所有子命令
├── requirements.txt            # 生产环境依赖列表
├── setup.py                    # 项目打包与安装配置
├── src/                        # 核心源代码目录
│   ├── __init__.py             # 包初始化
│   ├── importer.py             # 链接导入模块，支持 CSV/JSON 解析
│   ├── indexer.py              # 索引构建与内存存储管理
│   ├── checker.py              # 链接可用性检查，并发 HTTP 请求
│   ├── exporter.py             # 导出为 Markdown 列表或 JSON
│   └── server.py               # Flask Web 界面启动入口
├── tests/                      # 单元测试目录
│   ├── test_importer.py        # 导入功能测试用例
│   ├── test_indexer.py         # 索引增删改查测试
│   └── test_checker.py         # 链接检查模块的模拟测试
├── docs/                       # 文档目录
│   ├── quickstart.md           # 快速入门指南
│   ├── indexing-schema.md      # 索引字段与分类规范
│   ├── maintenance.md          # 维护与更新流程
│   └── development.md          # 开发环境搭建与 PR 流程
├── data/                       # 数据存储目录
│   ├── links.json              # 主索引数据文件，JSON 格式
│   └── categories.json         # 分类与标签映射表
└── scripts/                    # 辅助运维脚本
    ├── daily_check.sh          # 每日链接可用性检查定时脚本
    └── import_batch.py         # 批量导入工具，支持从文本文件读取 URL
```

## 贡献指南

1. 在 GitHub 上 fork 本仓库，并 clone 到本地开发环境。请确保本地 Python 版本不低于 3.8，并安装所有开发依赖。

2. 新增链接索引时，请先阅读 `docs/indexing-schema.md` 中的字段定义，按规范填写文章标题、分类标签和原始 URL。提交前运行 `pytest` 确保所有现有测试用例通过。

3. 若需要新增分类或调整标签体系，请同步更新 `data/categories.json` 文件，并在 PR 描述中说明改动理由和影响范围。

4. 提交 Pull Request 时，请将目标分支指向 `develop`，并在 PR 正文中附上本次改动的测试结果截图或日志。合并前至少需要一位项目维护者的审核批准。

5. 对于文档类修改（如修正错别字、补充示例），可直接提交 PR 到 `main` 分支，但需在标题中注明 `[doc]` 前缀以便分类。

## 常见问题

Q: 索引中部分链接无法访问，应该如何处理？

A: 项目内置了链接可用性检查命令 `python cli.py check --report`。运行后会生成一份失效链接清单。对于确认失效的链接，建议先尝试在原始站点内搜索相同标题的文章；若确认内容已彻底移除，可以通过 `python cli.py remove --url <URL>` 从索引中删除该条目。

Q: 能否将本项目的索引数据迁移到其他知识库工具中？

A: 可以。项目支持导出为多种格式。通过 `python cli.py export --format json` 可获取完整的结构化数据；使用 `--format markdown` 则生成纯文本列表，便于复制到任何支持 Markdown 的编辑器或 Wiki 系统中。

Q: 项目是否会对原始文章内容进行缓存或存储？

A: 不会。本项目仅存储文章标题、分类标签和原始 URL 字符串，不请求、不解析、不存储文章正文、图片或附件。所有访问请求均在用户点击链接时由浏览器直接发往原始服务器。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:29:36
