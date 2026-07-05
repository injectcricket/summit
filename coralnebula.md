# ResourceBridge

ResourceBridge 是一个面向技术开发者与架构师的开源外链资源归集与导航系统。项目定位为技术资料的中转枢纽，解决开发者在海量技术博客、官方文档、社区讨论中难以高效检索与回溯高质量文章的问题。ResourceBridge 不生产内容，而是通过结构化的外链管理机制，帮助个人与团队建立可维护、可分享的技术知识索引。

项目采用静态站点生成模式，所有资源链接按批次、分类、标签进行组织，支持本地化全文检索与快捷跳转。适用于需要长期积累技术阅读清单、维护团队知识库、或构建个人技术资讯聚合页的场景。ResourceBridge 本身不依赖数据库，所有数据以 Markdown 与 YAML 格式存储，便于版本控制与协作编辑。

## 功能概览

**多级分类体系**：支持按技术领域、难度等级、来源类型对资源进行多维度划分，每个资源可归属多个分类。

**批量导入与去重**：提供脚本工具从文本文件、书签导出文件或表格中批量导入 URL，自动检测并移除重复条目。

**全文检索与过滤**：基于标题、摘要、分类标签和文章编号进行关键词检索，支持按时间范围与来源域名过滤结果。

**静态站点生成**：内置模板引擎可将资源列表渲染为完整的静态 HTML 网站，适合部署到任意 Web 服务器或 CDN。

**资源状态标记**：每条链接可标记为有效、失效、待审阅或已归档，支持定期链接健康检查并生成报告。

**元数据扩展**：支持为每条资源记录添加自定义键值对元数据，如阅读时长、关联项目、笔记摘要等。

## 应用场景

技术团队内部知识沉淀：团队可将日常阅读的高质量技术文章通过 ResourceBridge 统一收录，按项目或技术栈分类，新成员入职时可直接通过该索引快速了解团队所关注的技术领域与最佳实践。

个人技术阅读管理：开发者可将订阅的 RSS 来源、技术博客、论文链接统一纳入 ResourceBridge，配合标签系统构建个人技术阅读清单，避免重复搜索与遗忘。

技术社区资源共建：开源社区或技术论坛可使用 ResourceBridge 搭建社区推荐阅读列表，成员可提交 PR 增加新链接，经审核后合并，形成社区驱动的知识导航。

离线文档辅助索引：在无法直接访问互联网的内网开发环境中，ResourceBridge 可作为外链的离线索引表，记录每条资源的原始出处与本地缓存路径，方便按图索骥获取资料。

## 快速开始

以下命令演示如何从 GitHub 克隆项目、安装依赖并启动本地开发服务器。

```bash
# 克隆项目仓库
git clone https://github.com/your-org/resource-bridge.git

# 进入项目目录
cd resource-bridge

# 安装 Python 依赖（推荐使用虚拟环境）
python -m venv venv
source venv/bin/activate  # Windows 下使用 venv\Scripts\activate
pip install -r requirements.txt

# 执行资源导入脚本（示例数据）
python scripts/import_urls.py --input data/urls.txt --batch 211

# 构建静态站点并启动预览服务
python build.py --output dist
cd dist && python -m http.server 8000
```

访问 http://localhost:8000 即可查看生成的资源导航页面。

## 安装要求

| 依赖 | 必需版本 | 说明 |
|------|----------|------|
| Python | 3.9 及以上 | 核心运行环境，用于构建与脚本执行 |
| pip | 21.0 及以上 | Python 包管理工具，用于安装依赖项 |
| PyYAML | 6.0 | 解析资源元数据与配置文件 |
| Jinja2 | 3.1 | 模板引擎，用于渲染静态 HTML 页面 |
| markdown | 3.4 | 将资源备注中的 Markdown 格式转换为 HTML |
| requests | 2.31 | 可选依赖，用于链接健康检查功能 |
| pytest | 7.4 | 开发依赖，用于运行单元测试与集成测试 |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|------|------|------------|
| 入门指南 | docs/getting-started.md | 如何安装、配置并运行第一个 ResourceBridge 实例 |
| 资源管理 | docs/resource-management.md | 如何导入、分类、编辑和删除资源条目 |
| 自定义模板 | docs/template-customization.md | 如何修改页面布局、样式和添加自定义组件 |
| API 参考 | docs/api-reference.md | 各模块函数与类的详细接口说明，面向二次开发者 |

## 资源列表

以下链接为本批次收录的全部原始外链，按原样列出。

技术文章类

http://www.blog.jnjpgf.cn/Article/details/285538.sHtML
http://www.blog.jnjpgf.cn/Article/details/250828.sHtML
http://www.blog.jnjpgf.cn/Article/details/2683724.sHtML
http://www.blog.jnjpgf.cn/Article/details/9752706.sHtML
http://www.blog.jnjpgf.cn/Article/details/392170.sHtML
http://www.blog.jnjpgf.cn/Article/details/1164.sHtML
http://www.blog.jnjpgf.cn/Article/details/6014.sHtML
http://www.blog.jnjpgf.cn/Article/details/5602.sHtML
http://www.blog.jnjpgf.cn/Article/details/4867.sHtML
http://www.blog.jnjpgf.cn/Article/details/685082.sHtML
http://www.blog.jnjpgf.cn/Article/details/449677.sHtML
http://www.blog.jnjpgf.cn/Article/details/81691.sHtML
http://www.blog.jnjpgf.cn/Article/details/8901624.sHtML
http://www.blog.jnjpgf.cn/Article/details/46300.sHtML
http://www.blog.jnjpgf.cn/Article/details/067426.sHtML
http://www.blog.jnjpgf.cn/Article/details/824578.sHtML
http://www.blog.jnjpgf.cn/Article/details/4729.sHtML
http://www.blog.jnjpgf.cn/Article/details/18201.sHtML
http://www.blog.jnjpgf.cn/Article/details/8731639.sHtML
http://www.blog.jnjpgf.cn/Article/details/0051.sHtML
http://www.blog.jnjpgf.cn/Article/details/2612208.sHtML
http://www.blog.jnjpgf.cn/Article/details/8585740.sHtML
http://www.blog.jnjpgf.cn/Article/details/464592.sHtML
http://www.blog.jnjpgf.cn/Article/details/445049.sHtML
http://www.blog.jnjpgf.cn/Article/details/0539.sHtML
http://www.blog.jnjpgf.cn/Article/details/4277.sHtML
http://www.blog.jnjpgf.cn/Article/details/430668.sHtML
http://www.blog.jnjpgf.cn/Article/details/4712960.sHtML
http://www.blog.jnjpgf.cn/Article/details/4873.sHtML
http://www.blog.jnjpgf.cn/Article/details/2641.sHtML
http://www.blog.jnjpgf.cn/Article/details/4234.sHtML
http://www.blog.jnjpgf.cn/Article/details/3695.sHtML
http://www.blog.jnjpgf.cn/Article/details/212473.sHtML
http://www.blog.jnjpgf.cn/Article/details/3277.sHtML
http://www.blog.jnjpgf.cn/Article/details/185643.sHtML
http://www.blog.jnjpgf.cn/Article/details/43112.sHtML
http://www.blog.jnjpgf.cn/Article/details/76043.sHtML
http://www.blog.jnjpgf.cn/Article/details/1995.sHtML
http://www.blog.jnjpgf.cn/Article/details/807646.sHtML
http://www.blog.jnjpgf.cn/Article/details/481698.sHtML
http://www.blog.jnjpgf.cn/Article/details/870742.sHtML
http://www.blog.jnjpgf.cn/Article/details/8754.sHtML
http://www.blog.jnjpgf.cn/Article/details/4584.sHtML
http://www.blog.jnjpgf.cn/Article/details/3698218.sHtML
http://www.blog.jnjpgf.cn/Article/details/4694.sHtML
http://www.blog.jnjpgf.cn/Article/details/8722429.sHtML
http://www.blog.jnjpgf.cn/Article/details/4761.sHtML
http://www.blog.jnjpgf.cn/Article/details/874591.sHtML
http://www.blog.jnjpgf.cn/Article/details/56156.sHtML
http://www.blog.jnjpgf.cn/Article/details/0256187.sHtML
http://www.blog.jnjpgf.cn/Article/details/1578.sHtML
http://www.blog.jnjpgf.cn/Article/details/71722.sHtML
http://www.blog.jnjpgf.cn/Article/details/03369.sHtML
http://www.blog.jnjpgf.cn/Article/details/091760.sHtML
http://www.blog.jnjpgf.cn/Article/details/039462.sHtML
http://www.blog.jnjpgf.cn/Article/details/6826406.sHtML
http://www.blog.jnjpgf.cn/Article/details/616239.sHtML
http://www.blog.jnjpgf.cn/Article/details/42724.sHtML
http://www.blog.jnjpgf.cn/Article/details/6827.sHtML
http://www.blog.jnjpgf.cn/Article/details/0194.sHtML
http://www.blog.jnjpgf.cn/Article/details/8601912.sHtML
http://www.blog.jnjpgf.cn/Article/details/6077.sHtML
http://www.blog.jnjpgf.cn/Article/details/44042.sHtML
http://www.blog.jnjpgf.cn/Article/details/9209244.sHtML
http://www.blog.jnjpgf.cn/Article/details/031617.sHtML
http://www.blog.jnjpgf.cn/Article/details/99954.sHtML
http://www.blog.jnjpgf.cn/Article/details/13038.sHtML
http://www.blog.jnjpgf.cn/Article/details/4313453.sHtML
http://www.blog.jnjpgf.cn/Article/details/7667179.sHtML
http://www.blog.jnjpgf.cn/Article/details/2126763.sHtML
http://www.blog.jnjpgf.cn/Article/details/90795.sHtML
http://www.blog.jnjpgf.cn/Article/details/6776993.sHtML
http://www.blog.jnjpgf.cn/Article/details/22475.sHtML
http://www.blog.jnjpgf.cn/Article/details/31176.sHtML
http://www.blog.jnjpgf.cn/Article/details/07805.sHtML
http://www.blog.jnjpgf.cn/Article/details/4751.sHtML
http://www.blog.jnjpgf.cn/Article/details/4498.sHtML
http://www.blog.jnjpgf.cn/Article/details/0968.sHtML
http://www.blog.jnjpgf.cn/Article/details/9788618.sHtML
http://www.blog.jnjpgf.cn/Article/details/9598.sHtML
http://www.blog.jnjpgf.cn/Article/details/263229.sHtML
http://www.blog.jnjpgf.cn/Article/details/903067.sHtML
http://www.blog.jnjpgf.cn/Article/details/1634263.sHtML
http://www.blog.jnjpgf.cn/Article/details/4685.sHtML
http://www.blog.jnjpgf.cn/Article/details/6420747.sHtML
http://www.blog.jnjpgf.cn/Article/details/03733.sHtML
http://www.blog.jnjpgf.cn/Article/details/9019290.sHtML
http://www.blog.jnjpgf.cn/Article/details/821183.sHtML
http://www.blog.jnjpgf.cn/Article/details/33521.sHtML
http://www.blog.jnjpgf.cn/Article/details/3719144.sHtML
http://www.blog.jnjpgf.cn/Article/details/204096.sHtML
http://www.blog.jnjpgf.cn/Article/details/4395.sHtML
http://www.blog.jnjpgf.cn/Article/details/5105.sHtML
http://www.blog.jnjpgf.cn/Article/details/5757.sHtML
http://www.blog.jnjpgf.cn/Article/details/1791.sHtML
http://www.blog.jnjpgf.cn/Article/details/09782.sHtML
http://www.blog.jnjpgf.cn/Article/details/8724.sHtML
http://www.blog.jnjpgf.cn/Article/details/314959.sHtML
http://www.blog.jnjpgf.cn/Article/details/972830.sHtML
http://www.blog.jnjpgf.cn/Article/details/47657.sHtML
http://www.blog.jnjpgf.cn/Article/details/6616002.sHtML
http://www.blog.jnjpgf.cn/Article/details/064232.sHtML
http://www.blog.jnjpgf.cn/Article/details/39635.sHtML
http://www.blog.jnjpgf.cn/Article/details/93585.sHtML
http://www.blog.jnjpgf.cn/Article/details/2667677.sHtML
http://www.blog.jnjpgf.cn/Article/details/3524910.sHtML
http://www.blog.jnjpgf.cn/Article/details/748352.sHtML
http://www.blog.jnjpgf.cn/Article/details/548520.sHtML
http://www.blog.jnjpgf.cn/Article/details/247175.sHtML
http://www.blog.jnjpgf.cn/Article/details/99251.sHtML
http://www.blog.jnjpgf.cn/Article/details/20449.sHtML
http://www.blog.jnjpgf.cn/Article/details/829983.sHtML
http://www.blog.jnjpgf.cn/Article/details/66176.sHtML
http://www.blog.jnjpgf.cn/Article/details/6911.sHtML
http://www.blog.jnjpgf.cn/Article/details/276798.sHtML
http://www.blog.jnjpgf.cn/Article/details/581164.sHtML
http://www.blog.jnjpgf.cn/Article/details/9918918.sHtML
http://www.blog.jnjpgf.cn/Article/details/3358.sHtML
http://www.blog.jnjpgf.cn/Article/details/9613.sHtML
http://www.blog.jnjpgf.cn/Article/details/6879.sHtML
http://www.blog.jnjpgf.cn/Article/details/9597.sHtML
http://www.blog.jnjpgf.cn/Article/details/2400183.sHtML
http://www.blog.jnjpgf.cn/Article/details/89552.sHtML
http://www.blog.jnjpgf.cn/Article/details/504948.sHtML
http://www.blog.jnjpgf.cn/Article/details/245785.sHtML
http://www.blog.jnjpgf.cn/Article/details/83548.sHtML
http://www.blog.jnjpgf.cn/Article/details/00380.sHtML
http://www.blog.jnjpgf.cn/Article/details/9825.sHtML
http://www.blog.jnjpgf.cn/Article/details/3223.sHtML
http://www.blog.jnjpgf.cn/Article/details/8240.sHtML
http://www.blog.jnjpgf.cn/Article/details/0959267.sHtML
http://www.blog.jnjpgf.cn/Article/details/5785227.sHtML
http://www.blog.jnjpgf.cn/Article/details/54263.sHtML
http://www.blog.jnjpgf.cn/Article/details/3088.sHtML
http://www.blog.jnjpgf.cn/Article/details/6669087.sHtML
http://www.blog.jnjpgf.cn/Article/details/62660.sHtML
http://www.blog.jnjpgf.cn/Article/details/8620.sHtML
http://www.blog.jnjpgf.cn/Article/details/508811.sHtML
http://www.blog.jnjpgf.cn/Article/details/005167.sHtML
http://www.blog.jnjpgf.cn/Article/details/402315.sHtML
http://www.blog.jnjpgf.cn/Article/details/47183.sHtML
http://www.blog.jnjpgf.cn/Article/details/0342608.sHtML
http://www.blog.jnjpgf.cn/Article/details/155139.sHtML
http://www.blog.jnjpgf.cn/Article/details/844159.sHtML
http://www.blog.jnjpgf.cn/Article/details/3843226.sHtML
http://www.blog.jnjpgf.cn/Article/details/26247.sHtML
http://www.blog.jnjpgf.cn/Article/details/494412.sHtML
http://www.blog.jnjpgf.cn/Article/details/3948314.sHtML
http://www.blog.jnjpgf.cn/Article/details/721728.sHtML
http://www.blog.jnjpgf.cn/Article/details/0835203.sHtML
http://www.blog.jnjpgf.cn/Article/details/9097.sHtML
http://www.blog.jnjpgf.cn/Article/details/10319.sHtML
http://www.blog.jnjpgf.cn/Article/details/269623.sHtML
http://www.blog.jnjpgf.cn/Article/details/300438.sHtML
http://www.blog.jnjpgf.cn/Article/details/10116.sHtML
http://www.blog.jnjpgf.cn/Article/details/1901.sHtML
http://www.blog.jnjpgf.cn/Article/details/6039656.sHtML
http://www.blog.jnjpgf.cn/Article/details/331366.sHtML
http://www.blog.jnjpgf.cn/Article/details/2863.sHtML
http://www.blog.jnjpgf.cn/Article/details/8898.sHtML
http://www.blog.jnjpgf.cn/Article/details/07554.sHtML
http://www.blog.jnjpgf.cn/Article/details/9130.sHtML
http://www.blog.jnjpgf.cn/Article/details/3990.sHtML
http://www.blog.jnjpgf.cn/Article/details/94236.sHtML
http://www.blog.jnjpgf.cn/Article/details/66252.sHtML
http://www.blog.jnjpgf.cn/Article/details/1128080.sHtML
http://www.blog.jnjpgf.cn/Article/details/61132.sHtML
http://www.blog.jnjpgf.cn/Article/details/26752.sHtML
http://www.blog.jnjpgf.cn/Article/details/7612994.sHtML
http://www.blog.jnjpgf.cn/Article/details/6105233.sHtML
http://www.blog.jnjpgf.cn/Article/details/4379.sHtML
http://www.blog.jnjpgf.cn/Article/details/5451.sHtML
http://www.blog.jnjpgf.cn/Article/details/077861.sHtML
http://www.blog.jnjpgf.cn/Article/details/63739.sHtML
http://www.blog.jnjpgf.cn/Article/details/652635.sHtML
http://www.blog.jnjpgf.cn/Article/details/10032.sHtML
http://www.blog.jnjpgf.cn/Article/details/8546940.sHtML
http://www.blog.jnjpgf.cn/Article/details/865356.sHtML
http://www.blog.jnjpgf.cn/Article/details/946723.sHtML
http://www.blog.jnjpgf.cn/Article/details/608621.sHtML
http://www.blog.jnjpgf.cn/Article/details/905105.sHtML
http://www.blog.jnjpgf.cn/Article/details/927531.sHtML
http://www.blog.jnjpgf.cn/Article/details/466136.sHtML
http://www.blog.jnjpgf.cn/Article/details/758988.sHtML
http://www.blog.jnjpgf.cn/Article/details/399742.sHtML
http://www.blog.jnjpgf.cn/Article/details/96389.sHtML
http://www.blog.jnjpgf.cn/Article/details/4380399.sHtML
http://www.blog.jnjpgf.cn/Article/details/9974.sHtML
http://www.blog.jnjpgf.cn/Article/details/1049382.sHtML
http://www.blog.jnjpgf.cn/Article/details/1631.sHtML
http://www.blog.jnjpgf.cn/Article/details/8818.sHtML
http://www.blog.jnjpgf.cn/Article/details/7982723.sHtML
http://www.blog.jnjpgf.cn/Article/details/238593.sHtML
http://www.blog.jnjpgf.cn/Article/details/9455946.sHtML
http://www.blog.jnjpgf.cn/Article/details/9830.sHtML
http://www.blog.jnjpgf.cn/Article/details/3340.sHtML
http://www.blog.jnjpgf.cn/Article/details/1891086.sHtML
http://www.blog.jnjpgf.cn/Article/details/2391.sHtML
http://www.blog.jnjpgf.cn/Article/details/8477820.sHtML
http://www.blog.jnjpgf.cn/Article/details/47710.sHtML
http://www.blog.jnjpgf.cn/Article/details/0980378.sHtML
http://www.blog.jnjpgf.cn/Article/details/665741.sHtML
http://www.blog.jnjpgf.cn/Article/details/6300811.sHtML
http://www.blog.jnjpgf.cn/Article/details/148192.sHtML
http://www.blog.jnjpgf.cn/Article/details/0415.sHtML
http://www.blog.jnjpgf.cn/Article/details/8284091.sHtML
http://www.blog.jnjpgf.cn/Article/details/74032.sHtML
http://www.blog.jnjpgf.cn/Article/details/77536.sHtML
http://www.blog.jnjpgf.cn/Article/details/3981356.sHtML
http://www.blog.jnjpgf.cn/Article/details/8196.sHtML
http://www.blog.jnjpgf.cn/Article/details/6159156.sHtML
http://www.blog.jnjpgf.cn/Article/details/997377.sHtML
http://www.blog.jnjpgf.cn/Article/details/2036189.sHtML
http://www.blog.jnjpgf.cn/Article/details/7270290.sHtML
http://www.blog.jnjpgf.cn/Article/details/89643.sHtML
http://www.blog.jnjpgf.cn/Article/details/2061.sHtML
http://www.blog.jnjpgf.cn/Article/details/7062.sHtML
http://www.blog.jnjpgf.cn/Article/details/16221.sHtML
http://www.blog.jnjpgf.cn/Article/details/7326.sHtML
http://www.blog.jnjpgf.cn/Article/details/3702.sHtML
http://www.blog.jnjpgf.cn/Article/details/66261.sHtML
http://www.blog.jnjpgf.cn/Article/details/893023.sHtML
http://www.blog.jnjpgf.cn/Article/details/47818.sHtML
http://www.blog.jnjpgf.cn/Article/details/3079957.sHtML
http://www.blog.jnjpgf.cn/Article/details/328526.sHtML
http://www.blog.jnjpgf.cn/Article/details/0574275.sHtML
http://www.blog.jnjpgf.cn/Article/details/306795.sHtML
http://www.blog.jnjpgf.cn/Article/details/7804515.sHtML
http://www.blog.jnjpgf.cn/Article/details/1075.sHtML
http://www.blog.jnjpgf.cn/Article/details/53013.sHtML
http://www.blog.jnjpgf.cn/Article/details/858224.sHtML
http://www.blog.jnjpgf.cn/Article/details/9389.sHtML
http://www.blog.jnjpgf.cn/Article/details/5211749.sHtML
http://www.blog.jnjpgf.cn/Article/details/57942.sHtML
http://www.blog.jnjpgf.cn/Article/details/90657.sHtML
http://www.blog.jnjpgf.cn/Article/details/2264984.sHtML
http://www.blog.jnjpgf.cn/Article/details/908563.sHtML
http://www.blog.jnjpgf.cn/Article/details/4905300.sHtML
http://www.blog.jnjpgf.cn/Article/details/6029043.sHtML
http://www.blog.jnjpgf.cn/Article/details/9550208.sHtML
http://www.blog.jnjpgf.cn/Article/details/7275.sHtML
http://www.blog.jnjpgf.cn/Article/details/9843068.sHtML
http://www.blog.jnjpgf.cn/Article/details/4720.sHtML
http://www.blog.jnjpgf.cn/Article/details/1087.sHtML
http://www.blog.jnjpgf.cn/Article/details/2583242.sHtML
http://www.blog.jnjpgf.cn/Article/details/283639.sHtML
http://www.blog.jnjpgf.cn/Article/details/1879.sHtML
http://www.blog.jnjpgf.cn/Article/details/310373.sHtML
http://www.blog.jnjpgf.cn/Article/details/0288615.sHtML
http://www.blog.jnjpgf.cn/Article/details/954246.sHtML

## 项目结构

```
resource-bridge/
├── data/
│   ├── batches/               # 按批次存放资源列表 (YAML)
│   │   └── 211.yaml           # 第211批资源元数据
│   ├── categories.yaml        # 分类体系定义
│   └── tags.yaml              # 标签库
├── scripts/
│   ├── import_urls.py         # 从文本文件批量导入URL
│   ├── check_links.py         # 链接健康状态检查
│   └── deduplicate.py         # 资源去重工具
├── src/
│   ├── parser.py              # 资源条目解析器
│   ├── indexer.py             # 全文索引构建模块
│   ├── renderer.py            # Jinja2模板渲染引擎封装
│   └── utils.py               # 通用工具函数
├── templates/
│   ├── base.html              # 基础页面模板
│   ├── index.html             # 资源列表页模板
│   └── detail.html            # 单条资源详情页模板
├── dist/                      # 静态站点构建输出目录 (生成)
├── tests/
│   ├── test_parser.py         # 解析器单元测试
│   └── test_indexer.py        # 索引器单元测试
├── docs/
│   ├── getting-started.md     # 入门指南
│   └── api-reference.md       # API参考文档
├── requirements.txt           # Python依赖声明
├── build.py                   # 主构建脚本
└── README.md                  # 项目说明文档
```

## 贡献指南

1. 在 GitHub 上 Fork 本仓库，并克隆到本地开发环境。确保使用 Python 3.9 及以上版本，并安装所有开发依赖 (pip install -r requirements-dev.txt)。

2. 新增资源条目时，请按照 data/batches/ 目录下已有 YAML 文件的格式编写，确保每条记录包含 id、url、title、category 和 tags 字段。提交前运行 scripts/deduplicate.py 检查是否与现有条目重复。

3. 若需修改模板样式或页面布局，请编辑 templates/ 目录下的 HTML 文件，并在本地执行 build.py 构建后预览效果。模板变量定义请参考 docs/template-customization.md。

4. 提交 Pull Request 前，请确保所有单元测试通过 (pytest tests/)，并在 PR 描述中简要说明变更内容与测试覆盖情况。涉及链接变更的 PR 需附带链接健康检查报告。

5. 对于重大功能更新或架构调整，请先在 Issues 中发起讨论，获得核心维护者反馈后再进行开发，避免无效工作。

## 常见问题

**问：如何更新已导入的资源链接或修改元数据？**

答：资源数据以 YAML 格式存储在 data/batches/ 目录下，每个批次一个文件。您可以直接编辑对应的 YAML 文件修改 url、title、category 等字段，然后重新运行 build.py 即可生成更新后的静态页面。修改前建议使用 scripts/deduplicate.py 检查是否有编号冲突或重复条目。

**问：支持从浏览器书签或其他格式迁移吗？**

答：ResourceBridge 提供了通用的导入脚本 import_urls.py，支持纯文本每行一个 URL 的格式、Netscape 书签导出格式 (HTML)、以及 CSV 格式。您可以通过 --format 参数指定输入格式。对于不支持的格式，可先将数据整理为上述三种格式之一再进行导入。

**问：静态站点如何部署到生产环境？**

答：执行 build.py 后，所有生成的 HTML、CSS、JavaScript 文件均输出到 dist/ 目录。您可以将该目录部署到任何支持静态文件的 Web 服务器（如 Nginx、Apache）、对象存储服务（如 AWS S3、阿里云 OSS）或静态托管平台（如 GitHub Pages、Netlify）。无需额外运行时环境。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:29:34
