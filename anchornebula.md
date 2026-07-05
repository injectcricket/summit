# ResourceBridge

ResourceBridge 是一个面向技术研究、内容聚合与知识工程场景的轻量级外链资源归集平台。该项目定位于帮助个人开发者、研究团队及内容运营者高效管理、检索和分发来源分散的技术文章、博客条目与知识碎片，特别适用于构建私有的知识检索基底或作为内容中台的上游数据管道。

本项目并不试图取代搜索引擎或数据库系统，而是作为结构化资源索引层，提供明确的条目映射与稳定的引用锚点。目标用户包括技术文档撰写者、开源社区维护者、数据分析工程师以及需要长期跟踪特定内容源的科研人员。通过统一的资源清单与清晰的分类导航，ResourceBridge 将大量原始 URL 转化为可维护、可审查、可扩展的知识资产。

## 功能概览

**批量资源导入**：支持一次性收录大量外部 URL，自动完成格式清洗与去重校验，确保条目唯一性与协议一致性。

**分类目录引擎**：内置基于主题标签与来源域名的自动归类逻辑，可将资源按技术领域、内容类型或更新频次划分至不同集合。

**引用状态监控**：对已收录的 URL 进行周期性的可访问性探测，标记失效链接并生成报告，辅助维护资源活性。

**结构化检索接口**：提供基于条目 ID、关键词匹配及正则表达式的查询能力，支持通过命令行工具或 HTTP API 获取资源详情。

**元数据扩展字段**：每条资源可附加备注、优先级、收录时间与关联批次信息，便于多维度筛选与统计。

**快照预览机制**：对于部分不可直接访问的源站，通过内置的文本摘要模块提取关键段落，保留核心语义信息。

## 应用场景

**技术博客归档**：团队内部可将零散收藏的技术文章统一录入 ResourceBridge，通过批次编号与分类标签构建可追溯的学习路径，避免内容散落在浏览器书签或即时通讯记录中。

**内容风控审查**：内容运营人员利用本项目的资源列表，对特定域名下的文章进行集中审查与合规性标注，形成待处理队列，并联动下游审批系统。

**知识图谱底表构建**：数据工程师可将 ResourceBridge 导出的资源清单作为实体链接的候选集合，配合自然语言处理流程提取主题词与关联关系，从而支撑上层推荐或搜索应用。

**长期项目参考存档**：科研项目组在开展文献调研时，通过本项目按批次记录参考链接，在项目周期内可随时回溯早期引用，避免因源站改版或内容迁移导致引用丢失。

## 快速开始

以下指令演示如何从代码仓库获取 ResourceBridge 并启动基础服务。

```bash
git clone https://github.com/resourcebridge/resourcebridge.git
cd resourcebridge
pip install -r requirements.txt
python app.py --init --batch 38
```

执行上述命令后，系统会创建本地 SQLite 数据库，并预置批次编号为 38 的资源占位记录。默认服务监听本机 8080 端口，可通过浏览器访问本地地址查看资源管理界面。

## 安装要求

| 依赖组件 | 必需版本 | 说明 |
|---|---|---|
| Python | 3.9 及以上 | 核心运行环境，用于执行资源管理逻辑与 API 服务 |
| pip | 22.0 及以上 | Python 包依赖管理工具 |
| SQLite | 3.35 及以上 | 默认内置数据库，用于存储资源条目与元数据 |
| Requests | 2.28.0 及以上 | 处理外部 URL 的 HTTP 请求与状态探测 |
| Flask | 2.2.0 及以上 | 提供 Web 管理界面与 RESTful 查询接口 |
| pytest | 7.0.0 及以上 | 单元测试与集成测试框架（仅开发阶段需要） |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|---|---|---|
| 用户手册 | docs/user_guide.md | 如何新增资源、如何批量导入、如何导出清单 |
| 运维指南 | docs/ops_guide.md | 如何配置监控告警、如何迁移数据库、如何优化查询性能 |
| 开发者文档 | docs/dev_guide.md | 如何扩展分类器、如何编写插件、如何提交合并请求 |
| API 参考 | docs/api_reference.md | 端点路径、请求参数、返回格式与状态码含义 |

## 资源列表

### 核心资源条目（第 38 批 / 共 280 批）

以下列表收录了本批次全部 250 个原始 URL。每个条目均按其来源域名与路径结构原样呈现，未作任何协议转换、域名补全或路径规范化处理。

http://www.blog.fuvxie.cn/Article/details/6055468.sHtML
http://www.blog.fuvxie.cn/Article/details/241652.sHtML
http://www.blog.fuvxie.cn/Article/details/497917.sHtML
http://www.blog.fuvxie.cn/Article/details/00481.sHtML
http://www.blog.fuvxie.cn/Article/details/204020.sHtML
http://www.blog.fuvxie.cn/Article/details/602125.sHtML
http://www.blog.fuvxie.cn/Article/details/60572.sHtML
http://www.blog.fuvxie.cn/Article/details/97868.sHtML
http://www.blog.fuvxie.cn/Article/details/6201.sHtML
http://www.blog.fuvxie.cn/Article/details/36596.sHtML
http://www.blog.fuvxie.cn/Article/details/97848.sHtML
http://www.blog.fuvxie.cn/Article/details/1237564.sHtML
http://www.blog.fuvxie.cn/Article/details/3679952.sHtML
http://www.blog.fuvxie.cn/Article/details/3756568.sHtML
http://www.blog.fuvxie.cn/Article/details/64426.sHtML
http://www.blog.fuvxie.cn/Article/details/822934.sHtML
http://www.blog.fuvxie.cn/Article/details/451110.sHtML
http://www.blog.fuvxie.cn/Article/details/58605.sHtML
http://www.blog.fuvxie.cn/Article/details/28731.sHtML
http://www.blog.fuvxie.cn/Article/details/1613.sHtML
http://www.blog.fuvxie.cn/Article/details/52915.sHtML
http://www.blog.fuvxie.cn/Article/details/7341.sHtML
http://www.blog.fuvxie.cn/Article/details/8251656.sHtML
http://www.blog.fuvxie.cn/Article/details/02256.sHtML
http://www.blog.fuvxie.cn/Article/details/71075.sHtML
http://www.blog.fuvxie.cn/Article/details/8224.sHtML
http://www.blog.fuvxie.cn/Article/details/1646355.sHtML
http://www.blog.fuvxie.cn/Article/details/80684.sHtML
http://www.blog.fuvxie.cn/Article/details/1844963.sHtML
http://www.blog.fuvxie.cn/Article/details/0722047.sHtML
http://www.blog.fuvxie.cn/Article/details/067162.sHtML
http://www.blog.fuvxie.cn/Article/details/967426.sHtML
http://www.blog.fuvxie.cn/Article/details/221852.sHtML
http://www.blog.fuvxie.cn/Article/details/84057.sHtML
http://www.blog.fuvxie.cn/Article/details/1525.sHtML
http://www.blog.fuvxie.cn/Article/details/50042.sHtML
http://www.blog.fuvxie.cn/Article/details/7882.sHtML
http://www.blog.fuvxie.cn/Article/details/16130.sHtML
http://www.blog.fuvxie.cn/Article/details/02723.sHtML
http://www.blog.fuvxie.cn/Article/details/94916.sHtML
http://www.blog.fuvxie.cn/Article/details/0060.sHtML
http://www.blog.fuvxie.cn/Article/details/9161682.sHtML
http://www.blog.fuvxie.cn/Article/details/22255.sHtML
http://www.blog.fuvxie.cn/Article/details/49303.sHtML
http://www.blog.fuvxie.cn/Article/details/7257.sHtML
http://www.blog.fuvxie.cn/Article/details/6297.sHtML
http://www.blog.fuvxie.cn/Article/details/10551.sHtML
http://www.blog.fuvxie.cn/Article/details/328285.sHtML
http://www.blog.fuvxie.cn/Article/details/3331527.sHtML
http://www.blog.fuvxie.cn/Article/details/907252.sHtML
http://www.blog.fuvxie.cn/Article/details/52583.sHtML
http://www.blog.fuvxie.cn/Article/details/3328633.sHtML
http://www.blog.fuvxie.cn/Article/details/164730.sHtML
http://www.blog.fuvxie.cn/Article/details/2517.sHtML
http://www.blog.fuvxie.cn/Article/details/060171.sHtML
http://www.blog.fuvxie.cn/Article/details/5645784.sHtML
http://www.blog.fuvxie.cn/Article/details/6611709.sHtML
http://www.blog.fuvxie.cn/Article/details/7442.sHtML
http://www.blog.fuvxie.cn/Article/details/8691026.sHtML
http://www.blog.fuvxie.cn/Article/details/29097.sHtML
http://www.blog.fuvxie.cn/Article/details/4691.sHtML
http://www.blog.fuvxie.cn/Article/details/6564320.sHtML
http://www.blog.fuvxie.cn/Article/details/386586.sHtML
http://www.blog.fuvxie.cn/Article/details/954698.sHtML
http://www.blog.fuvxie.cn/Article/details/19819.sHtML
http://www.blog.fuvxie.cn/Article/details/6131855.sHtML
http://www.blog.fuvxie.cn/Article/details/91115.sHtML
http://www.blog.fuvxie.cn/Article/details/9843.sHtML
http://www.blog.fuvxie.cn/Article/details/1897185.sHtML
http://www.blog.fuvxie.cn/Article/details/166529.sHtML
http://www.blog.fuvxie.cn/Article/details/0260546.sHtML
http://www.blog.fuvxie.cn/Article/details/351686.sHtML
http://www.blog.fuvxie.cn/Article/details/19662.sHtML
http://www.blog.fuvxie.cn/Article/details/7150585.sHtML
http://www.blog.fuvxie.cn/Article/details/411762.sHtML
http://www.blog.fuvxie.cn/Article/details/27760.sHtML
http://www.blog.fuvxie.cn/Article/details/4777.sHtML
http://www.blog.fuvxie.cn/Article/details/0478846.sHtML
http://www.blog.fuvxie.cn/Article/details/7582.sHtML
http://www.blog.fuvxie.cn/Article/details/1460126.sHtML
http://www.blog.fuvxie.cn/Article/details/02797.sHtML
http://www.blog.fuvxie.cn/Article/details/2277201.sHtML
http://www.blog.fuvxie.cn/Article/details/470878.sHtML
http://www.blog.fuvxie.cn/Article/details/656067.sHtML
http://www.blog.fuvxie.cn/Article/details/4046472.sHtML
http://www.blog.fuvxie.cn/Article/details/746668.sHtML
http://www.blog.fuvxie.cn/Article/details/77391.sHtML
http://www.blog.fuvxie.cn/Article/details/8488.sHtML
http://www.blog.fuvxie.cn/Article/details/563625.sHtML
http://www.blog.fuvxie.cn/Article/details/4166456.sHtML
http://www.blog.fuvxie.cn/Article/details/28546.sHtML
http://www.blog.fuvxie.cn/Article/details/069306.sHtML
http://www.blog.fuvxie.cn/Article/details/5438.sHtML
http://www.blog.fuvxie.cn/Article/details/5985243.sHtML
http://www.blog.fuvxie.cn/Article/details/0881651.sHtML
http://www.blog.fuvxie.cn/Article/details/4175.sHtML
http://www.blog.fuvxie.cn/Article/details/46060.sHtML
http://www.blog.fuvxie.cn/Article/details/65809.sHtML
http://www.blog.fuvxie.cn/Article/details/521651.sHtML
http://www.blog.fuvxie.cn/Article/details/0946468.sHtML
http://www.blog.fuvxie.cn/Article/details/7995831.sHtML
http://www.blog.fuvxie.cn/Article/details/298713.sHtML
http://www.blog.fuvxie.cn/Article/details/679956.sHtML
http://www.blog.fuvxie.cn/Article/details/0275758.sHtML
http://www.blog.fuvxie.cn/Article/details/33117.sHtML
http://www.blog.fuvxie.cn/Article/details/5489875.sHtML
http://www.blog.fuvxie.cn/Article/details/12615.sHtML
http://www.blog.fuvxie.cn/Article/details/8307177.sHtML
http://www.blog.fuvxie.cn/Article/details/80539.sHtML
http://www.blog.fuvxie.cn/Article/details/3993.sHtML
http://www.blog.fuvxie.cn/Article/details/2001.sHtML
http://www.blog.fuvxie.cn/Article/details/178444.sHtML
http://www.blog.fuvxie.cn/Article/details/9306.sHtML
http://www.blog.fuvxie.cn/Article/details/58361.sHtML
http://www.blog.fuvxie.cn/Article/details/97391.sHtML
http://www.blog.fuvxie.cn/Article/details/4592.sHtML
http://www.blog.fuvxie.cn/Article/details/250542.sHtML
http://www.blog.fuvxie.cn/Article/details/35342.sHtML
http://www.blog.fuvxie.cn/Article/details/444638.sHtML
http://www.blog.fuvxie.cn/Article/details/5836461.sHtML
http://www.blog.fuvxie.cn/Article/details/79717.sHtML
http://www.blog.fuvxie.cn/Article/details/7316.sHtML
http://www.blog.fuvxie.cn/Article/details/0868.sHtML
http://www.blog.fuvxie.cn/Article/details/710187.sHtML
http://www.blog.fuvxie.cn/Article/details/6851237.sHtML
http://www.blog.fuvxie.cn/Article/details/445062.sHtML
http://www.blog.fuvxie.cn/Article/details/998014.sHtML
http://www.blog.fuvxie.cn/Article/details/6278620.sHtML
http://www.blog.fuvxie.cn/Article/details/4024867.sHtML
http://www.blog.fuvxie.cn/Article/details/25228.sHtML
http://www.blog.fuvxie.cn/Article/details/12143.sHtML
http://www.blog.fuvxie.cn/Article/details/9244441.sHtML
http://www.blog.fuvxie.cn/Article/details/3906.sHtML
http://www.blog.fuvxie.cn/Article/details/8084919.sHtML
http://www.blog.fuvxie.cn/Article/details/467226.sHtML
http://www.blog.fuvxie.cn/Article/details/05048.sHtML
http://www.blog.fuvxie.cn/Article/details/09389.sHtML
http://www.blog.fuvxie.cn/Article/details/9570013.sHtML
http://www.blog.fuvxie.cn/Article/details/970179.sHtML
http://www.blog.fuvxie.cn/Article/details/0029.sHtML
http://www.blog.fuvxie.cn/Article/details/5654.sHtML
http://www.blog.fuvxie.cn/Article/details/31025.sHtML
http://www.blog.fuvxie.cn/Article/details/3131488.sHtML
http://www.blog.fuvxie.cn/Article/details/36946.sHtML
http://www.blog.fuvxie.cn/Article/details/623593.sHtML
http://www.blog.fuvxie.cn/Article/details/89739.sHtML
http://www.blog.fuvxie.cn/Article/details/02163.sHtML
http://www.blog.fuvxie.cn/Article/details/307235.sHtML
http://www.blog.fuvxie.cn/Article/details/399509.sHtML
http://www.blog.fuvxie.cn/Article/details/2779006.sHtML
http://www.blog.fuvxie.cn/Article/details/5245.sHtML
http://www.blog.fuvxie.cn/Article/details/6787.sHtML
http://www.blog.fuvxie.cn/Article/details/6281305.sHtML
http://www.blog.fuvxie.cn/Article/details/242620.sHtML
http://www.blog.fuvxie.cn/Article/details/78280.sHtML
http://www.blog.fuvxie.cn/Article/details/34336.sHtML
http://www.blog.fuvxie.cn/Article/details/4381.sHtML
http://www.blog.fuvxie.cn/Article/details/6828849.sHtML
http://www.blog.fuvxie.cn/Article/details/255210.sHtML
http://www.blog.fuvxie.cn/Article/details/41056.sHtML
http://www.blog.fuvxie.cn/Article/details/74251.sHtML
http://www.blog.fuvxie.cn/Article/details/725416.sHtML
http://www.blog.fuvxie.cn/Article/details/5621300.sHtML
http://www.blog.fuvxie.cn/Article/details/688787.sHtML
http://www.blog.fuvxie.cn/Article/details/72277.sHtML
http://www.blog.fuvxie.cn/Article/details/8279185.sHtML
http://www.blog.fuvxie.cn/Article/details/49202.sHtML
http://www.blog.fuvxie.cn/Article/details/917078.sHtML
http://www.blog.fuvxie.cn/Article/details/1388.sHtML
http://www.blog.fuvxie.cn/Article/details/2348972.sHtML
http://www.blog.fuvxie.cn/Article/details/380964.sHtML
http://www.blog.fuvxie.cn/Article/details/921388.sHtML
http://www.blog.fuvxie.cn/Article/details/07291.sHtML
http://www.blog.fuvxie.cn/Article/details/218895.sHtML
http://www.blog.fuvxie.cn/Article/details/876474.sHtML
http://www.blog.fuvxie.cn/Article/details/496018.sHtML
http://www.blog.fuvxie.cn/Article/details/5768079.sHtML
http://www.blog.fuvxie.cn/Article/details/18736.sHtML
http://www.blog.fuvxie.cn/Article/details/1300960.sHtML
http://www.blog.fuvxie.cn/Article/details/07143.sHtML
http://www.blog.fuvxie.cn/Article/details/06332.sHtML
http://www.blog.fuvxie.cn/Article/details/1174678.sHtML
http://www.blog.fuvxie.cn/Article/details/485216.sHtML
http://www.blog.fuvxie.cn/Article/details/3134572.sHtML
http://www.blog.fuvxie.cn/Article/details/70615.sHtML
http://www.blog.fuvxie.cn/Article/details/22288.sHtML
http://www.blog.fuvxie.cn/Article/details/7936.sHtML
http://www.blog.fuvxie.cn/Article/details/55507.sHtML
http://www.blog.fuvxie.cn/Article/details/3426339.sHtML
http://www.blog.fuvxie.cn/Article/details/59987.sHtML
http://www.blog.fuvxie.cn/Article/details/6972.sHtML
http://www.blog.fuvxie.cn/Article/details/2705064.sHtML
http://www.blog.fuvxie.cn/Article/details/4516917.sHtML
http://www.blog.fuvxie.cn/Article/details/7468.sHtML
http://www.blog.fuvxie.cn/Article/details/7456.sHtML
http://www.blog.fuvxie.cn/Article/details/020262.sHtML
http://www.blog.fuvxie.cn/Article/details/0747122.sHtML
http://www.blog.fuvxie.cn/Article/details/31023.sHtML
http://www.blog.fuvxie.cn/Article/details/218344.sHtML
http://www.blog.fuvxie.cn/Article/details/324131.sHtML
http://www.blog.fuvxie.cn/Article/details/9600568.sHtML
http://www.blog.fuvxie.cn/Article/details/1401.sHtML
http://www.blog.fuvxie.cn/Article/details/62375.sHtML
http://www.blog.fuvxie.cn/Article/details/1940.sHtML
http://www.blog.fuvxie.cn/Article/details/107472.sHtML
http://www.blog.fuvxie.cn/Article/details/869861.sHtML
http://www.blog.fuvxie.cn/Article/details/033041.sHtML
http://www.blog.fuvxie.cn/Article/details/906482.sHtML
http://www.blog.fuvxie.cn/Article/details/39288.sHtML
http://www.blog.fuvxie.cn/Article/details/8335.sHtML
http://www.blog.fuvxie.cn/Article/details/053192.sHtML
http://www.blog.fuvxie.cn/Article/details/3474601.sHtML
http://www.blog.fuvxie.cn/Article/details/1341.sHtML
http://www.blog.fuvxie.cn/Article/details/831551.sHtML
http://www.blog.fuvxie.cn/Article/details/0449.sHtML
http://www.blog.fuvxie.cn/Article/details/1099992.sHtML
http://www.blog.fuvxie.cn/Article/details/44248.sHtML
http://www.blog.fuvxie.cn/Article/details/967826.sHtML
http://www.blog.fuvxie.cn/Article/details/206077.sHtML
http://www.blog.fuvxie.cn/Article/details/435676.sHtML
http://www.blog.fuvxie.cn/Article/details/29079.sHtML
http://www.blog.fuvxie.cn/Article/details/0247.sHtML
http://www.blog.fuvxie.cn/Article/details/68439.sHtML
http://www.blog.fuvxie.cn/Article/details/78508.sHtML
http://www.blog.fuvxie.cn/Article/details/8849.sHtML
http://www.blog.fuvxie.cn/Article/details/02510.sHtML
http://www.blog.fuvxie.cn/Article/details/5060664.sHtML
http://www.blog.fuvxie.cn/Article/details/0358812.sHtML
http://www.blog.fuvxie.cn/Article/details/982385.sHtML
http://www.blog.fuvxie.cn/Article/details/230978.sHtML
http://www.blog.fuvxie.cn/Article/details/775362.sHtML
http://www.blog.fuvxie.cn/Article/details/2229.sHtML
http://www.blog.fuvxie.cn/Article/details/096093.sHtML
http://www.blog.fuvxie.cn/Article/details/6515.sHtML
http://www.blog.fuvxie.cn/Article/details/34145.sHtML
http://www.blog.fuvxie.cn/Article/details/3292.sHtML
http://www.blog.fuvxie.cn/Article/details/8998.sHtML
http://www.blog.fuvxie.cn/Article/details/57581.sHtML
http://www.blog.fuvxie.cn/Article/details/80572.sHtML
http://www.blog.fuvxie.cn/Article/details/8447.sHtML
http://www.blog.fuvxie.cn/Article/details/60920.sHtML
http://www.blog.fuvxie.cn/Article/details/05800.sHtML
http://www.blog.fuvxie.cn/Article/details/419131.sHtML
http://www.blog.fuvxie.cn/Article/details/57034.sHtML
http://www.blog.fuvxie.cn/Article/details/1117.sHtML
http://www.blog.fuvxie.cn/Article/details/56659.sHtML
http://www.blog.fuvxie.cn/Article/details/9965.sHtML
http://www.blog.fuvxie.cn/Article/details/49989.sHtML
http://www.blog.fuvxie.cn/Article/details/040784.sHtML
http://www.blog.fuvxie.cn/Article/details/594939.sHtML

## 项目结构

```
resourcebridge/
├── app.py                         # 主入口文件，初始化 Flask 应用与路由注册
├── requirements.txt               # Python 依赖清单，锁定各库版本号
├── config/
│   ├── settings.py                # 全局配置项（数据库路径、监听端口、日志级别）
│   └── batch_meta.json            # 批次元数据记录，包含当前批次编号与总量
├── core/
│   ├── loader.py                  # 资源加载器，解析外部列表并写入数据库
│   ├── classifier.py              # 分类引擎，基于域名与路径规则分配标签
│   └── monitor.py                 # 状态监控模块，周期性探测 URL 可访问性
├── api/
│   ├── routes.py                  # RESTful 端点定义（查询、新增、删除、统计）
│   └── serializer.py              # 响应数据序列化与格式转换
├── web/
│   ├── static/                    # 静态资源目录（层叠样式表与客户端脚本）
│   └── templates/                 # Jinja2 模板文件（管理界面与结果展示页）
├── tests/
│   ├── test_loader.py             # 加载器单元测试用例
│   ├── test_classifier.py         # 分类器逻辑覆盖率测试
│   └── test_monitor.py            # 监控模块模拟探测测试
└── docs/                          # 完整文档体系，包含用户手册与 API 参考
```

## 贡献指南

1. 查阅开发者文档 docs/dev_guide.md 了解核心模块的设计约定与代码风格规范，确保新增代码与现有架构保持一致。

2. 在 tests 目录下为新增功能或修复补丁编写对应的测试用例，要求测试覆盖率达到 90% 以上，并确保所有现有测试通过。

3. 提交合并请求前，请运行代码格式化工具 black 与静态检查工具 flake8，清理不符合规范的语法与导入语句。

4. 对于涉及资源列表格式或数据库表结构的变更，需要同步更新 docs/user_guide.md 中的示例说明与字段释义。

5. 提交信息采用语义化格式，标题行注明变更类型（feat、fix、docs、refactor），正文描述问题背景与解决方案。

## 常见问题

**Q：资源列表中的 URL 访问失败时，系统如何处理？**
A：监控模块会周期性发送 HEAD 请求验证资源活性。对于连续三次超时或返回 4xx/5xx 状态码的条目，系统将其标记为“失效”并记录最后检测时间，但不会自动删除条目。用户可在管理界面按状态过滤并批量导出失效列表，方便人工复核。

**Q：如何将本项目的资源数据迁移至其他数据库系统？**
A：核心存储层基于 SQLAlchemy ORM 实现，支持切换至 PostgreSQL 或 MySQL。用户需在 config/settings.py 中修改数据库连接串，并执行迁移脚本迁移现有表结构。详细步骤参考 docs/ops_guide.md 中的数据库迁移章节。

**Q：批次编号的作用是什么，是否可以跨批次检索？**
A：批次编号用于标识资源的收录批次，便于按时间维度回溯。跨批次检索可通过 API 的 batch 参数组合查询，或使用前端界面的高级筛选功能。系统默认按批次倒序排列结果，最新收录的资源优先展示。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:26:28
