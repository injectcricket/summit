# WebArchive Indexer

WebArchive Indexer 是一个面向技术研究者和内容策展人的结构化外链资源索引系统。该项目将分散于博客平台的历史技术文章、开发笔记与工程案例进行统一抓取、分类与元数据标注，生成可检索、可追溯的静态资源目录。项目本身不存储文章内容，仅提供稳定的引用聚合与状态监控能力，帮助团队或个人在文档站点、知识库或内部培训体系中快速引用外部参考材料。

目标用户包括技术文档工程师、开源项目维护者、DevOps 团队以及需要长期跟踪特定领域技术动态的研究人员。通过标准化的 URL 登记与健康检查机制，WebArchive Indexer 能够有效降低链接失效对知识体系造成的冲击，并支持按批次、按来源域名的批量导入与导出操作。

## 功能概览

**批量链接导入**：支持通过 CSV 或纯文本列表批量导入外部 URL，自动解析域名、路径与查询参数，生成结构化索引记录。

**健康状态巡检**：每日定时检测已收录链接的可访问性，标记 4xx、5xx 状态码及 DNS 解析异常，输出巡检报告。

**分类标签管理**：允许用户为每条链接添加自定义标签（如 "Docker"、"API 设计"、"性能调优"），支持多标签组合筛选。

**元数据提取**：对可访问的 HTML 页面自动提取标题、描述、发布日期及主要内容摘要（基于正文抽取算法）。

**静态站点生成**：基于索引数据一键生成纯静态 HTML 目录页，支持响应式布局与全文检索，适合托管于 GitHub Pages 或对象存储服务。

**变更日志记录**：记录每条链接的添加时间、状态变更历史及备注信息，便于团队审计与回溯。

**导出兼容性**：支持将索引数据导出为 JSON、YAML 或 Markdown 表格格式，便于与其他文档工具链集成。

## 应用场景

内部技术文档库的外链管理：企业技术团队在撰写设计文档或复盘报告时，需要引用大量外部博客文章。WebArchive Indexer 提供统一的引用登记入口，避免散落在 Wiki 或即时通讯工具中的链接失联，同时通过定期巡检提前发现不可用资源，提醒作者寻找替代材料。

开源项目 README 资源汇总：开源项目维护者经常在 README 中列出相关教程、生态工具或社区讨论链接。随着项目迭代，这些链接可能逐渐失效。使用 WebArchive Indexer 对链接进行批次管理与状态追踪，可以定期更新 README 中的外链部分，确保用户获得的参考信息始终有效。

技术雷达与行业动态追踪：技术调研团队需要定期梳理特定领域（如云原生、机器学习基础设施）的新兴项目与深度分析文章。WebArchive Indexer 允许按主题标签聚合链接，并记录每篇文章的发布时间与摘要，便于构建领域知识的时间轴视图，支撑技术选型决策。

离线文档备份的前置准备：在进行内部知识库的离线化改造时，需先梳理所有外部依赖链接。WebArchive Indexer 可生成完整的链接清单与元数据，供后续的离线归档工具或网页存档服务使用，确保离线副本与原始来源的对应关系清晰可溯。

## 快速开始

以下指令适用于 Linux 及 macOS 环境，Windows 用户建议通过 WSL2 或 Git Bash 执行。

```bash
# 克隆项目仓库
git clone https://github.com/your-org/webarchive-indexer.git
cd webarchive-indexer

# 安装 Python 依赖（推荐使用虚拟环境）
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# 初始化本地索引数据库并运行示例导入
python indexer.py --init
python indexer.py --import samples/links_batch_34.txt --batch 34
python indexer.py --status-check --batch 34
python indexer.py --generate --output ./public
```

执行完成后，可在 `./public/index.html` 查看生成的静态目录页。如需调整巡检间隔或输出格式，请参阅 `config.yaml` 中的参数说明。

## 安装要求

| 依赖组件 | 必需版本 | 说明 |
|---|---|---|
| Python | 3.9 或更高 | 核心运行环境，建议使用 3.11+ 以获得性能优化 |
| SQLite | 3.35 或更高 | 内置轻量级数据库，用于存储索引记录与状态日志，无需额外安装 |
| requests | 2.28.0 或更高 | HTTP 请求库，用于链接健康检查与页面内容获取 |
| beautifulsoup4 | 4.11.0 或更高 | HTML 解析库，用于标题及正文摘要提取 |
| PyYAML | 6.0 或更高 | 配置文件解析，支持自定义巡检策略与输出模板 |
| Jinja2 | 3.1.0 或更高 | 模板引擎，用于静态 HTML 目录页渲染 |
| pytest | 7.2.0 或更高 | 单元测试框架（仅开发环境需要） |
| black | 22.3.0 或更高 | 代码格式化工具（仅开发环境需要） |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|---|---|---|
| 入门指南 | docs/quickstart.md | 如何最快上手使用索引器的导入、巡检与生成三大核心命令 |
| 配置参考 | docs/configuration.md | config.yaml 中每个字段的含义及自定义调度策略的写法 |
| 数据格式 | docs/data-format.md | 索引表结构、JSON 导出字段定义以及标签系统的设计规范 |
| 运维手册 | docs/operations.md | 如何设置定时巡检任务、处理异常链接以及迁移索引数据库 |

## 资源列表

本批次为第 34/280 批，共收录 250 条来自 blog.fuvxie.cn 的技术文章链接。所有 URL 均按来源域名分组，并保留原始路径与查询参数格式，确保精确引用。

技术文章主站

http://www.blog.fuvxie.cn/Article/details/0409144.sHtML
http://www.blog.fuvxie.cn/Article/details/489431.sHtML
http://www.blog.fuvxie.cn/Article/details/905682.sHtML
http://www.blog.fuvxie.cn/Article/details/92263.sHtML
http://www.blog.fuvxie.cn/Article/details/2865.sHtML
http://www.blog.fuvxie.cn/Article/details/216124.sHtML
http://www.blog.fuvxie.cn/Article/details/442122.sHtML
http://www.blog.fuvxie.cn/Article/details/6497.sHtML
http://www.blog.fuvxie.cn/Article/details/3595858.sHtML
http://www.blog.fuvxie.cn/Article/details/243716.sHtML
http://www.blog.fuvxie.cn/Article/details/8433.sHtML
http://www.blog.fuvxie.cn/Article/details/8918.sHtML
http://www.blog.fuvxie.cn/Article/details/1630274.sHtML
http://www.blog.fuvxie.cn/Article/details/123904.sHtML
http://www.blog.fuvxie.cn/Article/details/340912.sHtML
http://www.blog.fuvxie.cn/Article/details/3047441.sHtML
http://www.blog.fuvxie.cn/Article/details/872959.sHtML
http://www.blog.fuvxie.cn/Article/details/925450.sHtML
http://www.blog.fuvxie.cn/Article/details/0850857.sHtML
http://www.blog.fuvxie.cn/Article/details/981902.sHtML
http://www.blog.fuvxie.cn/Article/details/169667.sHtML
http://www.blog.fuvxie.cn/Article/details/41589.sHtML
http://www.blog.fuvxie.cn/Article/details/87933.sHtML
http://www.blog.fuvxie.cn/Article/details/6697.sHtML
http://www.blog.fuvxie.cn/Article/details/35105.sHtML
http://www.blog.fuvxie.cn/Article/details/0819639.sHtML
http://www.blog.fuvxie.cn/Article/details/99389.sHtML
http://www.blog.fuvxie.cn/Article/details/23001.sHtML
http://www.blog.fuvxie.cn/Article/details/343791.sHtML
http://www.blog.fuvxie.cn/Article/details/13216.sHtML
http://www.blog.fuvxie.cn/Article/details/1548243.sHtML
http://www.blog.fuvxie.cn/Article/details/68579.sHtML
http://www.blog.fuvxie.cn/Article/details/408453.sHtML
http://www.blog.fuvxie.cn/Article/details/79872.sHtML
http://www.blog.fuvxie.cn/Article/details/8726.sHtML
http://www.blog.fuvxie.cn/Article/details/4058296.sHtML
http://www.blog.fuvxie.cn/Article/details/7359.sHtML
http://www.blog.fuvxie.cn/Article/details/0699578.sHtML
http://www.blog.fuvxie.cn/Article/details/554705.sHtML
http://www.blog.fuvxie.cn/Article/details/7845646.sHtML
http://www.blog.fuvxie.cn/Article/details/782032.sHtML
http://www.blog.fuvxie.cn/Article/details/0178.sHtML
http://www.blog.fuvxie.cn/Article/details/3381714.sHtML
http://www.blog.fuvxie.cn/Article/details/425955.sHtML
http://www.blog.fuvxie.cn/Article/details/5119.sHtML
http://www.blog.fuvxie.cn/Article/details/981062.sHtML
http://www.blog.fuvxie.cn/Article/details/9657456.sHtML
http://www.blog.fuvxie.cn/Article/details/566412.sHtML
http://www.blog.fuvxie.cn/Article/details/13303.sHtML
http://www.blog.fuvxie.cn/Article/details/6487.sHtML
http://www.blog.fuvxie.cn/Article/details/45016.sHtML
http://www.blog.fuvxie.cn/Article/details/1303181.sHtML
http://www.blog.fuvxie.cn/Article/details/8745.sHtML
http://www.blog.fuvxie.cn/Article/details/62702.sHtML
http://www.blog.fuvxie.cn/Article/details/9756784.sHtML
http://www.blog.fuvxie.cn/Article/details/7677814.sHtML
http://www.blog.fuvxie.cn/Article/details/4649.sHtML
http://www.blog.fuvxie.cn/Article/details/5719621.sHtML
http://www.blog.fuvxie.cn/Article/details/8226.sHtML
http://www.blog.fuvxie.cn/Article/details/072931.sHtML
http://www.blog.fuvxie.cn/Article/details/9108.sHtML
http://www.blog.fuvxie.cn/Article/details/94458.sHtML
http://www.blog.fuvxie.cn/Article/details/83341.sHtML
http://www.blog.fuvxie.cn/Article/details/253840.sHtML
http://www.blog.fuvxie.cn/Article/details/10916.sHtML
http://www.blog.fuvxie.cn/Article/details/0753.sHtML
http://www.blog.fuvxie.cn/Article/details/0134892.sHtML
http://www.blog.fuvxie.cn/Article/details/3818315.sHtML
http://www.blog.fuvxie.cn/Article/details/8010627.sHtML
http://www.blog.fuvxie.cn/Article/details/53771.sHtML
http://www.blog.fuvxie.cn/Article/details/1798.sHtML
http://www.blog.fuvxie.cn/Article/details/61281.sHtML
http://www.blog.fuvxie.cn/Article/details/1403230.sHtML
http://www.blog.fuvxie.cn/Article/details/8267.sHtML
http://www.blog.fuvxie.cn/Article/details/8862787.sHtML
http://www.blog.fuvxie.cn/Article/details/1158.sHtML
http://www.blog.fuvxie.cn/Article/details/3539219.sHtML
http://www.blog.fuvxie.cn/Article/details/1675.sHtML
http://www.blog.fuvxie.cn/Article/details/8225598.sHtML
http://www.blog.fuvxie.cn/Article/details/17952.sHtML
http://www.blog.fuvxie.cn/Article/details/9500.sHtML
http://www.blog.fuvxie.cn/Article/details/31837.sHtML
http://www.blog.fuvxie.cn/Article/details/80730.sHtML
http://www.blog.fuvxie.cn/Article/details/381579.sHtML
http://www.blog.fuvxie.cn/Article/details/5156527.sHtML
http://www.blog.fuvxie.cn/Article/details/15065.sHtML
http://www.blog.fuvxie.cn/Article/details/861654.sHtML
http://www.blog.fuvxie.cn/Article/details/63370.sHtML
http://www.blog.fuvxie.cn/Article/details/33319.sHtML
http://www.blog.fuvxie.cn/Article/details/6348.sHtML
http://www.blog.fuvxie.cn/Article/details/514943.sHtML
http://www.blog.fuvxie.cn/Article/details/671721.sHtML
http://www.blog.fuvxie.cn/Article/details/7900.sHtML
http://www.blog.fuvxie.cn/Article/details/9053.sHtML
http://www.blog.fuvxie.cn/Article/details/874346.sHtML
http://www.blog.fuvxie.cn/Article/details/691233.sHtML
http://www.blog.fuvxie.cn/Article/details/030726.sHtML
http://www.blog.fuvxie.cn/Article/details/2602195.sHtML
http://www.blog.fuvxie.cn/Article/details/21204.sHtML
http://www.blog.fuvxie.cn/Article/details/0335486.sHtML
http://www.blog.fuvxie.cn/Article/details/5925911.sHtML
http://www.blog.fuvxie.cn/Article/details/9849669.sHtML
http://www.blog.fuvxie.cn/Article/details/21283.sHtML
http://www.blog.fuvxie.cn/Article/details/904230.sHtML
http://www.blog.fuvxie.cn/Article/details/56313.sHtML
http://www.blog.fuvxie.cn/Article/details/844512.sHtML
http://www.blog.fuvxie.cn/Article/details/215099.sHtML
http://www.blog.fuvxie.cn/Article/details/7718896.sHtML
http://www.blog.fuvxie.cn/Article/details/048248.sHtML
http://www.blog.fuvxie.cn/Article/details/2632.sHtML
http://www.blog.fuvxie.cn/Article/details/203160.sHtML
http://www.blog.fuvxie.cn/Article/details/751752.sHtML
http://www.blog.fuvxie.cn/Article/details/019370.sHtML
http://www.blog.fuvxie.cn/Article/details/953379.sHtML
http://www.blog.fuvxie.cn/Article/details/652309.sHtML
http://www.blog.fuvxie.cn/Article/details/6284716.sHtML
http://www.blog.fuvxie.cn/Article/details/9142.sHtML
http://www.blog.fuvxie.cn/Article/details/049518.sHtML
http://www.blog.fuvxie.cn/Article/details/4828305.sHtML
http://www.blog.fuvxie.cn/Article/details/753686.sHtML
http://www.blog.fuvxie.cn/Article/details/2352.sHtML
http://www.blog.fuvxie.cn/Article/details/63775.sHtML
http://www.blog.fuvxie.cn/Article/details/811033.sHtML
http://www.blog.fuvxie.cn/Article/details/0772.sHtML
http://www.blog.fuvxie.cn/Article/details/835614.sHtML
http://www.blog.fuvxie.cn/Article/details/921457.sHtML
http://www.blog.fuvxie.cn/Article/details/883368.sHtML
http://www.blog.fuvxie.cn/Article/details/4044778.sHtML
http://www.blog.fuvxie.cn/Article/details/31514.sHtML
http://www.blog.fuvxie.cn/Article/details/7664.sHtML
http://www.blog.fuvxie.cn/Article/details/5613952.sHtML
http://www.blog.fuvxie.cn/Article/details/0091355.sHtML
http://www.blog.fuvxie.cn/Article/details/5229459.sHtML
http://www.blog.fuvxie.cn/Article/details/62429.sHtML
http://www.blog.fuvxie.cn/Article/details/8329.sHtML
http://www.blog.fuvxie.cn/Article/details/6063.sHtML
http://www.blog.fuvxie.cn/Article/details/929654.sHtML
http://www.blog.fuvxie.cn/Article/details/4933619.sHtML
http://www.blog.fuvxie.cn/Article/details/168686.sHtML
http://www.blog.fuvxie.cn/Article/details/6445.sHtML
http://www.blog.fuvxie.cn/Article/details/914529.sHtML
http://www.blog.fuvxie.cn/Article/details/7567.sHtML
http://www.blog.fuvxie.cn/Article/details/2098.sHtML
http://www.blog.fuvxie.cn/Article/details/4733188.sHtML
http://www.blog.fuvxie.cn/Article/details/56511.sHtML
http://www.blog.fuvxie.cn/Article/details/7218.sHtML
http://www.blog.fuvxie.cn/Article/details/6711.sHtML
http://www.blog.fuvxie.cn/Article/details/4077.sHtML
http://www.blog.fuvxie.cn/Article/details/22138.sHtML
http://www.blog.fuvxie.cn/Article/details/925062.sHtML
http://www.blog.fuvxie.cn/Article/details/307039.sHtML
http://www.blog.fuvxie.cn/Article/details/1928.sHtML
http://www.blog.fuvxie.cn/Article/details/790164.sHtML
http://www.blog.fuvxie.cn/Article/details/067574.sHtML
http://www.blog.fuvxie.cn/Article/details/9686046.sHtML
http://www.blog.fuvxie.cn/Article/details/4401.sHtML
http://www.blog.fuvxie.cn/Article/details/2123.sHtML
http://www.blog.fuvxie.cn/Article/details/82221.sHtML
http://www.blog.fuvxie.cn/Article/details/941682.sHtML
http://www.blog.fuvxie.cn/Article/details/1252.sHtML
http://www.blog.fuvxie.cn/Article/details/1924.sHtML
http://www.blog.fuvxie.cn/Article/details/4883959.sHtML
http://www.blog.fuvxie.cn/Article/details/40106.sHtML
http://www.blog.fuvxie.cn/Article/details/9904687.sHtML
http://www.blog.fuvxie.cn/Article/details/6970.sHtML
http://www.blog.fuvxie.cn/Article/details/88499.sHtML
http://www.blog.fuvxie.cn/Article/details/5840.sHtML
http://www.blog.fuvxie.cn/Article/details/305071.sHtML
http://www.blog.fuvxie.cn/Article/details/1935.sHtML
http://www.blog.fuvxie.cn/Article/details/15224.sHtML
http://www.blog.fuvxie.cn/Article/details/1060.sHtML
http://www.blog.fuvxie.cn/Article/details/406518.sHtML
http://www.blog.fuvxie.cn/Article/details/296547.sHtML
http://www.blog.fuvxie.cn/Article/details/9471.sHtML
http://www.blog.fuvxie.cn/Article/details/441308.sHtML
http://www.blog.fuvxie.cn/Article/details/4516.sHtML
http://www.blog.fuvxie.cn/Article/details/3465.sHtML
http://www.blog.fuvxie.cn/Article/details/867345.sHtML
http://www.blog.fuvxie.cn/Article/details/25617.sHtML
http://www.blog.fuvxie.cn/Article/details/326231.sHtML
http://www.blog.fuvxie.cn/Article/details/556956.sHtML
http://www.blog.fuvxie.cn/Article/details/39174.sHtML
http://www.blog.fuvxie.cn/Article/details/4987473.sHtML
http://www.blog.fuvxie.cn/Article/details/17143.sHtML
http://www.blog.fuvxie.cn/Article/details/2642.sHtML
http://www.blog.fuvxie.cn/Article/details/384384.sHtML
http://www.blog.fuvxie.cn/Article/details/511719.sHtML
http://www.blog.fuvxie.cn/Article/details/103348.sHtML
http://www.blog.fuvxie.cn/Article/details/83914.sHtML
http://www.blog.fuvxie.cn/Article/details/863544.sHtML
http://www.blog.fuvxie.cn/Article/details/2470.sHtML
http://www.blog.fuvxie.cn/Article/details/728682.sHtML
http://www.blog.fuvxie.cn/Article/details/725994.sHtML
http://www.blog.fuvxie.cn/Article/details/42624.sHtML
http://www.blog.fuvxie.cn/Article/details/70443.sHtML
http://www.blog.fuvxie.cn/Article/details/9271.sHtML
http://www.blog.fuvxie.cn/Article/details/2934941.sHtML
http://www.blog.fuvxie.cn/Article/details/847005.sHtML
http://www.blog.fuvxie.cn/Article/details/3100.sHtML
http://www.blog.fuvxie.cn/Article/details/81572.sHtML
http://www.blog.fuvxie.cn/Article/details/5216.sHtML
http://www.blog.fuvxie.cn/Article/details/0551174.sHtML
http://www.blog.fuvxie.cn/Article/details/581289.sHtML
http://www.blog.fuvxie.cn/Article/details/40130.sHtML
http://www.blog.fuvxie.cn/Article/details/444857.sHtML
http://www.blog.fuvxie.cn/Article/details/4005.sHtML
http://www.blog.fuvxie.cn/Article/details/107192.sHtML
http://www.blog.fuvxie.cn/Article/details/421587.sHtML
http://www.blog.fuvxie.cn/Article/details/128655.sHtML
http://www.blog.fuvxie.cn/Article/details/85277.sHtML
http://www.blog.fuvxie.cn/Article/details/1410835.sHtML
http://www.blog.fuvxie.cn/Article/details/3313085.sHtML
http://www.blog.fuvxie.cn/Article/details/5681.sHtML
http://www.blog.fuvxie.cn/Article/details/4772.sHtML
http://www.blog.fuvxie.cn/Article/details/7211577.sHtML
http://www.blog.fuvxie.cn/Article/details/2151266.sHtML
http://www.blog.fuvxie.cn/Article/details/5366.sHtML
http://www.blog.fuvxie.cn/Article/details/1101455.sHtML
http://www.blog.fuvxie.cn/Article/details/71532.sHtML
http://www.blog.fuvxie.cn/Article/details/6234539.sHtML
http://www.blog.fuvxie.cn/Article/details/698149.sHtML
http://www.blog.fuvxie.cn/Article/details/61555.sHtML
http://www.blog.fuvxie.cn/Article/details/7216.sHtML
http://www.blog.fuvxie.cn/Article/details/9991.sHtML
http://www.blog.fuvxie.cn/Article/details/284925.sHtML
http://www.blog.fuvxie.cn/Article/details/8497182.sHtML
http://www.blog.fuvxie.cn/Article/details/92005.sHtML
http://www.blog.fuvxie.cn/Article/details/57591.sHtML
http://www.blog.fuvxie.cn/Article/details/51905.sHtML
http://www.blog.fuvxie.cn/Article/details/85831.sHtML
http://www.blog.fuvxie.cn/Article/details/72701.sHtML
http://www.blog.fuvxie.cn/Article/details/9902.sHtML
http://www.blog.fuvxie.cn/Article/details/6603.sHtML
http://www.blog.fuvxie.cn/Article/details/68809.sHtML
http://www.blog.fuvxie.cn/Article/details/043968.sHtML
http://www.blog.fuvxie.cn/Article/details/385609.sHtML
http://www.blog.fuvxie.cn/Article/details/7292368.sHtML
http://www.blog.fuvxie.cn/Article/details/06467.sHtML
http://www.blog.fuvxie.cn/Article/details/5096.sHtML
http://www.blog.fuvxie.cn/Article/details/1199.sHtML
http://www.blog.fuvxie.cn/Article/details/6678477.sHtML
http://www.blog.fuvxie.cn/Article/details/416407.sHtML
http://www.blog.fuvxie.cn/Article/details/191069.sHtML
http://www.blog.fuvxie.cn/Article/details/7769537.sHtML
http://www.blog.fuvxie.cn/Article/details/89489.sHtML
http://www.blog.fuvxie.cn/Article/details/945077.sHtML
http://www.blog.fuvxie.cn/Article/details/865430.sHtML
http://www.blog.fuvxie.cn/Article/details/1219424.sHtML
http://www.blog.fuvxie.cn/Article/details/338386.sHtML
http://www.blog.fuvxie.cn/Article/details/4387.sHtML

## 项目结构

```
webarchive-indexer/
├── indexer.py                 # 命令行入口，整合导入、巡检、生成等子命令
├── config.yaml                # 主配置文件，定义数据库路径、巡检间隔、输出目录等
├── requirements.txt           # 生产环境依赖清单
├── dev-requirements.txt       # 开发环境额外依赖（测试、格式化、静态检查）
├── README.md                  # 项目说明文档（即本文档）
├── LICENSE                    # MIT 许可证全文
│
├── core/                      # 核心逻辑模块
│   ├── __init__.py
│   ├── importer.py            # 批量链接导入与解析，支持 CSV/TXT 格式
│   ├── checker.py             # 异步 HTTP 健康检查与状态更新
│   ├── extractor.py           # 基于 BeautifulSoup 的标题/摘要提取
│   └── generator.py           # 使用 Jinja2 渲染静态 HTML 目录页
│
├── storage/                   # 数据持久化层
│   ├── __init__.py
│   ├── database.py            # SQLite 连接池与表结构初始化
│   ├── models.py              # 数据模型定义（Link, Batch, StatusLog）
│   └── migrations/            # 数据库版本迁移脚本
│       └── v1_initial.sql
│
├── utils/                     # 通用工具函数
│   ├── __init__.py
│   ├── logger.py              # 日志配置与分级输出
│   ├── validators.py          # URL 规范化与格式校验
│   └── formatters.py          # 日期、状态码、文件大小等格式化
│
├── templates/                 # Jinja2 HTML 模板
│   ├── base.html              # 基础布局，包含响应式 CSS 框架
│   ├── index.html             # 目录首页，展示链接列表与筛选器
│   └── detail.html            # 单条链接详情页（含状态历史）
│
├── samples/                   # 示例数据与测试用例
│   ├── links_batch_34.txt     # 第 34 批导入示例（即本文档资源列表）
│   └── sample_export.json     # JSON 导出格式参考
│
├── tests/                     # 单元测试与集成测试
│   ├── test_importer.py
│   ├── test_checker.py
│   └── test_extractor.py
│
└── public/                    # 静态站点输出目录（git 忽略，由 generator 生成）
    ├── index.html
    ├── detail/
    ├── css/
    └── js/
```

## 贡献指南

我们欢迎并鼓励社区提交改进与扩展。请遵循以下步骤参与贡献：

1. 查阅 Issue 列表，选择未被认领的功能或缺陷。若为新特性建议，请先创建 Issue 并描述设计思路与使用场景，等待维护者反馈后再开始编码。

2. 从 main 分支创建功能分支（命名格式为 `feature/描述` 或 `fix/描述`），确保所有代码通过 black 格式化与 flake8 静态检查。提交信息请遵循 Conventional Commits 规范。

3. 为核心模块补充单元测试，覆盖率不低于 80%。测试需在 SQLite 内存数据库上运行，避免对开发环境的本地数据文件造成影响。

4. 更新相关文档，包括 README 中的功能说明、配置参考以及 API 注释。对于新增的命令行参数，需同步更新 `docs/` 目录下的使用示例。

5. 提交 Pull Request 至 main 分支，并在描述中关联对应的 Issue 编号。PR 合并前需要通过 CI 流水线（包含测试、格式化与文档构建检查）。重大变更需至少两名维护者审阅。

## 常见问题

**Q：导入大量链接时是否会触发目标网站的限流机制？**

A：项目内置了可配置的请求间隔（默认 500 毫秒）与并发控制（最大 10 个并发）。在巡检模式中，所有请求均携带合理的 User-Agent 头，并遵守 robots.txt 中的 Crawl-delay 指令。建议用户根据自身网络环境调整 `config.yaml` 中的 `checker.rate_limit` 参数。对于频繁出现 429 状态码的域名，可将该域名加入 `checker.whitelist` 并单独设置更长的间隔。

**Q：如何迁移索引数据库到其他服务器？**

A：索引数据存储于单个 SQLite 文件（默认为 `data/index.db`）。迁移时只需将该文件复制到目标服务器的相同路径，并确保 SQLite 版本兼容即可。如需切换为 PostgreSQL 或 MySQL，可参照 `storage/database.py` 中的适配器接口自行扩展，项目核心逻辑与存储层已做解耦设计。建议在迁移前执行 `python indexer.py --export --format json > backup.json` 进行完整导出备份。

**Q：静态生成的 HTML 页面能否支持暗色主题与移动端适配？**

A：生成的静态页面基于响应式 CSS 框架，默认跟随系统配色方案（prefers-color-scheme）。用户也可通过修改 `templates/base.html` 中的 CSS 变量自定义主题色。移动端布局针对屏幕宽度小于 768px 的设备做了导航折叠与表格横向滚动优化，确保在手机和平板上的阅读体验。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:26:27
