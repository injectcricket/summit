# ResourceBridge

ResourceBridge 是一个面向技术研究者和内容聚合者的结构化外链资源导航工具。该项目定位于将散落在各处的高价值技术文章、教程和文档进行统一的索引化整理，通过标准化的 URL 收录机制与轻量级元数据标注，帮助用户快速定位特定领域的技术资料。

ResourceBridge 不提供内容托管或镜像存储，而是作为一层高效的资源路由层，将用户引导至原始发布站点。项目适用于日常技术阅读、研究文献管理、团队知识库构建以及自动化爬虫采集策略的参考样例。

## 功能概览

**URL 标准化收录**：所有外链资源均以原始 URL 形式收录，不进行重定向、缩址或协议升级，保证链接的原始可追溯性。

**多级分类标签**：每一条资源支持通过目录结构进行粗粒度分类（如 Article / Documentation / Tutorial），便于按类型筛选。

**批量导入与校验**：提供批量 URL 导入接口，系统自动对链接进行可达性校验并标记异常状态。

**资源版本追踪**：记录每条资源的收录时间与最后校验时间，支持检测目标页面是否发生变更或失效。

**只读数据输出**：项目本身不提供写接口，所有资源列表以纯 Markdown 或 JSON 格式输出，适合静态站点生成或文档系统集成。

**零运行时依赖查阅**：项目运行仅需标准 Python 环境与系统自带工具，不依赖外部数据库或缓存服务。

## 应用场景

技术博客聚合阅读：技术爱好者可将 ResourceBridge 作为个人阅读列表的起点，通过分类索引快速浏览特定主题的文章，避免在多个站点之间反复切换。

团队知识库资源沉淀：开发团队可在内部文档系统中嵌入 ResourceBridge 生成的资源列表，统一存放团队推荐阅读的外链资料，降低新成员的学习路径查找成本。

爬虫策略参考样例：数据采集工程师可参考本项目的 URL 命名模式与目录层级设计，为自身采集任务构建合理的 URL 发现与去重策略。

自动化监控触发点：运维人员可基于本项目的资源列表编写监控脚本，定时检测目标链接的响应状态，及时发现内容下线或域名过期情况。

## 快速开始

以下命令演示如何将 ResourceBridge 仓库克隆至本地并启动基础服务。

```bash
# 克隆仓库
git clone https://github.com/resourcebridge/resourcebridge.git

# 进入项目目录
cd resourcebridge

# 安装依赖（使用 pip 与 requirements.txt）
pip install -r requirements.txt

# 运行资源校验脚本，生成当前资源列表的状态报告
python scripts/validate_links.py --input resources/master_list.txt --output reports/status.json
```

## 安装要求

| 依赖 | 必需版本 | 说明 |
|------|----------|------|
| Python | 3.8 及以上 | 运行时核心解释器 |
| pip | 20.0 及以上 | Python 包管理工具 |
| requests | 2.25.0 及以上 | 用于 HTTP 请求与链接校验 |
| markdown | 3.3.0 及以上 | 用于生成资源列表的 Markdown 输出 |
| PyYAML | 5.4.0 及以上 | 用于解析配置文件（可选） |
| git | 2.25.0 及以上 | 版本控制与仓库克隆 |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|------|------|------------|
| 用户手册 | docs/user_guide.md | 如何使用 ResourceBridge 进行资源检索和分类筛选 |
| 维护指南 | docs/maintainer_guide.md | 如何新增资源、更新失效链接以及批量导入 |
| 设计说明 | docs/design.md | 资源索引的数据结构设计、URL 处理策略与扩展性考量 |
| API 参考 | docs/api_reference.md | 校验接口的输出格式、错误码及调用示例 |

## 资源列表

### 技术文章与教程资源

http://www.blog.cmcvrr.cn/Article/details/242937.sHtML
http://www.blog.cmcvrr.cn/Article/details/203647.sHtML
http://www.blog.cmcvrr.cn/Article/details/73751.sHtML
http://www.blog.cmcvrr.cn/Article/details/925558.sHtML
http://www.blog.cmcvrr.cn/Article/details/78929.sHtML
http://www.blog.cmcvrr.cn/Article/details/8162831.sHtML
http://www.blog.cmcvrr.cn/Article/details/01277.sHtML
http://www.blog.cmcvrr.cn/Article/details/18981.sHtML
http://www.blog.cmcvrr.cn/Article/details/5832662.sHtML
http://www.blog.cmcvrr.cn/Article/details/26277.sHtML
http://www.blog.cmcvrr.cn/Article/details/286179.sHtML
http://www.blog.cmcvrr.cn/Article/details/0263.sHtML
http://www.blog.cmcvrr.cn/Article/details/92318.sHtML
http://www.blog.cmcvrr.cn/Article/details/2626448.sHtML
http://www.blog.cmcvrr.cn/Article/details/9235840.sHtML
http://www.blog.cmcvrr.cn/Article/details/6792147.sHtML
http://www.blog.cmcvrr.cn/Article/details/6073888.sHtML
http://www.blog.cmcvrr.cn/Article/details/8281658.sHtML
http://www.blog.cmcvrr.cn/Article/details/78397.sHtML
http://www.blog.cmcvrr.cn/Article/details/16274.sHtML
http://www.blog.cmcvrr.cn/Article/details/6396744.sHtML
http://www.blog.cmcvrr.cn/Article/details/954003.sHtML
http://www.blog.cmcvrr.cn/Article/details/81679.sHtML
http://www.blog.cmcvrr.cn/Article/details/4619952.sHtML
http://www.blog.cmcvrr.cn/Article/details/3510282.sHtML
http://www.blog.cmcvrr.cn/Article/details/82929.sHtML
http://www.blog.cmcvrr.cn/Article/details/376790.sHtML
http://www.blog.cmcvrr.cn/Article/details/8064.sHtML
http://www.blog.cmcvrr.cn/Article/details/4193.sHtML
http://www.blog.cmcvrr.cn/Article/details/292626.sHtML
http://www.blog.cmcvrr.cn/Article/details/6955.sHtML
http://www.blog.cmcvrr.cn/Article/details/879181.sHtML
http://www.blog.cmcvrr.cn/Article/details/8080540.sHtML
http://www.blog.cmcvrr.cn/Article/details/15699.sHtML
http://www.blog.cmcvrr.cn/Article/details/48518.sHtML
http://www.blog.cmcvrr.cn/Article/details/9970736.sHtML
http://www.blog.cmcvrr.cn/Article/details/7891.sHtML
http://www.blog.cmcvrr.cn/Article/details/9648.sHtML
http://www.blog.cmcvrr.cn/Article/details/2777.sHtML
http://www.blog.cmcvrr.cn/Article/details/5012.sHtML
http://www.blog.cmcvrr.cn/Article/details/543173.sHtML
http://www.blog.cmcvrr.cn/Article/details/70793.sHtML
http://www.blog.cmcvrr.cn/Article/details/8105.sHtML
http://www.blog.cmcvrr.cn/Article/details/21317.sHtML
http://www.blog.cmcvrr.cn/Article/details/383872.sHtML
http://www.blog.cmcvrr.cn/Article/details/0498.sHtML
http://www.blog.cmcvrr.cn/Article/details/7656198.sHtML
http://www.blog.cmcvrr.cn/Article/details/6292.sHtML
http://www.blog.cmcvrr.cn/Article/details/2809584.sHtML
http://www.blog.cmcvrr.cn/Article/details/723541.sHtML
http://www.blog.cmcvrr.cn/Article/details/127969.sHtML
http://www.blog.cmcvrr.cn/Article/details/461128.sHtML
http://www.blog.cmcvrr.cn/Article/details/9944.sHtML
http://www.blog.cmcvrr.cn/Article/details/57178.sHtML
http://www.blog.cmcvrr.cn/Article/details/31372.sHtML
http://www.blog.cmcvrr.cn/Article/details/6053.sHtML
http://www.blog.cmcvrr.cn/Article/details/0479473.sHtML
http://www.blog.cmcvrr.cn/Article/details/049018.sHtML
http://www.blog.cmcvrr.cn/Article/details/2646.sHtML
http://www.blog.cmcvrr.cn/Article/details/9350958.sHtML
http://www.blog.cmcvrr.cn/Article/details/3058097.sHtML
http://www.blog.cmcvrr.cn/Article/details/1286.sHtML
http://www.blog.cmcvrr.cn/Article/details/9854.sHtML
http://www.blog.cmcvrr.cn/Article/details/6962.sHtML
http://www.blog.cmcvrr.cn/Article/details/5884.sHtML
http://www.blog.cmcvrr.cn/Article/details/19453.sHtML
http://www.blog.cmcvrr.cn/Article/details/8497.sHtML
http://www.blog.cmcvrr.cn/Article/details/8886019.sHtML
http://www.blog.cmcvrr.cn/Article/details/4013.sHtML
http://www.blog.cmcvrr.cn/Article/details/5716.sHtML
http://www.blog.cmcvrr.cn/Article/details/3282058.sHtML
http://www.blog.cmcvrr.cn/Article/details/3428.sHtML
http://www.blog.cmcvrr.cn/Article/details/706222.sHtML
http://www.blog.cmcvrr.cn/Article/details/8560071.sHtML
http://www.blog.cmcvrr.cn/Article/details/65990.sHtML
http://www.blog.cmcvrr.cn/Article/details/5864.sHtML
http://www.blog.cmcvrr.cn/Article/details/579876.sHtML
http://www.blog.cmcvrr.cn/Article/details/923361.sHtML
http://www.blog.cmcvrr.cn/Article/details/8662.sHtML
http://www.blog.cmcvrr.cn/Article/details/8651758.sHtML
http://www.blog.cmcvrr.cn/Article/details/50487.sHtML
http://www.blog.cmcvrr.cn/Article/details/140338.sHtML
http://www.blog.cmcvrr.cn/Article/details/1451.sHtML
http://www.blog.cmcvrr.cn/Article/details/220368.sHtML
http://www.blog.cmcvrr.cn/Article/details/6948.sHtML
http://www.blog.cmcvrr.cn/Article/details/44662.sHtML
http://www.blog.cmcvrr.cn/Article/details/546992.sHtML
http://www.blog.cmcvrr.cn/Article/details/55289.sHtML
http://www.blog.cmcvrr.cn/Article/details/83376.sHtML
http://www.blog.cmcvrr.cn/Article/details/971177.sHtML
http://www.blog.cmcvrr.cn/Article/details/8090.sHtML
http://www.blog.cmcvrr.cn/Article/details/40094.sHtML
http://www.blog.cmcvrr.cn/Article/details/28008.sHtML
http://www.blog.cmcvrr.cn/Article/details/6982.sHtML
http://www.blog.cmcvrr.cn/Article/details/0569045.sHtML
http://www.blog.cmcvrr.cn/Article/details/3712168.sHtML
http://www.blog.cmcvrr.cn/Article/details/53660.sHtML
http://www.blog.cmcvrr.cn/Article/details/6073.sHtML
http://www.blog.cmcvrr.cn/Article/details/5745985.sHtML
http://www.blog.cmcvrr.cn/Article/details/952633.sHtML
http://www.blog.cmcvrr.cn/Article/details/0018334.sHtML
http://www.blog.cmcvrr.cn/Article/details/33503.sHtML
http://www.blog.cmcvrr.cn/Article/details/2132970.sHtML
http://www.blog.cmcvrr.cn/Article/details/0669789.sHtML
http://www.blog.cmcvrr.cn/Article/details/14161.sHtML
http://www.blog.cmcvrr.cn/Article/details/955803.sHtML
http://www.blog.cmcvrr.cn/Article/details/95918.sHtML
http://www.blog.cmcvrr.cn/Article/details/5509.sHtML
http://www.blog.cmcvrr.cn/Article/details/20420.sHtML
http://www.blog.cmcvrr.cn/Article/details/620666.sHtML
http://www.blog.cmcvrr.cn/Article/details/7044398.sHtML
http://www.blog.cmcvrr.cn/Article/details/8992.sHtML
http://www.blog.cmcvrr.cn/Article/details/277488.sHtML
http://www.blog.cmcvrr.cn/Article/details/31186.sHtML
http://www.blog.cmcvrr.cn/Article/details/532774.sHtML
http://www.blog.cmcvrr.cn/Article/details/6949126.sHtML
http://www.blog.cmcvrr.cn/Article/details/7268.sHtML
http://www.blog.cmcvrr.cn/Article/details/933172.sHtML
http://www.blog.cmcvrr.cn/Article/details/08160.sHtML
http://www.blog.cmcvrr.cn/Article/details/5341364.sHtML
http://www.blog.cmcvrr.cn/Article/details/577057.sHtML
http://www.blog.cmcvrr.cn/Article/details/7750.sHtML
http://www.blog.cmcvrr.cn/Article/details/71665.sHtML
http://www.blog.cmcvrr.cn/Article/details/0675.sHtML
http://www.blog.cmcvrr.cn/Article/details/5949027.sHtML
http://www.blog.cmcvrr.cn/Article/details/401707.sHtML
http://www.blog.cmcvrr.cn/Article/details/485717.sHtML
http://www.blog.cmcvrr.cn/Article/details/4472679.sHtML
http://www.blog.cmcvrr.cn/Article/details/38870.sHtML
http://www.blog.cmcvrr.cn/Article/details/72772.sHtML
http://www.blog.cmcvrr.cn/Article/details/262873.sHtML
http://www.blog.cmcvrr.cn/Article/details/29832.sHtML
http://www.blog.cmcvrr.cn/Article/details/9323908.sHtML
http://www.blog.cmcvrr.cn/Article/details/140431.sHtML
http://www.blog.cmcvrr.cn/Article/details/96787.sHtML
http://www.blog.cmcvrr.cn/Article/details/85009.sHtML
http://www.blog.cmcvrr.cn/Article/details/195342.sHtML
http://www.blog.cmcvrr.cn/Article/details/2857.sHtML
http://www.blog.cmcvrr.cn/Article/details/1649.sHtML
http://www.blog.cmcvrr.cn/Article/details/0289427.sHtML
http://www.blog.cmcvrr.cn/Article/details/7144078.sHtML
http://www.blog.cmcvrr.cn/Article/details/1900.sHtML
http://www.blog.cmcvrr.cn/Article/details/59960.sHtML
http://www.blog.cmcvrr.cn/Article/details/8320658.sHtML
http://www.blog.cmcvrr.cn/Article/details/326072.sHtML
http://www.blog.cmcvrr.cn/Article/details/5842379.sHtML
http://www.blog.cmcvrr.cn/Article/details/68821.sHtML
http://www.blog.cmcvrr.cn/Article/details/0439.sHtML
http://www.blog.cmcvrr.cn/Article/details/518051.sHtML
http://www.blog.cmcvrr.cn/Article/details/95049.sHtML
http://www.blog.cmcvrr.cn/Article/details/692587.sHtML
http://www.blog.cmcvrr.cn/Article/details/8392850.sHtML
http://www.blog.cmcvrr.cn/Article/details/0520150.sHtML
http://www.blog.cmcvrr.cn/Article/details/9506.sHtML
http://www.blog.cmcvrr.cn/Article/details/7160601.sHtML
http://www.blog.cmcvrr.cn/Article/details/53910.sHtML
http://www.blog.cmcvrr.cn/Article/details/810962.sHtML
http://www.blog.cmcvrr.cn/Article/details/993517.sHtML
http://www.blog.cmcvrr.cn/Article/details/806046.sHtML
http://www.blog.cmcvrr.cn/Article/details/211133.sHtML
http://www.blog.cmcvrr.cn/Article/details/9918424.sHtML
http://www.blog.cmcvrr.cn/Article/details/0671.sHtML
http://www.blog.cmcvrr.cn/Article/details/897344.sHtML
http://www.blog.cmcvrr.cn/Article/details/9888522.sHtML
http://www.blog.cmcvrr.cn/Article/details/5732956.sHtML
http://www.blog.cmcvrr.cn/Article/details/1934.sHtML
http://www.blog.cmcvrr.cn/Article/details/1922215.sHtML
http://www.blog.cmcvrr.cn/Article/details/538987.sHtML
http://www.blog.cmcvrr.cn/Article/details/5089.sHtML
http://www.blog.cmcvrr.cn/Article/details/43252.sHtML
http://www.blog.cmcvrr.cn/Article/details/265917.sHtML
http://www.blog.cmcvrr.cn/Article/details/13411.sHtML
http://www.blog.cmcvrr.cn/Article/details/7569.sHtML
http://www.blog.cmcvrr.cn/Article/details/58796.sHtML
http://www.blog.cmcvrr.cn/Article/details/03636.sHtML
http://www.blog.cmcvrr.cn/Article/details/599376.sHtML
http://www.blog.cmcvrr.cn/Article/details/8821.sHtML
http://www.blog.cmcvrr.cn/Article/details/987175.sHtML
http://www.blog.cmcvrr.cn/Article/details/74658.sHtML
http://www.blog.cmcvrr.cn/Article/details/3287771.sHtML
http://www.blog.cmcvrr.cn/Article/details/905915.sHtML
http://www.blog.cmcvrr.cn/Article/details/09046.sHtML
http://www.blog.cmcvrr.cn/Article/details/538219.sHtML
http://www.blog.cmcvrr.cn/Article/details/90044.sHtML
http://www.blog.cmcvrr.cn/Article/details/733575.sHtML
http://www.blog.cmcvrr.cn/Article/details/3948243.sHtML
http://www.blog.cmcvrr.cn/Article/details/3045415.sHtML
http://www.blog.cmcvrr.cn/Article/details/867916.sHtML
http://www.blog.cmcvrr.cn/Article/details/55217.sHtML
http://www.blog.cmcvrr.cn/Article/details/65518.sHtML
http://www.blog.cmcvrr.cn/Article/details/37335.sHtML
http://www.blog.cmcvrr.cn/Article/details/150701.sHtML
http://www.blog.cmcvrr.cn/Article/details/825311.sHtML
http://www.blog.cmcvrr.cn/Article/details/1886.sHtML
http://www.blog.cmcvrr.cn/Article/details/67508.sHtML
http://www.blog.cmcvrr.cn/Article/details/945936.sHtML
http://www.blog.cmcvrr.cn/Article/details/605261.sHtML
http://www.blog.cmcvrr.cn/Article/details/700577.sHtML
http://www.blog.cmcvrr.cn/Article/details/2511.sHtML
http://www.blog.cmcvrr.cn/Article/details/663266.sHtML
http://www.blog.cmcvrr.cn/Article/details/1958.sHtML
http://www.blog.cmcvrr.cn/Article/details/3930.sHtML
http://www.blog.cmcvrr.cn/Article/details/19614.sHtML
http://www.blog.cmcvrr.cn/Article/details/32660.sHtML
http://www.blog.cmcvrr.cn/Article/details/092895.sHtML
http://www.blog.cmcvrr.cn/Article/details/42799.sHtML
http://www.blog.cmcvrr.cn/Article/details/5207837.sHtML
http://www.blog.cmcvrr.cn/Article/details/66172.sHtML
http://www.blog.cmcvrr.cn/Article/details/0111.sHtML
http://www.blog.cmcvrr.cn/Article/details/58478.sHtML
http://www.blog.cmcvrr.cn/Article/details/42002.sHtML
http://www.blog.cmcvrr.cn/Article/details/50001.sHtML
http://www.blog.cmcvrr.cn/Article/details/7352.sHtML
http://www.blog.cmcvrr.cn/Article/details/8784550.sHtML
http://www.blog.cmcvrr.cn/Article/details/207189.sHtML
http://www.blog.cmcvrr.cn/Article/details/888977.sHtML
http://www.blog.cmcvrr.cn/Article/details/735412.sHtML
http://www.blog.cmcvrr.cn/Article/details/9966101.sHtML
http://www.blog.cmcvrr.cn/Article/details/8578884.sHtML
http://www.blog.cmcvrr.cn/Article/details/488254.sHtML
http://www.blog.cmcvrr.cn/Article/details/5252372.sHtML
http://www.blog.cmcvrr.cn/Article/details/1664.sHtML
http://www.blog.cmcvrr.cn/Article/details/8187.sHtML
http://www.blog.cmcvrr.cn/Article/details/5994997.sHtML
http://www.blog.cmcvrr.cn/Article/details/7491714.sHtML
http://www.blog.cmcvrr.cn/Article/details/80585.sHtML
http://www.blog.cmcvrr.cn/Article/details/15955.sHtML
http://www.blog.cmcvrr.cn/Article/details/92990.sHtML
http://www.blog.cmcvrr.cn/Article/details/71171.sHtML
http://www.blog.cmcvrr.cn/Article/details/128807.sHtML
http://www.blog.cmcvrr.cn/Article/details/0146.sHtML
http://www.blog.cmcvrr.cn/Article/details/2272742.sHtML
http://www.blog.cmcvrr.cn/Article/details/2777047.sHtML
http://www.blog.cmcvrr.cn/Article/details/6489.sHtML
http://www.blog.cmcvrr.cn/Article/details/1534.sHtML
http://www.blog.cmcvrr.cn/Article/details/6336.sHtML
http://www.blog.cmcvrr.cn/Article/details/8307587.sHtML
http://www.blog.cmcvrr.cn/Article/details/529942.sHtML
http://www.blog.cmcvrr.cn/Article/details/6757.sHtML
http://www.blog.cmcvrr.cn/Article/details/8766.sHtML
http://www.blog.cmcvrr.cn/Article/details/8476055.sHtML
http://www.blog.cmcvrr.cn/Article/details/857011.sHtML
http://www.blog.cmcvrr.cn/Article/details/8853.sHtML
http://www.blog.cmcvrr.cn/Article/details/288603.sHtML
http://www.blog.cmcvrr.cn/Article/details/72753.sHtML
http://www.blog.cmcvrr.cn/Article/details/2995.sHtML
http://www.blog.cmcvrr.cn/Article/details/08511.sHtML
http://www.blog.cmcvrr.cn/Article/details/61632.sHtML
http://www.blog.cmcvrr.cn/Article/details/452571.sHtML
http://www.blog.cmcvrr.cn/Article/details/211481.sHtML

## 项目结构

```
resourcebridge/
├── README.md                         # 项目说明文档
├── LICENSE                           # MIT 许可证文件
├── requirements.txt                  # Python 依赖清单
├── config/
│   └── settings.yaml                 # 全局配置文件（超时阈值、输出路径）
├── resources/
│   ├── master_list.txt               # 主资源列表，每行一个 URL
│   └── categories.yaml               # 分类映射定义
├── scripts/
│   ├── validate_links.py             # 链接可达性校验主脚本
│   ├── generate_markdown.py          # 从列表生成 Markdown 文档
│   └── utils/
│       ├── http_client.py            # 带重试机制的 HTTP 请求封装
│       └── logger.py                 # 日志记录与格式化输出
├── reports/
│   ├── status.json                   # 链接校验结果（JSON 格式）
│   └── summary.log                   # 校验过程日志
├── docs/
│   ├── user_guide.md                 # 用户使用手册
│   ├── maintainer_guide.md           # 维护者操作指南
│   ├── design.md                     # 架构设计文档
│   └── api_reference.md              # 脚本接口说明
└── tests/
    ├── test_http_client.py           # HTTP 模块单元测试
    └── test_validate.py              # 校验逻辑单元测试
```

## 贡献指南

提交 Issue 报告资源链接失效或分类错误：请在 GitHub Issues 页面新建 Issue，标题注明「链接失效」或「分类建议」，并附上具体 URL 及预期修正内容。

发起 Pull Request 更新资源列表：Fork 本仓库后，在 resources/master_list.txt 中追加或删除 URL，提交 PR 时请附带说明变更理由与校验结果截图。

完善文档与脚本功能：若您改进了校验逻辑、新增了输出格式或优化了性能，请在 PR 中清晰描述改动点，并确保通过现有单元测试。

遵循代码风格规范：Python 代码请遵循 PEP 8 规范，提交前运行 flake8 或 black 进行格式化检查。

## 常见问题

Q: 资源列表中的链接访问返回 404 或超时，应该如何处理？

A: 您可以通过 Issue 或 PR 告知我们失效链接。项目维护者会定期运行校验脚本，但对于部分临时性不可访问的站点，可能会等待一段时间后再次确认。若确认永久失效，将从列表中移除。

Q: 为什么某些 URL 的协议是 http 而非 https？

A: ResourceBridge 严格保留原始收录时的 URL 字符串，不做协议升级或降级。这是因为部分源站点可能未配置 HTTPS 支持，或存在特殊的访问策略。用户访问时可根据自身安全需求自行决定是否升级协议。

Q: 我可以将 ResourceBridge 的资源列表用于自己的项目或网站吗？

A: 可以。本项目的资源列表本身属于公共信息汇编，不涉及版权内容。但请注意，每个外链指向的原始页面仍受其各自版权条款约束。建议在使用时标注资源来源为 ResourceBridge 收录。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:28:08
