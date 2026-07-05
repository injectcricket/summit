# BlogNav 聚合导航系统

BlogNav 是一个面向技术内容聚合与知识导航的开源工具集，专为需要从分散技术博客、文档站点与资讯平台中高效提取、分类与检索文章链接的开发者与研究员设计。该项目通过结构化的数据组织方式，帮助用户将大量零散的外部技术文章 URL 转化为可检索、可浏览、可扩展的本地导航知识库。

BlogNav 的核心目标用户包括技术博主、开源社区维护者、DevOps 工程师以及知识管理爱好者。当用户面对数百条来自同一来源但路径各异的文章链接时，BlogNav 提供了一套自动化抓取元信息、生成索引目录、并支持多维度筛选的轻量级方案，从而显著降低人工整理成本并提升信息复用效率。

## 功能概览

批量链接导入与规范化校验 支持从文本文件或标准输入流中导入大量 HTTP URL，自动检测链接可达性并过滤无效条目。

元数据自动提取引擎 对每个有效链接发起 HEAD 请求获取响应头信息，并尝试从 HTML 标题标签中提取文章标题作为默认展示名称。

多级分类标签生成 基于 URL 路径中的目录分段（如 Article/details/）自动生成一级分类，同时允许用户通过配置文件自定义标签映射规则。

本地全文索引构建 将链接标题、分类标签、最后修改时间与原始 URL 存储为 SQLite 关系表，支持基于 B-tree 的快速字符串匹配查询。

静态导航站点生成器 内置 Mustache 模板引擎，可根据索引数据一键生成响应式 HTML 导航页面，包含分类过滤面板与搜索输入框。

导入导出互通支持 提供 JSON 与 CSV 两种序列化格式的导入导出接口，便于与其他数据处理工具（如 jq、Excel、Pandas）协同工作。

增量更新与去重机制 在重复导入相同 URL 时自动识别并更新其元信息，避免产生冗余记录，同时保留首次导入时间戳用于追溯。

## 应用场景

技术博客归档整理 技术作者可以将自己多年发表在不同平台上的文章链接集中导入 BlogNav，生成一份带有分类标签的个人作品集导航页，方便读者按主题浏览。

开源项目文档聚合 开源项目维护者可将项目相关的教程、API 参考、社区案例等外部链接统一收录，作为项目官方文档的补充资源板块，提升生态信息可发现性。

团队知识库外链管理 企业内部技术团队可将每周技术分享会中提及的参考链接、故障排查记录、第三方库文档等通过 BlogNav 建立团队共享导航，减少重复提问并加速问题定位。

个人阅读列表优先级排序 研究人员可将待读的论文预印本、技术分析文章、性能测试报告等批量导入，利用 BlogNav 的分类与时间戳功能按主题或时效性筛选，制定每日阅读计划。

## 快速开始

以下指令演示如何获取项目源码、安装依赖并启动一个最小化的本地导航服务。

```bash
# 克隆项目仓库至本地
git clone https://github.com/technav-io/blognav.git

# 进入项目根目录并安装 Python 依赖（建议使用虚拟环境）
cd blognav
python -m venv venv
source venv/bin/activate  # Windows 下使用 venv\Scripts\activate
pip install -r requirements.txt

# 将示例链接列表导入并生成静态导航页面
python blognav.py import --input samples/links.txt --output data/index.db
python blognav.py build --database data/index.db --output dist/
```

执行完毕后，使用任意 HTTP 服务器（如 `python -m http.server 8000 --directory dist/`）在本地查看生成的导航页面。

## 安装要求

| 依赖 | 必需版本 | 说明 |
|---|---|---|
| Python | 3.9 及以上 | 核心运行环境，提供异步 I/O 与类型注解支持 |
| aiohttp | 3.8.0 及以上 | 用于高并发异步 HTTP 请求，提升链接检查与元数据抓取效率 |
| beautifulsoup4 | 4.11.0 及以上 | 解析 HTML 文档以提取标题和 meta 描述信息 |
| lxml | 4.9.0 及以上 | 作为 BeautifulSoup 的解析后端，提供高性能 XML/HTML 树遍历 |
| markdown | 3.4.0 及以上 | 将每条链接的备注字段从 Markdown 渲染为 HTML 片段 |
| jinja2 | 3.1.0 及以上 | 模板引擎，用于生成自定义样式的导航页面（可替代内置 Mustache） |
| pytest | 7.2.0 及以上 | 单元测试框架，仅开发与调试时需要 |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|---|---|---|
| 入门指南 | docs/quickstart.md | 如何用三个命令完成首次链接导入与页面生成？ |
| 配置参考 | docs/configuration.md | 分类映射规则、请求超时、模板路径等参数如何调整？ |
| 开发指南 | docs/development.md | 项目代码结构、新增数据源解析器、提交测试的流程是什么？ |
| API 接口 | docs/api_reference.md | 各模块对外暴露的函数签名、参数类型与返回值结构说明 |
| 模板定制 | docs/template_customization.md | 如何替换默认导航主题或添加自定义 CSS/JavaScript？ |
| 性能调优 | docs/performance.md | 处理 5000+ 链接时的内存占用与并发数推荐配置 |

## 资源列表

本批次（第 180/280 批）收录的外部技术文章链接均来自同一技术博客平台，按文章 ID 分段整理如下。所有链接保持原始格式一字不差列出。

技术文章主序列

http://www.blog.nzfnve.cn/Article/details/82165.sHtML
http://www.blog.nzfnve.cn/Article/details/29331.sHtML
http://www.blog.nzfnve.cn/Article/details/1624992.sHtML
http://www.blog.nzfnve.cn/Article/details/707387.sHtML
http://www.blog.nzfnve.cn/Article/details/42021.sHtML
http://www.blog.nzfnve.cn/Article/details/2955851.sHtML
http://www.blog.nzfnve.cn/Article/details/1615925.sHtML
http://www.blog.nzfnve.cn/Article/details/58579.sHtML
http://www.blog.nzfnve.cn/Article/details/47400.sHtML
http://www.blog.nzfnve.cn/Article/details/3244166.sHtML
http://www.blog.nzfnve.cn/Article/details/38411.sHtML
http://www.blog.nzfnve.cn/Article/details/8533.sHtML
http://www.blog.nzfnve.cn/Article/details/23790.sHtML
http://www.blog.nzfnve.cn/Article/details/899868.sHtML
http://www.blog.nzfnve.cn/Article/details/0837.sHtML
http://www.blog.nzfnve.cn/Article/details/887466.sHtML
http://www.blog.nzfnve.cn/Article/details/9553.sHtML
http://www.blog.nzfnve.cn/Article/details/7035863.sHtML
http://www.blog.nzfnve.cn/Article/details/074894.sHtML
http://www.blog.nzfnve.cn/Article/details/307068.sHtML
http://www.blog.nzfnve.cn/Article/details/908944.sHtML
http://www.blog.nzfnve.cn/Article/details/58440.sHtML
http://www.blog.nzfnve.cn/Article/details/7175.sHtML
http://www.blog.nzfnve.cn/Article/details/79949.sHtML
http://www.blog.nzfnve.cn/Article/details/28028.sHtML
http://www.blog.nzfnve.cn/Article/details/882395.sHtML
http://www.blog.nzfnve.cn/Article/details/2202043.sHtML
http://www.blog.nzfnve.cn/Article/details/1925932.sHtML
http://www.blog.nzfnve.cn/Article/details/281082.sHtML
http://www.blog.nzfnve.cn/Article/details/3617.sHtML
http://www.blog.nzfnve.cn/Article/details/0713.sHtML
http://www.blog.nzfnve.cn/Article/details/8106009.sHtML
http://www.blog.nzfnve.cn/Article/details/3214754.sHtML
http://www.blog.nzfnve.cn/Article/details/84784.sHtML
http://www.blog.nzfnve.cn/Article/details/770371.sHtML
http://www.blog.nzfnve.cn/Article/details/028813.sHtML
http://www.blog.nzfnve.cn/Article/details/83819.sHtML
http://www.blog.nzfnve.cn/Article/details/280966.sHtML
http://www.blog.nzfnve.cn/Article/details/787441.sHtML
http://www.blog.nzfnve.cn/Article/details/702327.sHtML
http://www.blog.nzfnve.cn/Article/details/3271.sHtML
http://www.blog.nzfnve.cn/Article/details/541572.sHtML
http://www.blog.nzfnve.cn/Article/details/45614.sHtML
http://www.blog.nzfnve.cn/Article/details/821025.sHtML
http://www.blog.nzfnve.cn/Article/details/282978.sHtML
http://www.blog.nzfnve.cn/Article/details/9775686.sHtML
http://www.blog.nzfnve.cn/Article/details/272256.sHtML
http://www.blog.nzfnve.cn/Article/details/4368.sHtML
http://www.blog.nzfnve.cn/Article/details/83881.sHtML
http://www.blog.nzfnve.cn/Article/details/18300.sHtML
http://www.blog.nzfnve.cn/Article/details/241366.sHtML
http://www.blog.nzfnve.cn/Article/details/832884.sHtML
http://www.blog.nzfnve.cn/Article/details/98407.sHtML
http://www.blog.nzfnve.cn/Article/details/49119.sHtML
http://www.blog.nzfnve.cn/Article/details/9682492.sHtML
http://www.blog.nzfnve.cn/Article/details/358773.sHtML
http://www.blog.nzfnve.cn/Article/details/2594507.sHtML
http://www.blog.nzfnve.cn/Article/details/2121153.sHtML
http://www.blog.nzfnve.cn/Article/details/94217.sHtML
http://www.blog.nzfnve.cn/Article/details/733859.sHtML
http://www.blog.nzfnve.cn/Article/details/05681.sHtML
http://www.blog.nzfnve.cn/Article/details/0386099.sHtML
http://www.blog.nzfnve.cn/Article/details/8462827.sHtML
http://www.blog.nzfnve.cn/Article/details/1110.sHtML
http://www.blog.nzfnve.cn/Article/details/5142.sHtML
http://www.blog.nzfnve.cn/Article/details/800577.sHtML
http://www.blog.nzfnve.cn/Article/details/58914.sHtML
http://www.blog.nzfnve.cn/Article/details/33176.sHtML
http://www.blog.nzfnve.cn/Article/details/401091.sHtML
http://www.blog.nzfnve.cn/Article/details/56456.sHtML
http://www.blog.nzfnve.cn/Article/details/03089.sHtML
http://www.blog.nzfnve.cn/Article/details/758139.sHtML
http://www.blog.nzfnve.cn/Article/details/68377.sHtML
http://www.blog.nzfnve.cn/Article/details/150451.sHtML
http://www.blog.nzfnve.cn/Article/details/6379509.sHtML
http://www.blog.nzfnve.cn/Article/details/39422.sHtML
http://www.blog.nzfnve.cn/Article/details/44241.sHtML
http://www.blog.nzfnve.cn/Article/details/7439.sHtML
http://www.blog.nzfnve.cn/Article/details/65152.sHtML
http://www.blog.nzfnve.cn/Article/details/5677180.sHtML
http://www.blog.nzfnve.cn/Article/details/2700.sHtML
http://www.blog.nzfnve.cn/Article/details/607838.sHtML
http://www.blog.nzfnve.cn/Article/details/5793.sHtML
http://www.blog.nzfnve.cn/Article/details/6727778.sHtML
http://www.blog.nzfnve.cn/Article/details/30670.sHtML
http://www.blog.nzfnve.cn/Article/details/732879.sHtML
http://www.blog.nzfnve.cn/Article/details/185189.sHtML
http://www.blog.nzfnve.cn/Article/details/850343.sHtML
http://www.blog.nzfnve.cn/Article/details/32968.sHtML
http://www.blog.nzfnve.cn/Article/details/9021.sHtML
http://www.blog.nzfnve.cn/Article/details/438961.sHtML
http://www.blog.nzfnve.cn/Article/details/6838.sHtML
http://www.blog.nzfnve.cn/Article/details/5292.sHtML
http://www.blog.nzfnve.cn/Article/details/84886.sHtML
http://www.blog.nzfnve.cn/Article/details/9670986.sHtML
http://www.blog.nzfnve.cn/Article/details/16555.sHtML
http://www.blog.nzfnve.cn/Article/details/05079.sHtML
http://www.blog.nzfnve.cn/Article/details/830694.sHtML
http://www.blog.nzfnve.cn/Article/details/7697525.sHtML
http://www.blog.nzfnve.cn/Article/details/022764.sHtML
http://www.blog.nzfnve.cn/Article/details/6744.sHtML
http://www.blog.nzfnve.cn/Article/details/5901026.sHtML
http://www.blog.nzfnve.cn/Article/details/15004.sHtML
http://www.blog.nzfnve.cn/Article/details/7289.sHtML
http://www.blog.nzfnve.cn/Article/details/418643.sHtML
http://www.blog.nzfnve.cn/Article/details/89256.sHtML
http://www.blog.nzfnve.cn/Article/details/0052718.sHtML
http://www.blog.nzfnve.cn/Article/details/5326.sHtML
http://www.blog.nzfnve.cn/Article/details/49326.sHtML
http://www.blog.nzfnve.cn/Article/details/2316995.sHtML
http://www.blog.nzfnve.cn/Article/details/57591.sHtML
http://www.blog.nzfnve.cn/Article/details/4091.sHtML
http://www.blog.nzfnve.cn/Article/details/3242.sHtML
http://www.blog.nzfnve.cn/Article/details/10365.sHtML
http://www.blog.nzfnve.cn/Article/details/0690.sHtML
http://www.blog.nzfnve.cn/Article/details/95885.sHtML
http://www.blog.nzfnve.cn/Article/details/032318.sHtML
http://www.blog.nzfnve.cn/Article/details/4803.sHtML
http://www.blog.nzfnve.cn/Article/details/6410581.sHtML
http://www.blog.nzfnve.cn/Article/details/6425044.sHtML
http://www.blog.nzfnve.cn/Article/details/025646.sHtML
http://www.blog.nzfnve.cn/Article/details/94261.sHtML
http://www.blog.nzfnve.cn/Article/details/3848268.sHtML
http://www.blog.nzfnve.cn/Article/details/7797422.sHtML
http://www.blog.nzfnve.cn/Article/details/91183.sHtML
http://www.blog.nzfnve.cn/Article/details/901631.sHtML
http://www.blog.nzfnve.cn/Article/details/4043222.sHtML
http://www.blog.nzfnve.cn/Article/details/14815.sHtML
http://www.blog.nzfnve.cn/Article/details/08057.sHtML
http://www.blog.nzfnve.cn/Article/details/982071.sHtML
http://www.blog.nzfnve.cn/Article/details/04709.sHtML
http://www.blog.nzfnve.cn/Article/details/48510.sHtML
http://www.blog.nzfnve.cn/Article/details/712753.sHtML
http://www.blog.nzfnve.cn/Article/details/6531.sHtML
http://www.blog.nzfnve.cn/Article/details/3286.sHtML
http://www.blog.nzfnve.cn/Article/details/6310738.sHtML
http://www.blog.nzfnve.cn/Article/details/976739.sHtML
http://www.blog.nzfnve.cn/Article/details/7972468.sHtML
http://www.blog.nzfnve.cn/Article/details/4415505.sHtML
http://www.blog.nzfnve.cn/Article/details/3068772.sHtML
http://www.blog.nzfnve.cn/Article/details/482985.sHtML
http://www.blog.nzfnve.cn/Article/details/91024.sHtML
http://www.blog.nzfnve.cn/Article/details/6633819.sHtML
http://www.blog.nzfnve.cn/Article/details/5234.sHtML
http://www.blog.nzfnve.cn/Article/details/4527545.sHtML
http://www.blog.nzfnve.cn/Article/details/1240.sHtML
http://www.blog.nzfnve.cn/Article/details/9531.sHtML
http://www.blog.nzfnve.cn/Article/details/0326367.sHtML
http://www.blog.nzfnve.cn/Article/details/78710.sHtML
http://www.blog.nzfnve.cn/Article/details/9985567.sHtML
http://www.blog.nzfnve.cn/Article/details/70180.sHtML
http://www.blog.nzfnve.cn/Article/details/77858.sHtML
http://www.blog.nzfnve.cn/Article/details/9500.sHtML
http://www.blog.nzfnve.cn/Article/details/6740.sHtML
http://www.blog.nzfnve.cn/Article/details/6557.sHtML
http://www.blog.nzfnve.cn/Article/details/1711.sHtML
http://www.blog.nzfnve.cn/Article/details/6355161.sHtML
http://www.blog.nzfnve.cn/Article/details/4831695.sHtML
http://www.blog.nzfnve.cn/Article/details/74449.sHtML
http://www.blog.nzfnve.cn/Article/details/4692.sHtML
http://www.blog.nzfnve.cn/Article/details/35281.sHtML
http://www.blog.nzfnve.cn/Article/details/60902.sHtML
http://www.blog.nzfnve.cn/Article/details/315591.sHtML
http://www.blog.nzfnve.cn/Article/details/1620344.sHtML
http://www.blog.nzfnve.cn/Article/details/8011949.sHtML
http://www.blog.nzfnve.cn/Article/details/685761.sHtML
http://www.blog.nzfnve.cn/Article/details/5014.sHtML
http://www.blog.nzfnve.cn/Article/details/6903.sHtML
http://www.blog.nzfnve.cn/Article/details/6233996.sHtML
http://www.blog.nzfnve.cn/Article/details/6006303.sHtML
http://www.blog.nzfnve.cn/Article/details/0487.sHtML
http://www.blog.nzfnve.cn/Article/details/54102.sHtML
http://www.blog.nzfnve.cn/Article/details/95521.sHtML
http://www.blog.nzfnve.cn/Article/details/84950.sHtML
http://www.blog.nzfnve.cn/Article/details/5463623.sHtML
http://www.blog.nzfnve.cn/Article/details/0173.sHtML
http://www.blog.nzfnve.cn/Article/details/00398.sHtML
http://www.blog.nzfnve.cn/Article/details/9296.sHtML
http://www.blog.nzfnve.cn/Article/details/291461.sHtML
http://www.blog.nzfnve.cn/Article/details/01375.sHtML
http://www.blog.nzfnve.cn/Article/details/4573225.sHtML
http://www.blog.nzfnve.cn/Article/details/6183346.sHtML
http://www.blog.nzfnve.cn/Article/details/714588.sHtML
http://www.blog.nzfnve.cn/Article/details/97547.sHtML
http://www.blog.nzfnve.cn/Article/details/073529.sHtML
http://www.blog.nzfnve.cn/Article/details/25721.sHtML
http://www.blog.nzfnve.cn/Article/details/3686.sHtML
http://www.blog.nzfnve.cn/Article/details/4083128.sHtML
http://www.blog.nzfnve.cn/Article/details/67116.sHtML
http://www.blog.nzfnve.cn/Article/details/305467.sHtML
http://www.blog.nzfnve.cn/Article/details/3541624.sHtML
http://www.blog.nzfnve.cn/Article/details/169735.sHtML
http://www.blog.nzfnve.cn/Article/details/98881.sHtML
http://www.blog.nzfnve.cn/Article/details/7520.sHtML
http://www.blog.nzfnve.cn/Article/details/9775.sHtML
http://www.blog.nzfnve.cn/Article/details/0914.sHtML
http://www.blog.nzfnve.cn/Article/details/48731.sHtML
http://www.blog.nzfnve.cn/Article/details/777547.sHtML
http://www.blog.nzfnve.cn/Article/details/9065539.sHtML
http://www.blog.nzfnve.cn/Article/details/0608740.sHtML
http://www.blog.nzfnve.cn/Article/details/46247.sHtML
http://www.blog.nzfnve.cn/Article/details/40954.sHtML
http://www.blog.nzfnve.cn/Article/details/7057359.sHtML
http://www.blog.nzfnve.cn/Article/details/7099537.sHtML
http://www.blog.nzfnve.cn/Article/details/559717.sHtML
http://www.blog.nzfnve.cn/Article/details/0649569.sHtML
http://www.blog.nzfnve.cn/Article/details/6023992.sHtML
http://www.blog.nzfnve.cn/Article/details/62205.sHtML
http://www.blog.nzfnve.cn/Article/details/5048912.sHtML
http://www.blog.nzfnve.cn/Article/details/8659.sHtML
http://www.blog.nzfnve.cn/Article/details/1359.sHtML
http://www.blog.nzfnve.cn/Article/details/12497.sHtML
http://www.blog.nzfnve.cn/Article/details/83892.sHtML
http://www.blog.nzfnve.cn/Article/details/67356.sHtML
http://www.blog.nzfnve.cn/Article/details/772162.sHtML
http://www.blog.nzfnve.cn/Article/details/059893.sHtML
http://www.blog.nzfnve.cn/Article/details/3928524.sHtML
http://www.blog.nzfnve.cn/Article/details/28636.sHtML
http://www.blog.nzfnve.cn/Article/details/14123.sHtML
http://www.blog.nzfnve.cn/Article/details/2086944.sHtML
http://www.blog.nzfnve.cn/Article/details/1303708.sHtML
http://www.blog.nzfnve.cn/Article/details/476923.sHtML
http://www.blog.nzfnve.cn/Article/details/2863051.sHtML
http://www.blog.nzfnve.cn/Article/details/7236.sHtML
http://www.blog.nzfnve.cn/Article/details/9510583.sHtML
http://www.blog.nzfnve.cn/Article/details/0317126.sHtML
http://www.blog.nzfnve.cn/Article/details/1348700.sHtML
http://www.blog.nzfnve.cn/Article/details/96066.sHtML
http://www.blog.nzfnve.cn/Article/details/3160546.sHtML
http://www.blog.nzfnve.cn/Article/details/229807.sHtML
http://www.blog.nzfnve.cn/Article/details/3295295.sHtML
http://www.blog.nzfnve.cn/Article/details/13154.sHtML
http://www.blog.nzfnve.cn/Article/details/16924.sHtML
http://www.blog.nzfnve.cn/Article/details/929168.sHtML
http://www.blog.nzfnve.cn/Article/details/7861260.sHtML
http://www.blog.nzfnve.cn/Article/details/56674.sHtML
http://www.blog.nzfnve.cn/Article/details/3450409.sHtML
http://www.blog.nzfnve.cn/Article/details/01083.sHtML
http://www.blog.nzfnve.cn/Article/details/2167.sHtML
http://www.blog.nzfnve.cn/Article/details/071700.sHtML
http://www.blog.nzfnve.cn/Article/details/4071.sHtML
http://www.blog.nzfnve.cn/Article/details/8364.sHtML
http://www.blog.nzfnve.cn/Article/details/208834.sHtML
http://www.blog.nzfnve.cn/Article/details/1087400.sHtML
http://www.blog.nzfnve.cn/Article/details/56133.sHtML
http://www.blog.nzfnve.cn/Article/details/25000.sHtML
http://www.blog.nzfnve.cn/Article/details/2176.sHtML
http://www.blog.nzfnve.cn/Article/details/1610386.sHtML
http://www.blog.nzfnve.cn/Article/details/5396.sHtML
http://www.blog.nzfnve.cn/Article/details/2636.sHtML

## 项目结构

```
blognav/
├── blognav.py                    # CLI 入口，整合导入、构建、导出命令
├── requirements.txt              # 生产环境依赖清单（aiohttp, bs4, lxml, jinja2）
├── README.md                     # 项目说明文档（即当前文件）
├── .gitignore                    # 忽略虚拟环境、缓存、临时数据与 dist 目录
├── config/
│   ├── default.yaml              # 默认配置：并发数 20，超时 10s，模板主题 light
│   └── custom_mapping.yaml       # 用户自定义分类映射规则（示例：路径含 python 映射至语言-Python）
├── core/
│   ├── __init__.py               # 模块导出：Link, LinkCollection, Indexer
│   ├── fetcher.py                # 异步 HTTP 获取器，含重试与 SSL 忽略逻辑
│   ├── parser.py                 # HTML 标题与 meta 描述提取，使用 BeautifulSoup
│   ├── indexer.py                # SQLite 索引写入与查询接口，支持 upsert
│   └── validator.py              # URL 格式校验、域名白名单检查与去重哈希计算
├── templates/
│   ├── default.mustache          # 主页面模板：包含分类侧边栏与卡片列表
│   ├── item.mustache             # 单条链接渲染模板：标题、URL、标签、时间戳
│   └── static/                   # 内置 CSS（基于 minireset.css）与 JavaScript（过滤逻辑）
├── tests/
│   ├── test_fetcher.py           # 模拟 HTTP 响应，测试重试与超时分支
│   ├── test_parser.py            # 使用固定 HTML 片段验证标题提取准确性
│   └── test_indexer.py           # 内存 SQLite 测试，覆盖插入、更新、去重场景
├── samples/
│   ├── links.txt                 # 示例输入文件，每行一个 URL（即本批次资源列表）
│   └── exported.json             # 示例导出结果，展示 JSON 序列化格式
└── dist/                         # 构建输出目录（默认），包含 index.html 与静态资源
```

## 贡献指南

1. 查阅 issue 列表并选择未被分配的、带有 "help wanted" 或 "good first issue" 标签的任务，在对应 issue 下评论表明认领意图，避免重复工作。

2. 从主分支创建新功能分支，分支命名遵循 `feature/功能简述` 或 `fix/问题简述` 格式，例如 `feature/add-rss-export`。所有开发均在此分支上完成。

3. 编写或修改代码时，请确保新增逻辑附有对应的单元测试（位于 `tests/` 目录），且现有测试套件全部通过。测试命令为 `pytest -v`。

4. 提交代码前运行 `make lint`（需预先安装 flake8 与 mypy）进行静态检查，修复所有风格警告与类型错误。提交信息采用约定式提交格式，如 `feat: 增加 CSV 导出支持` 或 `fix: 修复长链接截断导致的索引异常`。

5. 发起 Pull Request 至 main 分支，PR 描述中必须包含关联 issue 编号、变更摘要、测试结果截图或日志，并邀请至少一名项目维护者进行代码审查。审查通过后由维护者合并。

## 常见问题

Q: 导入大量链接时出现连接超时或 SSL 证书错误，如何解决？
A: 可在配置文件中调整 `request_timeout` 参数（单位秒）并设置 `ssl_verify=false` 跳过证书校验。对于网络不稳定环境，建议降低 `concurrency_limit` 至 5 以下并启用 `retry_on_failure` 选项。

Q: 生成的导航页面无法正确显示中文标题，出现乱码。
A: 请确保源 HTML 页面使用 UTF-8 编码。BlogNav 默认以 UTF-8 解析响应，若源站使用 GBK 或 GB2312，可在配置文件的 `encoding_override` 段中按域名指定字符集。同时确保生成的 HTML 页面 `<meta charset="utf-8">` 声明正确。

Q: 如何将现有的链接索引迁移至另一台机器或分享给他人？
A: 使用 `export` 命令将 SQLite 数据导出为 JSON 或 CSV 文件，在目标机器上使用 `import` 命令重新导入。若仅需共享导航页面，可直接分发 `dist/` 目录下的所有静态文件，无需安装 Python 环境。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:28:22
