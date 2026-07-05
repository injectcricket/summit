# TechLink Navigator

TechLink Navigator 是一个面向开发者与技术研究人员的开源技术资源外链聚合平台，旨在系统性地收集、分类与索引高质量的外部技术文章、教程与工程实践文档。该项目不生产内容，而是作为技术知识的中转枢纽，帮助用户快速定位到特定主题下的优质外部资源，减少信息检索与过滤的时间成本。

项目定位为轻量级、纯静态的技术导航站点，核心功能围绕 URL 的归集、展示与检索展开，适用于个人知识管理、团队技术文档索引、开源项目外部参考链接整理等多种场景。所有外链数据基于纯文本格式存储，支持通过脚本批量导入、导出与校验，便于版本控制与协作维护。

## 功能概览

**批量外链导入**：支持从 CSV、JSON 及纯文本列表批量导入 URL 数据，自动去重并校验 URL 可访问性。

**多级分类索引**：外链可按技术领域、文章类型、来源站点等维度进行多级分类，支持自定义标签与分类树。

**全文检索与筛选**：基于标题、描述、标签及 URL 关键词的轻量级全文检索，支持按分类与标签组合筛选。

**外部资源快照预览**：对已收录的外链生成页面标题与摘要的快照缓存，在链接失效时仍可查看基础元数据。

**链接健康状态监控**：定期对已收录 URL 进行可用性检查，标记失效链接并生成报告，便于维护者及时更新。

**静态站点生成**：基于收录数据一键生成完整的静态 HTML 导航站点，可直接部署至 GitHub Pages、Cloudflare Pages 或任何 Web 服务器。

**数据导出与备份**：支持将全量外链数据导出为 CSV、JSON 或 Markdown 表格格式，便于迁移与二次处理。

**访问统计与热度排序**：记录各外链的点击次数，支持按热度排序展示，帮助用户发现高频访问的资源。

## 应用场景

**技术团队内部知识库索引**：技术团队可将日常阅读的优质技术文章、官方文档、调试笔记等外链统一收录至 TechLink Navigator，作为团队知识库的外部参考索引，新成员可快速了解团队关注的技术栈与学习路径。

**开源项目的参考链接附录**：开源项目维护者可将项目依赖的参考资料、设计文档出处、相关标准规范等外链通过 TechLink Navigator 进行管理，生成结构化的参考链接附录，便于贡献者追溯设计决策依据。

**个人开发者的学习路径管理**：个人开发者可将日常学习的教程、API 手册、案例代码等外链按学习主题分类收藏，配合检索功能快速回顾之前学习的内容，形成个人化的技术学习知识图谱。

**技术社区资源聚合导航站**：技术社区或博客平台可基于 TechLink Navigator 搭建垂直领域的资源导航站，将社区内产生的优质内容与外部参考资料整合展示，提升社区内容资产的可发现性。

## 快速开始

以下命令可在本地快速启动 TechLink Navigator 的开发实例，用于数据导入、分类管理与站点预览。

```bash
# 克隆项目仓库至本地
git clone https://github.com/techlink-navigator/techlink-navigator.git

# 进入项目根目录并安装依赖
cd techlink-navigator
pip install -r requirements.txt

# 执行数据初始化与开发服务器启动
python manage.py init --import-demo
python manage.py runserver --host 127.0.0.1 --port 8080
```

执行完成后，访问 http://127.0.0.1:8080 即可进入本地的导航站点管理界面，默认包含约 250 条示例外链数据用于功能演示。

## 安装要求

| 依赖组件 | 必需版本 | 说明 |
|---|---|---|
| Python | 3.9 及以上 | 核心运行环境，用于数据处理与站点生成 |
| pip | 22.0 及以上 | Python 包依赖管理工具 |
| SQLite | 3.35 及以上 | 内置轻量级数据库，用于外链元数据存储 |
| Git | 2.25 及以上 | 版本控制，用于克隆仓库与贡献同步 |
| Node.js | 18.0 及以上 | 仅用于静态站点的前端资源构建（可选） |
| curl | 7.68 及以上 | 用于外链健康状态监控的请求探测（可选） |
| cron | 系统自带 | 用于定时执行链接健康检查任务（生产部署推荐） |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|---|---|---|
| 用户指南 | docs/user-guide/ | 如何导入外链、如何分类管理、如何生成静态站点 |
| 维护手册 | docs/maintainer-guide/ | 如何进行链接健康检查、如何更新失效链接、如何备份数据 |
| 开发者文档 | docs/developer-guide/ | 项目架构说明、API 接口定义、如何二次开发与扩展 |
| 部署参考 | docs/deployment/ | 如何部署至 GitHub Pages、Cloudflare Pages、VPS 或容器环境 |
| 数据格式规范 | docs/data-spec/ | CSV/JSON 导入导出字段定义、分类标签命名规范 |
| 贡献流程 | docs/contributing/ | 外链贡献审核流程、分类建议模板、PR 提交规范 |

## 资源列表

本批次收录的外链全部来自以下来源，按原始格式原样列出。

技术文章与教程类：

http://www.blog.puhvjy.cn/Article/details/370221.sHtML
http://www.blog.puhvjy.cn/Article/details/081572.sHtML
http://www.blog.puhvjy.cn/Article/details/6342309.sHtML
http://www.blog.puhvjy.cn/Article/details/7908179.sHtML
http://www.blog.puhvjy.cn/Article/details/446246.sHtML
http://www.blog.puhvjy.cn/Article/details/0047789.sHtML
http://www.blog.puhvjy.cn/Article/details/7562316.sHtML
http://www.blog.puhvjy.cn/Article/details/733153.sHtML
http://www.blog.puhvjy.cn/Article/details/421774.sHtML
http://www.blog.puhvjy.cn/Article/details/0956509.sHtML
http://www.blog.puhvjy.cn/Article/details/7307.sHtML
http://www.blog.puhvjy.cn/Article/details/1158184.sHtML
http://www.blog.puhvjy.cn/Article/details/69689.sHtML
http://www.blog.puhvjy.cn/Article/details/397732.sHtML
http://www.blog.puhvjy.cn/Article/details/4846734.sHtML
http://www.blog.puhvjy.cn/Article/details/6406180.sHtML
http://www.blog.puhvjy.cn/Article/details/087443.sHtML
http://www.blog.puhvjy.cn/Article/details/34467.sHtML
http://www.blog.puhvjy.cn/Article/details/0806482.sHtML
http://www.blog.puhvjy.cn/Article/details/2403.sHtML
http://www.blog.puhvjy.cn/Article/details/9462473.sHtML
http://www.blog.puhvjy.cn/Article/details/9990767.sHtML
http://www.blog.puhvjy.cn/Article/details/90037.sHtML
http://www.blog.puhvjy.cn/Article/details/013137.sHtML
http://www.blog.puhvjy.cn/Article/details/7986.sHtML
http://www.blog.puhvjy.cn/Article/details/8837.sHtML
http://www.blog.puhvjy.cn/Article/details/69122.sHtML
http://www.blog.puhvjy.cn/Article/details/4674455.sHtML
http://www.blog.puhvjy.cn/Article/details/5809526.sHtML
http://www.blog.puhvjy.cn/Article/details/7669324.sHtML
http://www.blog.puhvjy.cn/Article/details/54663.sHtML
http://www.blog.puhvjy.cn/Article/details/98612.sHtML
http://www.blog.puhvjy.cn/Article/details/9779849.sHtML
http://www.blog.puhvjy.cn/Article/details/97950.sHtML
http://www.blog.puhvjy.cn/Article/details/1225.sHtML
http://www.blog.puhvjy.cn/Article/details/09728.sHtML
http://www.blog.puhvjy.cn/Article/details/782326.sHtML
http://www.blog.puhvjy.cn/Article/details/6180396.sHtML
http://www.blog.puhvjy.cn/Article/details/0894013.sHtML
http://www.blog.puhvjy.cn/Article/details/54596.sHtML
http://www.blog.puhvjy.cn/Article/details/5404115.sHtML
http://www.blog.puhvjy.cn/Article/details/650389.sHtML
http://www.blog.puhvjy.cn/Article/details/1085.sHtML
http://www.blog.puhvjy.cn/Article/details/9137163.sHtML
http://www.blog.puhvjy.cn/Article/details/35235.sHtML
http://www.blog.puhvjy.cn/Article/details/5859169.sHtML
http://www.blog.puhvjy.cn/Article/details/280778.sHtML
http://www.blog.puhvjy.cn/Article/details/4423855.sHtML
http://www.blog.puhvjy.cn/Article/details/9815077.sHtML
http://www.blog.puhvjy.cn/Article/details/3493.sHtML
http://www.blog.puhvjy.cn/Article/details/709156.sHtML
http://www.blog.puhvjy.cn/Article/details/8091.sHtML
http://www.blog.puhvjy.cn/Article/details/0153.sHtML
http://www.blog.puhvjy.cn/Article/details/574824.sHtML
http://www.blog.puhvjy.cn/Article/details/9774.sHtML
http://www.blog.puhvjy.cn/Article/details/94841.sHtML
http://www.blog.puhvjy.cn/Article/details/2617.sHtML
http://www.blog.puhvjy.cn/Article/details/53549.sHtML
http://www.blog.puhvjy.cn/Article/details/4335298.sHtML
http://www.blog.puhvjy.cn/Article/details/3406.sHtML
http://www.blog.puhvjy.cn/Article/details/893269.sHtML
http://www.blog.puhvjy.cn/Article/details/7205.sHtML
http://www.blog.puhvjy.cn/Article/details/9205.sHtML
http://www.blog.puhvjy.cn/Article/details/4741.sHtML
http://www.blog.puhvjy.cn/Article/details/019362.sHtML
http://www.blog.puhvjy.cn/Article/details/93627.sHtML
http://www.blog.puhvjy.cn/Article/details/7906.sHtML
http://www.blog.puhvjy.cn/Article/details/3848.sHtML
http://www.blog.puhvjy.cn/Article/details/2173.sHtML
http://www.blog.puhvjy.cn/Article/details/42248.sHtML
http://www.blog.puhvjy.cn/Article/details/6593.sHtML
http://www.blog.puhvjy.cn/Article/details/99556.sHtML
http://www.blog.puhvjy.cn/Article/details/92988.sHtML
http://www.blog.puhvjy.cn/Article/details/55935.sHtML
http://www.blog.puhvjy.cn/Article/details/831401.sHtML
http://www.blog.puhvjy.cn/Article/details/06630.sHtML
http://www.blog.puhvjy.cn/Article/details/0286612.sHtML
http://www.blog.puhvjy.cn/Article/details/6999636.sHtML
http://www.blog.puhvjy.cn/Article/details/04306.sHtML
http://www.blog.puhvjy.cn/Article/details/267202.sHtML
http://www.blog.puhvjy.cn/Article/details/8042828.sHtML
http://www.blog.puhvjy.cn/Article/details/11693.sHtML
http://www.blog.puhvjy.cn/Article/details/5546.sHtML
http://www.blog.puhvjy.cn/Article/details/75681.sHtML
http://www.blog.puhvjy.cn/Article/details/2953756.sHtML
http://www.blog.puhvjy.cn/Article/details/02263.sHtML
http://www.blog.puhvjy.cn/Article/details/1969161.sHtML
http://www.blog.puhvjy.cn/Article/details/312330.sHtML
http://www.blog.puhvjy.cn/Article/details/09082.sHtML
http://www.blog.puhvjy.cn/Article/details/30281.sHtML
http://www.blog.puhvjy.cn/Article/details/369633.sHtML
http://www.blog.puhvjy.cn/Article/details/4368255.sHtML
http://www.blog.puhvjy.cn/Article/details/4045479.sHtML
http://www.blog.puhvjy.cn/Article/details/8382.sHtML
http://www.blog.puhvjy.cn/Article/details/394654.sHtML
http://www.blog.puhvjy.cn/Article/details/42627.sHtML
http://www.blog.puhvjy.cn/Article/details/0414.sHtML
http://www.blog.puhvjy.cn/Article/details/017579.sHtML
http://www.blog.puhvjy.cn/Article/details/7321600.sHtML
http://www.blog.puhvjy.cn/Article/details/6447.sHtML
http://www.blog.puhvjy.cn/Article/details/404884.sHtML
http://www.blog.puhvjy.cn/Article/details/54226.sHtML
http://www.blog.puhvjy.cn/Article/details/74376.sHtML
http://www.blog.puhvjy.cn/Article/details/80814.sHtML
http://www.blog.puhvjy.cn/Article/details/8510285.sHtML
http://www.blog.puhvjy.cn/Article/details/46900.sHtML
http://www.blog.puhvjy.cn/Article/details/224756.sHtML
http://www.blog.puhvjy.cn/Article/details/456412.sHtML
http://www.blog.puhvjy.cn/Article/details/0877.sHtML
http://www.blog.puhvjy.cn/Article/details/59993.sHtML
http://www.blog.puhvjy.cn/Article/details/3983.sHtML
http://www.blog.puhvjy.cn/Article/details/1269.sHtML
http://www.blog.puhvjy.cn/Article/details/367592.sHtML
http://www.blog.puhvjy.cn/Article/details/7933117.sHtML
http://www.blog.puhvjy.cn/Article/details/6275972.sHtML
http://www.blog.puhvjy.cn/Article/details/52552.sHtML
http://www.blog.puhvjy.cn/Article/details/27367.sHtML
http://www.blog.puhvjy.cn/Article/details/371130.sHtML
http://www.blog.puhvjy.cn/Article/details/1237249.sHtML
http://www.blog.puhvjy.cn/Article/details/0822440.sHtML
http://www.blog.puhvjy.cn/Article/details/05474.sHtML
http://www.blog.puhvjy.cn/Article/details/19632.sHtML
http://www.blog.puhvjy.cn/Article/details/290963.sHtML
http://www.blog.puhvjy.cn/Article/details/4217.sHtML
http://www.blog.puhvjy.cn/Article/details/69727.sHtML
http://www.blog.puhvjy.cn/Article/details/2847437.sHtML
http://www.blog.puhvjy.cn/Article/details/35558.sHtML
http://www.blog.puhvjy.cn/Article/details/372369.sHtML
http://www.blog.puhvjy.cn/Article/details/351060.sHtML
http://www.blog.puhvjy.cn/Article/details/96642.sHtML
http://www.blog.puhvjy.cn/Article/details/2014.sHtML
http://www.blog.puhvjy.cn/Article/details/2612961.sHtML
http://www.blog.puhvjy.cn/Article/details/36971.sHtML
http://www.blog.puhvjy.cn/Article/details/6217.sHtML
http://www.blog.puhvjy.cn/Article/details/790173.sHtML
http://www.blog.puhvjy.cn/Article/details/999217.sHtML
http://www.blog.puhvjy.cn/Article/details/3457576.sHtML
http://www.blog.puhvjy.cn/Article/details/87775.sHtML
http://www.blog.puhvjy.cn/Article/details/0905.sHtML
http://www.blog.puhvjy.cn/Article/details/1427.sHtML
http://www.blog.puhvjy.cn/Article/details/8962728.sHtML
http://www.blog.puhvjy.cn/Article/details/593203.sHtML
http://www.blog.puhvjy.cn/Article/details/2577821.sHtML
http://www.blog.puhvjy.cn/Article/details/089588.sHtML
http://www.blog.puhvjy.cn/Article/details/46823.sHtML
http://www.blog.puhvjy.cn/Article/details/98195.sHtML
http://www.blog.puhvjy.cn/Article/details/9770.sHtML
http://www.blog.puhvjy.cn/Article/details/9027591.sHtML
http://www.blog.puhvjy.cn/Article/details/8680.sHtML
http://www.blog.puhvjy.cn/Article/details/533114.sHtML
http://www.blog.puhvjy.cn/Article/details/4473423.sHtML
http://www.blog.puhvjy.cn/Article/details/1834.sHtML
http://www.blog.puhvjy.cn/Article/details/5988.sHtML
http://www.blog.puhvjy.cn/Article/details/99060.sHtML
http://www.blog.puhvjy.cn/Article/details/963052.sHtML
http://www.blog.puhvjy.cn/Article/details/592176.sHtML
http://www.blog.puhvjy.cn/Article/details/71531.sHtML
http://www.blog.puhvjy.cn/Article/details/075269.sHtML
http://www.blog.puhvjy.cn/Article/details/9943.sHtML
http://www.blog.puhvjy.cn/Article/details/988196.sHtML
http://www.blog.puhvjy.cn/Article/details/2170259.sHtML
http://www.blog.puhvjy.cn/Article/details/4573766.sHtML
http://www.blog.puhvjy.cn/Article/details/7766.sHtML
http://www.blog.puhvjy.cn/Article/details/44762.sHtML
http://www.blog.puhvjy.cn/Article/details/458380.sHtML
http://www.blog.puhvjy.cn/Article/details/000544.sHtML
http://www.blog.puhvjy.cn/Article/details/249194.sHtML
http://www.blog.puhvjy.cn/Article/details/7240.sHtML
http://www.blog.puhvjy.cn/Article/details/669942.sHtML
http://www.blog.puhvjy.cn/Article/details/2523893.sHtML
http://www.blog.puhvjy.cn/Article/details/4088.sHtML
http://www.blog.puhvjy.cn/Article/details/1425475.sHtML
http://www.blog.puhvjy.cn/Article/details/7146.sHtML
http://www.blog.puhvjy.cn/Article/details/664590.sHtML
http://www.blog.puhvjy.cn/Article/details/2105409.sHtML
http://www.blog.puhvjy.cn/Article/details/9623.sHtML
http://www.blog.puhvjy.cn/Article/details/44603.sHtML
http://www.blog.puhvjy.cn/Article/details/46074.sHtML
http://www.blog.puhvjy.cn/Article/details/3416491.sHtML
http://www.blog.puhvjy.cn/Article/details/7731133.sHtML
http://www.blog.puhvjy.cn/Article/details/912557.sHtML
http://www.blog.puhvjy.cn/Article/details/4843806.sHtML
http://www.blog.puhvjy.cn/Article/details/401305.sHtML
http://www.blog.puhvjy.cn/Article/details/8700476.sHtML
http://www.blog.puhvjy.cn/Article/details/55180.sHtML
http://www.blog.puhvjy.cn/Article/details/157524.sHtML
http://www.blog.puhvjy.cn/Article/details/65473.sHtML
http://www.blog.puhvjy.cn/Article/details/48582.sHtML
http://www.blog.puhvjy.cn/Article/details/97440.sHtML
http://www.blog.puhvjy.cn/Article/details/7337599.sHtML
http://www.blog.puhvjy.cn/Article/details/42295.sHtML
http://www.blog.puhvjy.cn/Article/details/0609240.sHtML
http://www.blog.puhvjy.cn/Article/details/4430672.sHtML
http://www.blog.puhvjy.cn/Article/details/0572189.sHtML
http://www.blog.puhvjy.cn/Article/details/7050.sHtML
http://www.blog.puhvjy.cn/Article/details/0975193.sHtML
http://www.blog.puhvjy.cn/Article/details/8945135.sHtML
http://www.blog.puhvjy.cn/Article/details/194534.sHtML
http://www.blog.puhvjy.cn/Article/details/1357547.sHtML
http://www.blog.puhvjy.cn/Article/details/514312.sHtML
http://www.blog.puhvjy.cn/Article/details/2866313.sHtML
http://www.blog.puhvjy.cn/Article/details/6187.sHtML
http://www.blog.puhvjy.cn/Article/details/70593.sHtML
http://www.blog.puhvjy.cn/Article/details/398745.sHtML
http://www.blog.puhvjy.cn/Article/details/1912774.sHtML
http://www.blog.puhvjy.cn/Article/details/4620334.sHtML
http://www.blog.puhvjy.cn/Article/details/4379968.sHtML
http://www.blog.puhvjy.cn/Article/details/26667.sHtML
http://www.blog.puhvjy.cn/Article/details/800388.sHtML
http://www.blog.puhvjy.cn/Article/details/37329.sHtML
http://www.blog.puhvjy.cn/Article/details/0234.sHtML
http://www.blog.puhvjy.cn/Article/details/279065.sHtML
http://www.blog.puhvjy.cn/Article/details/23393.sHtML
http://www.blog.puhvjy.cn/Article/details/16733.sHtML
http://www.blog.puhvjy.cn/Article/details/445628.sHtML
http://www.blog.puhvjy.cn/Article/details/607742.sHtML
http://www.blog.puhvjy.cn/Article/details/543477.sHtML
http://www.blog.puhvjy.cn/Article/details/00441.sHtML
http://www.blog.puhvjy.cn/Article/details/147498.sHtML
http://www.blog.puhvjy.cn/Article/details/883344.sHtML
http://www.blog.puhvjy.cn/Article/details/85641.sHtML
http://www.blog.puhvjy.cn/Article/details/3070.sHtML
http://www.blog.puhvjy.cn/Article/details/4766257.sHtML
http://www.blog.puhvjy.cn/Article/details/090162.sHtML
http://www.blog.puhvjy.cn/Article/details/5696725.sHtML
http://www.blog.puhvjy.cn/Article/details/2858541.sHtML
http://www.blog.puhvjy.cn/Article/details/285553.sHtML
http://www.blog.puhvjy.cn/Article/details/01755.sHtML
http://www.blog.puhvjy.cn/Article/details/316258.sHtML
http://www.blog.puhvjy.cn/Article/details/8733933.sHtML
http://www.blog.puhvjy.cn/Article/details/3753.sHtML
http://www.blog.puhvjy.cn/Article/details/199767.sHtML
http://www.blog.puhvjy.cn/Article/details/77358.sHtML
http://www.blog.puhvjy.cn/Article/details/037314.sHtML
http://www.blog.puhvjy.cn/Article/details/22756.sHtML
http://www.blog.puhvjy.cn/Article/details/6745.sHtML
http://www.blog.puhvjy.cn/Article/details/3340798.sHtML
http://www.blog.puhvjy.cn/Article/details/1299.sHtML
http://www.blog.puhvjy.cn/Article/details/9386903.sHtML
http://www.blog.puhvjy.cn/Article/details/5193961.sHtML
http://www.blog.puhvjy.cn/Article/details/625007.sHtML
http://www.blog.puhvjy.cn/Article/details/90336.sHtML
http://www.blog.puhvjy.cn/Article/details/5364152.sHtML
http://www.blog.puhvjy.cn/Article/details/21719.sHtML
http://www.blog.puhvjy.cn/Article/details/463035.sHtML
http://www.blog.puhvjy.cn/Article/details/68474.sHtML
http://www.blog.puhvjy.cn/Article/details/884821.sHtML
http://www.blog.puhvjy.cn/Article/details/28271.sHtML
http://www.blog.puhvjy.cn/Article/details/2983519.sHtML
http://www.blog.puhvjy.cn/Article/details/2832268.sHtML

## 项目结构

```
techlink-navigator/
├── data/                                   # 数据存储目录
│   ├── raw/                                # 原始导入数据暂存
│   │   ├── batch_256_280.csv               # 第256/280批外链数据
│   │   └── import_history.json             # 导入操作历史记录
│   ├── parsed/                             # 解析后的标准化数据
│   │   ├── links.db                        # SQLite主数据库（外链元数据）
│   │   └── categories.json                 # 分类与标签定义
│   └── cache/                              # 快照缓存与健康检查缓存
│       ├── snapshots/                      # 页面标题/摘要快照
│       └── health/                         # 各外链最近一次可用性检查结果
├── src/                                    # 核心源代码
│   ├── core/                               # 核心业务逻辑
│   │   ├── importer.py                     # 多格式数据导入器
│   │   ├── validator.py                    # URL格式与可访问性校验
│   │   ├── classifier.py                   # 自动分类与标签推荐
│   │   └── health_checker.py               # 链接健康状态监控
│   ├── web/                                # Web界面与API
│   │   ├── app.py                          # Flask/Streamlit主应用
│   │   ├── routes/                         # 路由与视图函数
│   │   └── templates/                      # 静态站点生成模板
│   ├── cli/                                # 命令行工具
│   │   ├── manage.py                       # 统一管理命令入口
│   │   └── commands/                       # 各子命令实现
│   └── utils/                              # 通用工具函数
│       ├── fetcher.py                      # HTTP请求与重试封装
│       ├── parser.py                       # HTML标题/摘要提取
│       └── formatter.py                    # 数据导出格式化
├── tests/                                  # 单元测试与集成测试
│   ├── unit/                               # 各模块单元测试
│   └── fixtures/                           # 测试用样例数据
├── docs/                                   # 完整文档（见文档导航章节）
├── scripts/                                # 运维与辅助脚本
│   ├── cron_health_check.sh                # 定时健康检查脚本
│   └── export_backup.sh                    # 数据备份导出脚本
├── config/                                 # 配置文件
│   ├── default.yaml                        # 默认配置
│   └── production.yaml                     # 生产环境覆盖配置
├── requirements.txt                        # Python依赖清单
├── setup.py                                # 安装打包配置
├── LICENSE                                 # MIT许可证
└── README.md                               # 本文件
```

## 贡献指南

1. 外链资源贡献：通过 Issue 提交建议收录的外链，需附带标题、简短描述及建议分类标签。提交前请确认链接可正常访问且内容与现有分类主题相关。

2. 分类体系优化：若发现现有分类存在缺失、重叠或命名不清晰的情况，可在 Discussion 中发起分类调整讨论，达成共识后提交修改分类定义文件的 Pull Request。

3. 代码与文档改进：修复 Bug、优化性能或完善文档均可通过 Pull Request 提交。代码提交需通过单元测试（tests/ 目录）及代码风格检查（flake8/pylint）。

4. 链接健康维护：定期查看 health check 报告，若发现失效链接，可协助查找替代链接或确认内容迁移后的新地址，并在数据文件中更新。

5. 本地化与国际化：欢迎贡献多语言界面翻译或外链描述的多语言版本，相关翻译文件位于 src/web/locales/ 目录。

## 常见问题

**Q：导入大量外链后，如何快速验证所有链接的可访问性？**

A：项目提供了健康检查命令，执行 `python manage.py health-check --timeout 5 --concurrency 10` 可对全量外链进行并发探测，结果会写入 data/cache/health/ 目录。检查完成后可通过 `python manage.py health-report` 生成失效链接列表及状态码摘要。

**Q：如果外链来源站点变更了 URL 结构，历史链接全部失效怎么办？**

A：可采用批量替换功能，通过 `python manage.py replace-url --old-pattern "blog.puhvjy.cn/Article/details/" --new-pattern "new-site.com/archives/"` 进行前缀替换。若只是单个链接失效，可在数据文件中直接编辑对应条目，重新导入后系统会自动覆盖旧记录并保留历史点击统计数据。

**Q：静态站点生成后，如何自定义页面主题与布局？**

A：静态站点基于 Jinja2 模板引擎生成，所有模板文件位于 src/web/templates/ 目录。用户可修改 base.html 调整全局布局，修改 index.html 调整首页展示结构。CSS 样式文件位于 src/web/static/css/，支持完全自定义。修改后执行 `python manage.py build --output ./dist` 即可重新生成全量静态页面。

## 许可证

MIT License

Copyright (c) 2026 TechLink Navigator Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

> 外链数量: 250 | 生成时间: 2026-07-05 16:29:45
