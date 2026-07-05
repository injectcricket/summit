# WebIndex Central

WebIndex Central 是一个面向技术研究者、开发者和信息分析人员的结构化外链与资源聚合系统。该项目不直接存储或托管任何原始内容，而是通过人工筛选与自动化校验相结合的方式，对分散于互联网各处的技术文档、教程文章、工具站点及深度分析报告进行系统性编录与分类索引。

本项目定位于解决技术信息碎片化与检索效率低下问题。通过统一的条目格式、标签体系与摘要规范，WebIndex Central 帮助用户在特定技术领域内快速定位高质量外部资源，避免重复检索与信息过载。项目本身以静态站点形式交付，兼容主流 HTTP 服务器部署方式，支持本地离线浏览与在线公开访问两种使用模式。

## 功能概览

**结构化外链编录** 每一条资源均经过标题提取、来源校验与分类标记，确保索引条目具备可追溯性与明确语义。

**多维度分类体系** 资源按技术领域、内容类型、目标读者等维度进行交叉归类，支持快速筛选与组合查询。

**批量导入与校验机制** 支持从结构化数据文件批量导入外链清单，并自动检测链接可达性与响应状态码。

**轻量级全文检索** 基于标题关键字与摘要描述构建本地倒排索引，无需外部搜索引擎即可完成基础检索操作。

**静态页面生成输出** 项目构建后输出为纯静态 HTML 文件，可直接挂载至 Nginx、Apache 或 CDN 服务。

**版本化变更追踪** 每次资源列表更新均记录变更日志，支持回溯历史版本与审查增量差异。

**自定义标签与备注字段** 用户可根据实际使用场景为每条外链添加个人标签与补充说明，不影响公共索引结构。

**响应式浏览界面** 默认前端模板适配桌面与移动设备，保证在不同屏幕尺寸下的可读性与操作便利性。

## 应用场景

技术团队内部知识库建设。团队可将 WebIndex Central 作为内部文档系统的外链前置层，统一管理项目开发中引用的第三方库文档、运维手册与架构设计博文，降低新人上手时的信息搜寻成本。

个人技术阅读清单管理。开发者可利用本项目的分类与检索功能，整理日常阅读中积累的技术文章、视频教程与工具官网，形成个人化的技术学习路径与参考手册。

社区资源聚合站点搭建。技术社区或开源组织可使用 WebIndex Central 快速构建社区推荐的优质资源导航页，将分散的社区贡献链接集中展示并保持更新，提升社区内容资产的可发现性。

离线环境下的资源引用目录。在无互联网接入的内网开发环境中，WebIndex Central 可作为外部文档的引用映射清单，帮助开发者在受限环境下仍能查阅所需资料的原始来源与摘要信息。

## 快速开始

以下指令适用于 Linux 与 macOS 环境，Windows 用户可使用 WSL 或 Git Bash 执行。

```bash
# 克隆项目仓库至本地
git clone https://github.com/your-org/webindex-central.git

# 进入项目目录
cd webindex-central

# 安装依赖（基于 Python 3.10+）
pip install -r requirements.txt

# 执行构建流程，生成静态站点文件
python build.py --input ./data/links.json --output ./dist
```

构建完成后，静态文件输出于 ./dist 目录，可通过任意 HTTP 服务器托管。例如使用 Python 内置模块快速启动预览：

```bash
cd ./dist
python -m http.server 8000
```

访问 http://localhost:8000 即可查看索引页面。

## 安装要求

| 依赖组件 | 必需版本 | 说明 |
|---------|---------|------|
| Python | 3.10 或更高 | 核心构建脚本运行环境，低于此版本将导致语法错误 |
| pip | 21.0 或更高 | Python 包管理器，用于安装项目依赖库 |
| requests | 2.28.0 或更高 | 用于外链可达性校验与响应状态检查 |
| markdown | 3.4.0 或更高 | 将资源描述从 Markdown 格式渲染为 HTML 内容 |
| jinja2 | 3.1.0 或更高 | 模板引擎，用于生成静态页面与索引列表 |
| json5 | 0.9.0 或更高 | 支持 JSON5 格式配置文件读取，允许注释与尾随逗号 |
| pytest | 7.0.0 或更高 | 仅开发测试阶段需要，生产环境可忽略 |
| git | 2.25.0 或更高 | 用于版本管理与变更日志生成，非强制但建议安装 |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|------|------|------------|
| 用户手册 | docs/user-guide.md | 如何进行资源检索、分类浏览与个人标签管理 |
| 管理员指南 | docs/admin-guide.md | 如何批量导入外链、执行可达性校验与发布更新 |
| 开发者文档 | docs/developer-guide.md | 如何扩展分类体系、自定义模板与修改构建流程 |
| 配置参考 | docs/configuration.md | 所有可调用的环境变量、命令行参数与配置文件字段说明 |
| 设计说明 | docs/design.md | 项目架构设计决策、数据模型与模板渲染原理 |
| 变更日志 | CHANGELOG.md | 每个版本的更新内容、修复缺陷与破坏性变更列表 |

## 资源列表

本批次为第 228/280 批，共包含 250 个外链资源。以下按类别分组列出全部原始链接，每条均保持原始格式原样呈现。

技术文章与教程

http://www.blog.jnjpgf.cn/Article/details/1428.sHtML
http://www.blog.jnjpgf.cn/Article/details/06015.sHtML
http://www.blog.jnjpgf.cn/Article/details/947121.sHtML
http://www.blog.jnjpgf.cn/Article/details/1393.sHtML
http://www.blog.jnjpgf.cn/Article/details/986717.sHtML
http://www.blog.jnjpgf.cn/Article/details/30344.sHtML
http://www.blog.jnjpgf.cn/Article/details/8175918.sHtML
http://www.blog.jnjpgf.cn/Article/details/0749.sHtML
http://www.blog.jnjpgf.cn/Article/details/1265.sHtML
http://www.blog.jnjpgf.cn/Article/details/8214162.sHtML
http://www.blog.jnjpgf.cn/Article/details/678548.sHtML
http://www.blog.jnjpgf.cn/Article/details/936225.sHtML
http://www.blog.jnjpgf.cn/Article/details/7395.sHtML
http://www.blog.jnjpgf.cn/Article/details/862949.sHtML
http://www.blog.jnjpgf.cn/Article/details/43658.sHtML
http://www.blog.jnjpgf.cn/Article/details/2365889.sHtML
http://www.blog.jnjpgf.cn/Article/details/0315693.sHtML
http://www.blog.jnjpgf.cn/Article/details/14747.sHtML
http://www.blog.jnjpgf.cn/Article/details/7482.sHtML
http://www.blog.jnjpgf.cn/Article/details/0482.sHtML
http://www.blog.jnjpgf.cn/Article/details/2550.sHtML
http://www.blog.jnjpgf.cn/Article/details/8340489.sHtML
http://www.blog.jnjpgf.cn/Article/details/3369.sHtML
http://www.blog.jnjpgf.cn/Article/details/9025786.sHtML
http://www.blog.jnjpgf.cn/Article/details/858079.sHtML
http://www.blog.jnjpgf.cn/Article/details/42559.sHtML
http://www.blog.jnjpgf.cn/Article/details/5700.sHtML
http://www.blog.jnjpgf.cn/Article/details/13242.sHtML
http://www.blog.jnjpgf.cn/Article/details/9857.sHtML
http://www.blog.jnjpgf.cn/Article/details/3589164.sHtML
http://www.blog.jnjpgf.cn/Article/details/534853.sHtML
http://www.blog.jnjpgf.cn/Article/details/5816.sHtML
http://www.blog.jnjpgf.cn/Article/details/485748.sHtML
http://www.blog.jnjpgf.cn/Article/details/6284.sHtML
http://www.blog.jnjpgf.cn/Article/details/98866.sHtML
http://www.blog.jnjpgf.cn/Article/details/461018.sHtML
http://www.blog.jnjpgf.cn/Article/details/791989.sHtML
http://www.blog.jnjpgf.cn/Article/details/893039.sHtML
http://www.blog.jnjpgf.cn/Article/details/9996187.sHtML
http://www.blog.jnjpgf.cn/Article/details/6665803.sHtML
http://www.blog.jnjpgf.cn/Article/details/9834451.sHtML
http://www.blog.jnjpgf.cn/Article/details/1439480.sHtML
http://www.blog.jnjpgf.cn/Article/details/7422790.sHtML
http://www.blog.jnjpgf.cn/Article/details/8191636.sHtML
http://www.blog.jnjpgf.cn/Article/details/2310451.sHtML
http://www.blog.jnjpgf.cn/Article/details/35120.sHtML
http://www.blog.jnjpgf.cn/Article/details/832285.sHtML
http://www.blog.jnjpgf.cn/Article/details/03108.sHtML
http://www.blog.jnjpgf.cn/Article/details/76154.sHtML
http://www.blog.jnjpgf.cn/Article/details/5158363.sHtML
http://www.blog.jnjpgf.cn/Article/details/6813385.sHtML
http://www.blog.jnjpgf.cn/Article/details/00126.sHtML
http://www.blog.jnjpgf.cn/Article/details/7938.sHtML
http://www.blog.jnjpgf.cn/Article/details/0102889.sHtML
http://www.blog.jnjpgf.cn/Article/details/56413.sHtML
http://www.blog.jnjpgf.cn/Article/details/4099827.sHtML
http://www.blog.jnjpgf.cn/Article/details/1930604.sHtML
http://www.blog.jnjpgf.cn/Article/details/3229665.sHtML
http://www.blog.jnjpgf.cn/Article/details/529751.sHtML
http://www.blog.jnjpgf.cn/Article/details/231221.sHtML
http://www.blog.jnjpgf.cn/Article/details/1910.sHtML
http://www.blog.jnjpgf.cn/Article/details/2453.sHtML
http://www.blog.jnjpgf.cn/Article/details/6098529.sHtML
http://www.blog.jnjpgf.cn/Article/details/15201.sHtML
http://www.blog.jnjpgf.cn/Article/details/5795.sHtML
http://www.blog.jnjpgf.cn/Article/details/9579.sHtML
http://www.blog.jnjpgf.cn/Article/details/41526.sHtML
http://www.blog.jnjpgf.cn/Article/details/463414.sHtML
http://www.blog.jnjpgf.cn/Article/details/5862608.sHtML
http://www.blog.jnjpgf.cn/Article/details/20651.sHtML
http://www.blog.jnjpgf.cn/Article/details/7878.sHtML
http://www.blog.jnjpgf.cn/Article/details/9769.sHtML
http://www.blog.jnjpgf.cn/Article/details/6507620.sHtML
http://www.blog.jnjpgf.cn/Article/details/3161.sHtML
http://www.blog.jnjpgf.cn/Article/details/662353.sHtML
http://www.blog.jnjpgf.cn/Article/details/7092.sHtML
http://www.blog.jnjpgf.cn/Article/details/955434.sHtML
http://www.blog.jnjpgf.cn/Article/details/044595.sHtML
http://www.blog.jnjpgf.cn/Article/details/18169.sHtML
http://www.blog.jnjpgf.cn/Article/details/7913906.sHtML
http://www.blog.jnjpgf.cn/Article/details/248304.sHtML
http://www.blog.jnjpgf.cn/Article/details/274453.sHtML
http://www.blog.jnjpgf.cn/Article/details/21796.sHtML
http://www.blog.jnjpgf.cn/Article/details/4553127.sHtML
http://www.blog.jnjpgf.cn/Article/details/7419.sHtML
http://www.blog.jnjpgf.cn/Article/details/9200314.sHtML
http://www.blog.jnjpgf.cn/Article/details/5732.sHtML
http://www.blog.jnjpgf.cn/Article/details/5659104.sHtML
http://www.blog.jnjpgf.cn/Article/details/8100470.sHtML
http://www.blog.jnjpgf.cn/Article/details/007533.sHtML
http://www.blog.jnjpgf.cn/Article/details/330736.sHtML
http://www.blog.jnjpgf.cn/Article/details/0754267.sHtML
http://www.blog.jnjpgf.cn/Article/details/36831.sHtML
http://www.blog.jnjpgf.cn/Article/details/40167.sHtML
http://www.blog.jnjpgf.cn/Article/details/4195494.sHtML
http://www.blog.jnjpgf.cn/Article/details/2579159.sHtML
http://www.blog.jnjpgf.cn/Article/details/1216717.sHtML
http://www.blog.jnjpgf.cn/Article/details/37255.sHtML
http://www.blog.jnjpgf.cn/Article/details/4699.sHtML
http://www.blog.jnjpgf.cn/Article/details/2001.sHtML
http://www.blog.jnjpgf.cn/Article/details/59204.sHtML
http://www.blog.jnjpgf.cn/Article/details/405541.sHtML
http://www.blog.jnjpgf.cn/Article/details/8493225.sHtML
http://www.blog.jnjpgf.cn/Article/details/96703.sHtML
http://www.blog.jnjpgf.cn/Article/details/8032068.sHtML
http://www.blog.jnjpgf.cn/Article/details/5018.sHtML
http://www.blog.jnjpgf.cn/Article/details/414660.sHtML
http://www.blog.jnjpgf.cn/Article/details/01378.sHtML
http://www.blog.jnjpgf.cn/Article/details/2929257.sHtML
http://www.blog.jnjpgf.cn/Article/details/35992.sHtML
http://www.blog.jnjpgf.cn/Article/details/7978509.sHtML
http://www.blog.jnjpgf.cn/Article/details/6488.sHtML
http://www.blog.jnjpgf.cn/Article/details/116119.sHtML
http://www.blog.jnjpgf.cn/Article/details/0184463.sHtML
http://www.blog.jnjpgf.cn/Article/details/57332.sHtML
http://www.blog.jnjpgf.cn/Article/details/04071.sHtML
http://www.blog.jnjpgf.cn/Article/details/9284746.sHtML
http://www.blog.jnjpgf.cn/Article/details/7726.sHtML
http://www.blog.jnjpgf.cn/Article/details/067444.sHtML
http://www.blog.jnjpgf.cn/Article/details/8012594.sHtML
http://www.blog.jnjpgf.cn/Article/details/0438.sHtML
http://www.blog.jnjpgf.cn/Article/details/259737.sHtML
http://www.blog.jnjpgf.cn/Article/details/42078.sHtML
http://www.blog.jnjpgf.cn/Article/details/095810.sHtML
http://www.blog.jnjpgf.cn/Article/details/75356.sHtML
http://www.blog.jnjpgf.cn/Article/details/0354735.sHtML
http://www.blog.jnjpgf.cn/Article/details/16600.sHtML
http://www.blog.jnjpgf.cn/Article/details/488684.sHtML
http://www.blog.jnjpgf.cn/Article/details/852125.sHtML
http://www.blog.jnjpgf.cn/Article/details/1984556.sHtML
http://www.blog.jnjpgf.cn/Article/details/8573624.sHtML
http://www.blog.jnjpgf.cn/Article/details/39730.sHtML
http://www.blog.jnjpgf.cn/Article/details/01900.sHtML
http://www.blog.jnjpgf.cn/Article/details/1800715.sHtML
http://www.blog.jnjpgf.cn/Article/details/0516.sHtML
http://www.blog.jnjpgf.cn/Article/details/834618.sHtML
http://www.blog.jnjpgf.cn/Article/details/0795568.sHtML
http://www.blog.jnjpgf.cn/Article/details/53005.sHtML
http://www.blog.jnjpgf.cn/Article/details/69906.sHtML
http://www.blog.jnjpgf.cn/Article/details/011145.sHtML
http://www.blog.jnjpgf.cn/Article/details/929266.sHtML
http://www.blog.jnjpgf.cn/Article/details/9113342.sHtML
http://www.blog.jnjpgf.cn/Article/details/74220.sHtML
http://www.blog.jnjpgf.cn/Article/details/84602.sHtML
http://www.blog.jnjpgf.cn/Article/details/10278.sHtML
http://www.blog.jnjpgf.cn/Article/details/758165.sHtML
http://www.blog.jnjpgf.cn/Article/details/00360.sHtML
http://www.blog.jnjpgf.cn/Article/details/244570.sHtML
http://www.blog.jnjpgf.cn/Article/details/1401400.sHtML
http://www.blog.jnjpgf.cn/Article/details/7356191.sHtML
http://www.blog.jnjpgf.cn/Article/details/2711.sHtML
http://www.blog.jnjpgf.cn/Article/details/757911.sHtML
http://www.blog.jnjpgf.cn/Article/details/1920.sHtML
http://www.blog.jnjpgf.cn/Article/details/3667.sHtML
http://www.blog.jnjpgf.cn/Article/details/8606388.sHtML
http://www.blog.jnjpgf.cn/Article/details/5551.sHtML
http://www.blog.jnjpgf.cn/Article/details/971840.sHtML
http://www.blog.jnjpgf.cn/Article/details/518063.sHtML
http://www.blog.jnjpgf.cn/Article/details/3131.sHtML
http://www.blog.jnjpgf.cn/Article/details/8935588.sHtML
http://www.blog.jnjpgf.cn/Article/details/1294394.sHtML
http://www.blog.jnjpgf.cn/Article/details/24044.sHtML
http://www.blog.jnjpgf.cn/Article/details/284987.sHtML
http://www.blog.jnjpgf.cn/Article/details/2513859.sHtML
http://www.blog.jnjpgf.cn/Article/details/76184.sHtML
http://www.blog.jnjpgf.cn/Article/details/490614.sHtML
http://www.blog.jnjpgf.cn/Article/details/6095996.sHtML
http://www.blog.jnjpgf.cn/Article/details/1338.sHtML
http://www.blog.jnjpgf.cn/Article/details/9293.sHtML
http://www.blog.jnjpgf.cn/Article/details/68436.sHtML
http://www.blog.jnjpgf.cn/Article/details/588232.sHtML
http://www.blog.jnjpgf.cn/Article/details/225952.sHtML
http://www.blog.jnjpgf.cn/Article/details/4493443.sHtML
http://www.blog.jnjpgf.cn/Article/details/878960.sHtML
http://www.blog.jnjpgf.cn/Article/details/66870.sHtML
http://www.blog.jnjpgf.cn/Article/details/2296781.sHtML
http://www.blog.jnjpgf.cn/Article/details/168258.sHtML
http://www.blog.jnjpgf.cn/Article/details/7023.sHtML
http://www.blog.jnjpgf.cn/Article/details/0694.sHtML
http://www.blog.jnjpgf.cn/Article/details/2166.sHtML
http://www.blog.jnjpgf.cn/Article/details/80743.sHtML
http://www.blog.jnjpgf.cn/Article/details/687910.sHtML
http://www.blog.jnjpgf.cn/Article/details/54998.sHtML
http://www.blog.jnjpgf.cn/Article/details/63011.sHtML
http://www.blog.jnjpgf.cn/Article/details/315034.sHtML
http://www.blog.jnjpgf.cn/Article/details/1045495.sHtML
http://www.blog.jnjpgf.cn/Article/details/3214.sHtML
http://www.blog.jnjpgf.cn/Article/details/1058.sHtML
http://www.blog.jnjpgf.cn/Article/details/3393983.sHtML
http://www.blog.jnjpgf.cn/Article/details/45841.sHtML
http://www.blog.jnjpgf.cn/Article/details/8618.sHtML
http://www.blog.jnjpgf.cn/Article/details/567549.sHtML
http://www.blog.jnjpgf.cn/Article/details/588715.sHtML
http://www.blog.jnjpgf.cn/Article/details/61551.sHtML
http://www.blog.jnjpgf.cn/Article/details/06243.sHtML
http://www.blog.jnjpgf.cn/Article/details/61206.sHtML
http://www.blog.jnjpgf.cn/Article/details/665709.sHtML
http://www.blog.jnjpgf.cn/Article/details/86721.sHtML
http://www.blog.jnjpgf.cn/Article/details/9555.sHtML
http://www.blog.jnjpgf.cn/Article/details/763270.sHtML
http://www.blog.jnjpgf.cn/Article/details/9167553.sHtML
http://www.blog.jnjpgf.cn/Article/details/672316.sHtML
http://www.blog.jnjpgf.cn/Article/details/443685.sHtML
http://www.blog.jnjpgf.cn/Article/details/6894.sHtML
http://www.blog.jnjpgf.cn/Article/details/12513.sHtML
http://www.blog.jnjpgf.cn/Article/details/561270.sHtML
http://www.blog.jnjpgf.cn/Article/details/180031.sHtML
http://www.blog.jnjpgf.cn/Article/details/79457.sHtML
http://www.blog.jnjpgf.cn/Article/details/3627.sHtML
http://www.blog.jnjpgf.cn/Article/details/4177.sHtML
http://www.blog.jnjpgf.cn/Article/details/27497.sHtML
http://www.blog.jnjpgf.cn/Article/details/61431.sHtML
http://www.blog.jnjpgf.cn/Article/details/990404.sHtML
http://www.blog.jnjpgf.cn/Article/details/323408.sHtML
http://www.blog.jnjpgf.cn/Article/details/9623.sHtML
http://www.blog.jnjpgf.cn/Article/details/5304.sHtML
http://www.blog.jnjpgf.cn/Article/details/5440.sHtML
http://www.blog.jnjpgf.cn/Article/details/374391.sHtML
http://www.blog.jnjpgf.cn/Article/details/54240.sHtML
http://www.blog.jnjpgf.cn/Article/details/86355.sHtML
http://www.blog.jnjpgf.cn/Article/details/0715904.sHtML
http://www.blog.jnjpgf.cn/Article/details/0815.sHtML
http://www.blog.jnjpgf.cn/Article/details/6673444.sHtML
http://www.blog.jnjpgf.cn/Article/details/4384.sHtML
http://www.blog.jnjpgf.cn/Article/details/5638277.sHtML
http://www.blog.jnjpgf.cn/Article/details/387686.sHtML
http://www.blog.jnjpgf.cn/Article/details/957854.sHtML
http://www.blog.jnjpgf.cn/Article/details/7357965.sHtML
http://www.blog.jnjpgf.cn/Article/details/311447.sHtML
http://www.blog.jnjpgf.cn/Article/details/7613448.sHtML
http://www.blog.jnjpgf.cn/Article/details/292401.sHtML
http://www.blog.jnjpgf.cn/Article/details/59649.sHtML
http://www.blog.jnjpgf.cn/Article/details/6542307.sHtML
http://www.blog.jnjpgf.cn/Article/details/8452897.sHtML
http://www.blog.jnjpgf.cn/Article/details/367478.sHtML
http://www.blog.jnjpgf.cn/Article/details/2128.sHtML
http://www.blog.jnjpgf.cn/Article/details/9851909.sHtML
http://www.blog.jnjpgf.cn/Article/details/3045724.sHtML
http://www.blog.jnjpgf.cn/Article/details/304582.sHtML
http://www.blog.jnjpgf.cn/Article/details/01325.sHtML
http://www.blog.jnjpgf.cn/Article/details/76493.sHtML
http://www.blog.jnjpgf.cn/Article/details/5093.sHtML
http://www.blog.jnjpgf.cn/Article/details/26003.sHtML
http://www.blog.jnjpgf.cn/Article/details/0248257.sHtML
http://www.blog.jnjpgf.cn/Article/details/513255.sHtML
http://www.blog.jnjpgf.cn/Article/details/6067247.sHtML
http://www.blog.jnjpgf.cn/Article/details/758725.sHtML
http://www.blog.jnjpgf.cn/Article/details/428472.sHtML
http://www.blog.jnjpgf.cn/Article/details/26381.sHtML
http://www.blog.jnjpgf.cn/Article/details/8796.sHtML

## 项目结构

```
webindex-central/
├── build.py                 # 主构建脚本，协调数据加载、模板渲染与输出
├── requirements.txt         # Python 依赖声明文件，用于 pip 安装
├── CHANGELOG.md             # 版本变更记录，按日期与版本号归档
├── README.md                # 项目说明文档（本文件）
├── .gitignore               # Git 版本忽略规则，排除临时与敏感文件
│
├── data/                    # 数据存储目录
│   ├── links.json           # 主外链索引数据，JSON 格式，包含标题、URL、分类与标签
│   ├── categories.json      # 分类体系定义，包含层级关系与显示名称
│   └── schema/              # JSON Schema 校验文件，用于数据格式验证
│       └── link-schema.json
│
├── src/                     # 核心源代码目录
│   ├── loader.py            # 数据加载与解析模块，支持 JSON/JSON5 格式
│   ├── validator.py         # 链接可达性校验与状态检查模块
│   ├── indexer.py           # 本地倒排索引构建与检索模块
│   ├── renderer.py          # 模板渲染引擎封装，基于 Jinja2
│   └── utils.py             # 通用工具函数，含日志、路径处理与日期格式化
│
├── templates/               # Jinja2 模板目录
│   ├── base.html            # 基础布局模板，定义页面骨架与通用样式
│   ├── index.html           # 首页模板，展示分类导航与最新资源
│   ├── detail.html          # 资源详情页模板，展示完整条目信息
│   └── search.html          # 搜索结果页模板
│
├── static/                  # 静态资源目录，构建时原样复制至输出目录
│   ├── css/                 # 样式表文件
│   │   ├── main.css
│   │   └── responsive.css
│   ├── js/                  # 前端 JavaScript 脚本
│   │   ├── search.js
│   │   └── filter.js
│   └── assets/              # 图片与字体等资源
│       └── logo.svg
│
├── tests/                   # 单元测试与集成测试目录
│   ├── test_loader.py
│   ├── test_validator.py
│   └── test_indexer.py
│
└── dist/                    # 构建输出目录（生成产物，默认不纳入版本库）
    ├── index.html
    ├── detail/
    ├── search/
    └── static/
```

## 贡献指南

贡献者需遵循以下流程以保证索引质量与项目一致性。

第一，在 GitHub 上 Fork 本仓库至个人账户，并克隆至本地开发环境。所有修改应在独立功能分支上进行，分支命名格式为 feature/简述修改内容 或 fix/简述修复问题。

第二，修改 data/links.json 文件时，必须严格遵循 data/schema/link-schema.json 中定义的格式规范，包括必需字段（title、url、category、tags）与字段类型。新增条目须确保 url 字段为完整 HTTP/HTTPS 链接且可访问。

第三，提交变更前需执行本地构建与校验流程。运行 python build.py --validate-only 进行数据格式校验与链接可达性检查，确保无报错后执行完整构建 python build.py --output ./dist 并检查输出页面渲染是否正常。

第四，提交 Pull Request 时需附清晰描述，说明本次变更的目的、涉及条目数量以及任何可能影响现有功能的风险点。PR 标题应遵循 [Category] Brief Description 格式，例如 [Data] Add 50 links for distributed systems。

第五，项目维护者将在 PR 提交后 3 个工作日内进行审查。若审查通过则合并至主分支，并自动触发变更日志更新与静态站点重新部署。

## 常见问题

问：构建过程中遇到 ModuleNotFoundError: No module named 'json5' 如何解决？

答：请检查 requirements.txt 文件是否完整安装。执行 pip install -r requirements.txt --upgrade 重新安装所有依赖。若仍存在问题，可尝试使用 pip install json5 单独安装该模块，并确认 Python 环境版本符合 3.10 或更高要求。

问：外链可达性校验报错超时或连接被拒绝，是否影响构建流程？

答：默认情况下，校验超时或连接错误会记录警告日志但不会中断构建流程，以保证索引数据的完整性。若需要严格模式，可在 build.py 中设置 --strict 参数，此时任何不可达链接将导致构建失败。建议在批量导入新链接时先使用 --validate-only 模式进行预检。

问：如何自定义输出页面的品牌标识与配色方案？

答：品牌标识替换位于 static/assets/logo.svg，直接覆盖该文件即可。配色方案与全局样式定义于 static/css/main.css 中的 CSS 变量（:root 选择器下），调整 --primary-color、--secondary-color 等变量值可快速变更主题色调，无需修改模板文件。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:29:37
