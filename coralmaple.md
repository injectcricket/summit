# LinkVault Resource Aggregator

LinkVault 是一个面向开发者、技术研究人员以及信息分析师的轻量级技术资源外链聚合与导航系统。该项目不存储任何实际内容，仅提供结构化、可检索的外部链接索引服务，帮助用户从分散的网络资源中快速定位具有参考价值的技术文章、案例分析、数据快照及开发日志。

项目定位为纯静态外链门户，适用于个人或小团队搭建内部技术知识库的入口层，通过简单的链接分类与元数据标注，解决信息过载时代下“已知资源但无法高效回溯”的痛点。LinkVault 本身不依赖后端数据库，所有链接数据以 Markdown 或 YAML 格式维护，支持静态站点生成器直接编译，亦可嵌入现有文档平台。

## 功能概览

**多级分类索引**：支持按技术领域、内容类型、时间跨度对链接进行多维度分组，提供清晰的导航路径。

**原样链接透传**：所有外链以原始 URL 形式完整保留，不进行重定向、短链转换或参数追加，确保访问路径的确定性。

**批量导入与校验**：提供脚本工具，支持从 CSV 或 JSON 批量导入链接列表，并自动校验 URL 可达性及协议一致性。

**静态化输出**：项目构建时生成纯 HTML 目录页，无需运行时数据库或服务端进程，可直接部署于对象存储或 CDN。

**全文检索占位**：预留与第三方站内搜索组件（如 Pagefind、Algolia）的集成接口，便于对链接标题及描述进行客户端检索。

**访问审计日志**：可选开启轻量级访问日志记录功能，统计各链接的点击频次，辅助评估资源热度。

## 应用场景

技术团队内部知识库入口：研发团队可将日常踩坑记录、第三方库文档、官方公告等外链统一收归至 LinkVault，新成员入职时可快速了解团队常用技术参考源，减少重复沟通成本。

个人开发者的阅读清单管理：自由职业者或独立开发者可使用 LinkVault 维护个人技术阅读列表，按周或按月归档高质量博客与教程，避免浏览器书签过多导致的检索效率下降问题。

数据分析项目的外部数据源索引：在进行市场分析或学术研究时，研究者常需引用大量网页数据快照。LinkVault 可作为数据源清单管理工具，确保每一份引用链接均有据可查，便于后续复查。

离线文档配套导航：对于部署于内网或离线环境的文档站，LinkVault 可作为外部网络资源的映射表，明确标注哪些内容需联网访问，辅助网络策略配置。

## 快速开始

以下步骤适用于 Linux / macOS / Windows WSL 环境，确保已安装 Git 与 Node.js 16.x 或以上版本。

```bash
# 克隆仓库到本地
git clone https://github.com/your-org/linkvault.git
cd linkvault

# 安装依赖（使用 npm 或 yarn）
npm install

# 构建静态站点（输出目录为 dist/）
npm run build
```

构建完成后，将 `dist/` 目录下的所有文件上传至任意静态托管服务（如 Nginx、S3、Cloudflare Pages）即可上线。开发模式下可使用 `npm run dev` 启动本地预览服务器，默认监听端口 8080。

## 安装要求

| 依赖组件 | 必需版本 | 说明 |
|---------|---------|------|
| Node.js | 16.x 或更高 | 运行时环境，用于执行构建脚本与依赖管理 |
| npm | 8.x 或更高 | 包管理器，用于安装项目依赖及运行脚本 |
| Git | 2.30 或更高 | 版本控制工具，用于克隆仓库及管理链接数据变更 |
| YAML 解析器 | 项目内置 | 用于解析链接分类配置文件，无需独立安装 |
| 静态 Web 服务器 | 任意（推荐 Nginx 1.20+） | 生产环境用于托管构建后的静态文件 |
| 现代浏览器 | Chrome 90+ / Firefox 88+ | 访问最终生成的导航页面，支持 ES6 语法 |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|------|------|-----------|
| 入门指南 | docs/getting-started.md | 如何快速部署一个最小化实例，以及首次配置需要修改哪些文件 |
| 链接分类规范 | docs/categorization.md | 如何定义分类层级、标签体系以及链接元数据字段的填写规则 |
| 构建与部署 | docs/build-deploy.md | 针对不同托管平台（Vercel、Netlify、Cloudflare）的构建参数与部署策略 |
| 故障排除 | docs/troubleshooting.md | 常见构建错误、链接访问超时以及页面空白等问题的排查流程 |
| 接口扩展 | docs/api-extension.md | 如何编写自定义钩子函数以处理链接导入前/后的数据转换逻辑 |

## 资源列表

### 核心技术文章索引（第一批次）

http://www.blog.puhvjy.cn/Article/details/496619.sHtML
http://www.blog.puhvjy.cn/Article/details/709685.sHtML
http://www.blog.puhvjy.cn/Article/details/6743486.sHtML
http://www.blog.puhvjy.cn/Article/details/3492956.sHtML
http://www.blog.puhvjy.cn/Article/details/7066.sHtML
http://www.blog.puhvjy.cn/Article/details/618992.sHtML
http://www.blog.puhvjy.cn/Article/details/616866.sHtML
http://www.blog.puhvjy.cn/Article/details/0542430.sHtML
http://www.blog.puhvjy.cn/Article/details/22774.sHtML
http://www.blog.puhvjy.cn/Article/details/65626.sHtML
http://www.blog.puhvjy.cn/Article/details/587826.sHtML
http://www.blog.puhvjy.cn/Article/details/745350.sHtML
http://www.blog.puhvjy.cn/Article/details/125254.sHtML
http://www.blog.puhvjy.cn/Article/details/365662.sHtML
http://www.blog.puhvjy.cn/Article/details/383222.sHtML
http://www.blog.puhvjy.cn/Article/details/7842471.sHtML
http://www.blog.puhvjy.cn/Article/details/8155.sHtML
http://www.blog.puhvjy.cn/Article/details/5394501.sHtML
http://www.blog.puhvjy.cn/Article/details/7173196.sHtML
http://www.blog.puhvjy.cn/Article/details/8412.sHtML
http://www.blog.puhvjy.cn/Article/details/2377.sHtML
http://www.blog.puhvjy.cn/Article/details/671871.sHtML
http://www.blog.puhvjy.cn/Article/details/24632.sHtML
http://www.blog.puhvjy.cn/Article/details/2193.sHtML
http://www.blog.puhvjy.cn/Article/details/0430376.sHtML
http://www.blog.puhvjy.cn/Article/details/81314.sHtML
http://www.blog.puhvjy.cn/Article/details/08516.sHtML
http://www.blog.puhvjy.cn/Article/details/08016.sHtML
http://www.blog.puhvjy.cn/Article/details/8064778.sHtML
http://www.blog.puhvjy.cn/Article/details/4603127.sHtML
http://www.blog.puhvjy.cn/Article/details/4131445.sHtML
http://www.blog.puhvjy.cn/Article/details/03437.sHtML
http://www.blog.puhvjy.cn/Article/details/7209546.sHtML
http://www.blog.puhvjy.cn/Article/details/2667.sHtML
http://www.blog.puhvjy.cn/Article/details/975601.sHtML
http://www.blog.puhvjy.cn/Article/details/42940.sHtML
http://www.blog.puhvjy.cn/Article/details/15959.sHtML
http://www.blog.puhvjy.cn/Article/details/91958.sHtML
http://www.blog.puhvjy.cn/Article/details/2344999.sHtML
http://www.blog.puhvjy.cn/Article/details/3197522.sHtML
http://www.blog.puhvjy.cn/Article/details/7609030.sHtML
http://www.blog.puhvjy.cn/Article/details/6675.sHtML
http://www.blog.puhvjy.cn/Article/details/673514.sHtML
http://www.blog.puhvjy.cn/Article/details/937634.sHtML
http://www.blog.puhvjy.cn/Article/details/680699.sHtML
http://www.blog.puhvjy.cn/Article/details/38650.sHtML
http://www.blog.puhvjy.cn/Article/details/9075047.sHtML
http://www.blog.puhvjy.cn/Article/details/688035.sHtML
http://www.blog.puhvjy.cn/Article/details/958363.sHtML
http://www.blog.puhvjy.cn/Article/details/26993.sHtML
http://www.blog.puhvjy.cn/Article/details/559250.sHtML
http://www.blog.puhvjy.cn/Article/details/971707.sHtML
http://www.blog.puhvjy.cn/Article/details/1132.sHtML
http://www.blog.puhvjy.cn/Article/details/3432183.sHtML
http://www.blog.puhvjy.cn/Article/details/2613758.sHtML
http://www.blog.puhvjy.cn/Article/details/0620.sHtML
http://www.blog.puhvjy.cn/Article/details/0753302.sHtML
http://www.blog.puhvjy.cn/Article/details/69333.sHtML
http://www.blog.puhvjy.cn/Article/details/0366685.sHtML
http://www.blog.puhvjy.cn/Article/details/565221.sHtML
http://www.blog.puhvjy.cn/Article/details/6380.sHtML
http://www.blog.puhvjy.cn/Article/details/6923.sHtML
http://www.blog.puhvjy.cn/Article/details/8574617.sHtML
http://www.blog.puhvjy.cn/Article/details/4433991.sHtML
http://www.blog.puhvjy.cn/Article/details/8161810.sHtML
http://www.blog.puhvjy.cn/Article/details/4424.sHtML
http://www.blog.puhvjy.cn/Article/details/9877.sHtML
http://www.blog.puhvjy.cn/Article/details/6869.sHtML
http://www.blog.puhvjy.cn/Article/details/860600.sHtML
http://www.blog.puhvjy.cn/Article/details/73600.sHtML
http://www.blog.puhvjy.cn/Article/details/1192.sHtML
http://www.blog.puhvjy.cn/Article/details/0909.sHtML
http://www.blog.puhvjy.cn/Article/details/36272.sHtML
http://www.blog.puhvjy.cn/Article/details/80591.sHtML
http://www.blog.puhvjy.cn/Article/details/0858.sHtML
http://www.blog.puhvjy.cn/Article/details/5791.sHtML
http://www.blog.puhvjy.cn/Article/details/895858.sHtML
http://www.blog.puhvjy.cn/Article/details/031724.sHtML
http://www.blog.puhvjy.cn/Article/details/249275.sHtML
http://www.blog.puhvjy.cn/Article/details/09005.sHtML
http://www.blog.puhvjy.cn/Article/details/5633887.sHtML
http://www.blog.puhvjy.cn/Article/details/45571.sHtML
http://www.blog.puhvjy.cn/Article/details/453790.sHtML
http://www.blog.puhvjy.cn/Article/details/4186902.sHtML
http://www.blog.puhvjy.cn/Article/details/189350.sHtML
http://www.blog.puhvjy.cn/Article/details/5124995.sHtML
http://www.blog.puhvjy.cn/Article/details/5949.sHtML
http://www.blog.puhvjy.cn/Article/details/49424.sHtML
http://www.blog.puhvjy.cn/Article/details/3452153.sHtML
http://www.blog.puhvjy.cn/Article/details/894469.sHtML
http://www.blog.puhvjy.cn/Article/details/4512.sHtML
http://www.blog.puhvjy.cn/Article/details/6857.sHtML
http://www.blog.puhvjy.cn/Article/details/8888.sHtML
http://www.blog.puhvjy.cn/Article/details/7934.sHtML
http://www.blog.puhvjy.cn/Article/details/9362.sHtML
http://www.blog.puhvjy.cn/Article/details/93497.sHtML
http://www.blog.puhvjy.cn/Article/details/770475.sHtML
http://www.blog.puhvjy.cn/Article/details/7982921.sHtML
http://www.blog.puhvjy.cn/Article/details/2009521.sHtML
http://www.blog.puhvjy.cn/Article/details/30213.sHtML
http://www.blog.puhvjy.cn/Article/details/8635.sHtML
http://www.blog.puhvjy.cn/Article/details/260821.sHtML
http://www.blog.puhvjy.cn/Article/details/7955.sHtML
http://www.blog.puhvjy.cn/Article/details/4390823.sHtML
http://www.blog.puhvjy.cn/Article/details/3000321.sHtML
http://www.blog.puhvjy.cn/Article/details/3636601.sHtML
http://www.blog.puhvjy.cn/Article/details/91600.sHtML
http://www.blog.puhvjy.cn/Article/details/97694.sHtML
http://www.blog.puhvjy.cn/Article/details/890193.sHtML
http://www.blog.puhvjy.cn/Article/details/6317.sHtML
http://www.blog.puhvjy.cn/Article/details/418217.sHtML
http://www.blog.puhvjy.cn/Article/details/66524.sHtML
http://www.blog.puhvjy.cn/Article/details/51943.sHtML
http://www.blog.puhvjy.cn/Article/details/75047.sHtML
http://www.blog.puhvjy.cn/Article/details/8208.sHtML
http://www.blog.puhvjy.cn/Article/details/9370.sHtML
http://www.blog.puhvjy.cn/Article/details/9363052.sHtML
http://www.blog.puhvjy.cn/Article/details/33852.sHtML
http://www.blog.puhvjy.cn/Article/details/0161006.sHtML
http://www.blog.puhvjy.cn/Article/details/2501650.sHtML
http://www.blog.puhvjy.cn/Article/details/54780.sHtML
http://www.blog.puhvjy.cn/Article/details/86712.sHtML
http://www.blog.puhvjy.cn/Article/details/96312.sHtML
http://www.blog.puhvjy.cn/Article/details/0667.sHtML
http://www.blog.puhvjy.cn/Article/details/526286.sHtML
http://www.blog.puhvjy.cn/Article/details/96417.sHtML
http://www.blog.puhvjy.cn/Article/details/7281793.sHtML
http://www.blog.puhvjy.cn/Article/details/17700.sHtML
http://www.blog.puhvjy.cn/Article/details/400017.sHtML
http://www.blog.puhvjy.cn/Article/details/4358811.sHtML
http://www.blog.puhvjy.cn/Article/details/5048.sHtML
http://www.blog.puhvjy.cn/Article/details/59314.sHtML
http://www.blog.puhvjy.cn/Article/details/70251.sHtML
http://www.blog.puhvjy.cn/Article/details/3751727.sHtML
http://www.blog.puhvjy.cn/Article/details/56099.sHtML
http://www.blog.puhvjy.cn/Article/details/9780.sHtML
http://www.blog.puhvjy.cn/Article/details/17338.sHtML
http://www.blog.puhvjy.cn/Article/details/2037604.sHtML
http://www.blog.puhvjy.cn/Article/details/1508.sHtML
http://www.blog.puhvjy.cn/Article/details/111910.sHtML
http://www.blog.puhvjy.cn/Article/details/9564284.sHtML
http://www.blog.puhvjy.cn/Article/details/609659.sHtML
http://www.blog.puhvjy.cn/Article/details/2283644.sHtML
http://www.blog.puhvjy.cn/Article/details/5754622.sHtML
http://www.blog.puhvjy.cn/Article/details/372263.sHtML
http://www.blog.puhvjy.cn/Article/details/1019446.sHtML
http://www.blog.puhvjy.cn/Article/details/58851.sHtML
http://www.blog.puhvjy.cn/Article/details/919707.sHtML
http://www.blog.puhvjy.cn/Article/details/27862.sHtML
http://www.blog.puhvjy.cn/Article/details/749219.sHtML
http://www.blog.puhvjy.cn/Article/details/5459590.sHtML
http://www.blog.puhvjy.cn/Article/details/0296.sHtML
http://www.blog.puhvjy.cn/Article/details/345458.sHtML
http://www.blog.puhvjy.cn/Article/details/9826329.sHtML
http://www.blog.puhvjy.cn/Article/details/75108.sHtML
http://www.blog.puhvjy.cn/Article/details/9659363.sHtML
http://www.blog.puhvjy.cn/Article/details/813736.sHtML
http://www.blog.puhvjy.cn/Article/details/26165.sHtML
http://www.blog.puhvjy.cn/Article/details/75020.sHtML
http://www.blog.puhvjy.cn/Article/details/4134626.sHtML
http://www.blog.puhvjy.cn/Article/details/5059870.sHtML
http://www.blog.puhvjy.cn/Article/details/70429.sHtML
http://www.blog.puhvjy.cn/Article/details/8699368.sHtML
http://www.blog.puhvjy.cn/Article/details/369791.sHtML
http://www.blog.puhvjy.cn/Article/details/5614.sHtML
http://www.blog.puhvjy.cn/Article/details/96687.sHtML
http://www.blog.puhvjy.cn/Article/details/7968866.sHtML
http://www.blog.puhvjy.cn/Article/details/413722.sHtML
http://www.blog.puhvjy.cn/Article/details/77965.sHtML
http://www.blog.puhvjy.cn/Article/details/6916150.sHtML
http://www.blog.puhvjy.cn/Article/details/569259.sHtML
http://www.blog.puhvjy.cn/Article/details/3246.sHtML
http://www.blog.puhvjy.cn/Article/details/9090.sHtML
http://www.blog.puhvjy.cn/Article/details/288609.sHtML
http://www.blog.puhvjy.cn/Article/details/049698.sHtML
http://www.blog.puhvjy.cn/Article/details/61617.sHtML
http://www.blog.puhvjy.cn/Article/details/0362.sHtML
http://www.blog.puhvjy.cn/Article/details/921156.sHtML
http://www.blog.puhvjy.cn/Article/details/362105.sHtML
http://www.blog.puhvjy.cn/Article/details/78142.sHtML
http://www.blog.puhvjy.cn/Article/details/07136.sHtML
http://www.blog.puhvjy.cn/Article/details/23049.sHtML
http://www.blog.puhvjy.cn/Article/details/05769.sHtML
http://www.blog.puhvjy.cn/Article/details/0140378.sHtML
http://www.blog.puhvjy.cn/Article/details/820329.sHtML
http://www.blog.puhvjy.cn/Article/details/9415.sHtML
http://www.blog.puhvjy.cn/Article/details/4224.sHtML
http://www.blog.puhvjy.cn/Article/details/22911.sHtML
http://www.blog.puhvjy.cn/Article/details/591648.sHtML
http://www.blog.puhvjy.cn/Article/details/32233.sHtML
http://www.blog.puhvjy.cn/Article/details/676777.sHtML
http://www.blog.puhvjy.cn/Article/details/600215.sHtML
http://www.blog.puhvjy.cn/Article/details/8535.sHtML
http://www.blog.puhvjy.cn/Article/details/171314.sHtML
http://www.blog.puhvjy.cn/Article/details/58632.sHtML
http://www.blog.puhvjy.cn/Article/details/795378.sHtML
http://www.blog.puhvjy.cn/Article/details/967838.sHtML
http://www.blog.puhvjy.cn/Article/details/754989.sHtML
http://www.blog.puhvjy.cn/Article/details/076942.sHtML
http://www.blog.puhvjy.cn/Article/details/832044.sHtML
http://www.blog.puhvjy.cn/Article/details/04366.sHtML
http://www.blog.puhvjy.cn/Article/details/1175.sHtML
http://www.blog.puhvjy.cn/Article/details/86541.sHtML
http://www.blog.puhvjy.cn/Article/details/257175.sHtML
http://www.blog.puhvjy.cn/Article/details/9683.sHtML
http://www.blog.puhvjy.cn/Article/details/3507.sHtML
http://www.blog.puhvjy.cn/Article/details/052636.sHtML
http://www.blog.puhvjy.cn/Article/details/46240.sHtML
http://www.blog.puhvjy.cn/Article/details/8105.sHtML
http://www.blog.puhvjy.cn/Article/details/4257059.sHtML
http://www.blog.puhvjy.cn/Article/details/4195.sHtML
http://www.blog.puhvjy.cn/Article/details/8822.sHtML
http://www.blog.puhvjy.cn/Article/details/64276.sHtML
http://www.blog.puhvjy.cn/Article/details/0535352.sHtML
http://www.blog.puhvjy.cn/Article/details/863013.sHtML
http://www.blog.puhvjy.cn/Article/details/90116.sHtML
http://www.blog.puhvjy.cn/Article/details/8190.sHtML
http://www.blog.puhvjy.cn/Article/details/899784.sHtML
http://www.blog.puhvjy.cn/Article/details/452622.sHtML
http://www.blog.puhvjy.cn/Article/details/178181.sHtML
http://www.blog.puhvjy.cn/Article/details/7232850.sHtML
http://www.blog.puhvjy.cn/Article/details/198740.sHtML
http://www.blog.puhvjy.cn/Article/details/1398256.sHtML
http://www.blog.puhvjy.cn/Article/details/8037347.sHtML
http://www.blog.puhvjy.cn/Article/details/547528.sHtML
http://www.blog.puhvjy.cn/Article/details/4920.sHtML
http://www.blog.puhvjy.cn/Article/details/9884.sHtML
http://www.blog.puhvjy.cn/Article/details/7790.sHtML
http://www.blog.puhvjy.cn/Article/details/0857387.sHtML
http://www.blog.puhvjy.cn/Article/details/7064.sHtML
http://www.blog.puhvjy.cn/Article/details/912764.sHtML
http://www.blog.puhvjy.cn/Article/details/6163605.sHtML
http://www.blog.puhvjy.cn/Article/details/30907.sHtML
http://www.blog.puhvjy.cn/Article/details/00075.sHtML
http://www.blog.puhvjy.cn/Article/details/9890.sHtML
http://www.blog.puhvjy.cn/Article/details/688973.sHtML
http://www.blog.puhvjy.cn/Article/details/905262.sHtML
http://www.blog.puhvjy.cn/Article/details/1899.sHtML
http://www.blog.puhvjy.cn/Article/details/17173.sHtML
http://www.blog.puhvjy.cn/Article/details/680466.sHtML
http://www.blog.puhvjy.cn/Article/details/6390309.sHtML
http://www.blog.puhvjy.cn/Article/details/808692.sHtML
http://www.blog.puhvjy.cn/Article/details/866353.sHtML
http://www.blog.puhvjy.cn/Article/details/3360896.sHtML
http://www.blog.puhvjy.cn/Article/details/801684.sHtML
http://www.blog.puhvjy.cn/Article/details/828404.sHtML
http://www.blog.puhvjy.cn/Article/details/771006.sHtML
http://www.blog.puhvjy.cn/Article/details/119290.sHtML
http://www.blog.puhvjy.cn/Article/details/7496728.sHtML
http://www.blog.puhvjy.cn/Article/details/5788.sHtML

## 项目结构

```
linkvault/
├── src/                              # 源代码主目录
│   ├── index.js                      # 入口脚本，负责读取配置并触发构建流程
│   ├── parser/                       # 链接解析模块
│   │   ├── yaml-loader.js           # 加载并校验 links.yaml 配置文件
│   │   └── url-normalizer.js        # 对输入 URL 做基本格式清洗（但保留协议）
│   ├── generator/                    # 静态页面生成器
│   │   ├── page-builder.js          # 构建 HTML 目录页主逻辑
│   │   └── template-engine.js       # 模板引擎，支持 EJS 语法渲染
│   ├── utils/                        # 通用工具函数集
│   │   ├── logger.js                # 日志输出工具，支持分级打印
│   │   └── validator.js             # 链接可达性校验（非阻塞）
│   └── hooks/                        # 用户可扩展钩子
│       └── custom-transform.js      # 示例钩子，用于链接标题自动补全
├── config/                           # 项目全局配置目录
│   ├── site.yaml                    # 站点名称、描述、构建目标等基础配置
│   └── links.yaml                   # 核心链接数据，按分类维护
├── docs/                             # 详细文档目录
│   ├── getting-started.md
│   ├── categorization.md
│   ├── build-deploy.md
│   ├── troubleshooting.md
│   └── api-extension.md
├── dist/                             # 构建输出目录（git 忽略，运行时生成）
│   └── index.html                   # 最终生成的导航主页
├── scripts/                          # 辅助脚本
│   ├── import-csv.js                # 从 CSV 导入链接列表
│   └── validate-urls.js             # 批量校验链接状态
├── .gitignore                        # Git 忽略规则
├── package.json                      # npm 项目依赖及脚本定义
└── README.md                         # 项目说明文件（本文件）
```

## 贡献指南

1. 问题追踪与提案提交：请在 GitHub Issues 中描述你发现的问题或希望新增的功能，使用提供的模板填写运行环境、复现步骤及预期行为。对于重大变更，建议先创建 Discussion 进行讨论。

2. 链接数据补充流程：若希望向资源列表中添加新链接，请编辑 `config/links.yaml` 文件，遵循既有的分类结构和字段格式（标题、URL、标签、简述），提交 Pull Request 时需附带链接的有效性说明。

3. 本地开发与测试：Fork 仓库后，在本地运行 `npm install` 及 `npm run test` 确保所有单元测试通过。新增功能需补充对应的测试用例，测试文件放置于 `test/` 目录下。

4. 代码风格规范：项目使用 ESLint + Prettier 统一代码风格，提交前请执行 `npm run lint` 和 `npm run format` 进行自动修复。Pull Request 描述中需注明变更类型（feat/fix/docs/chore）。

5. 文档同步更新：任何影响配置格式或构建流程的变更，需同步更新 `docs/` 下的相关文档，并确保示例代码与实际功能一致。

## 常见问题

Q: 构建时提示“链接校验超时”，是否会影响最终输出？
A: 默认配置下，链接校验采用非阻塞模式。超时或不可达的链接仅会在日志中标记为警告（WARN），不会中断构建流程，但会在生成的页面中添加 `data-unreachable` 属性，便于前端做样式标记。若需严格模式，可在 `config/site.yaml` 中设置 `strictValidation: true`。

Q: 如何自定义页面布局或添加品牌标识？
A: 项目使用 EJS 模板引擎，所有模板文件位于 `src/generator/templates/` 目录。您可直接修改 `index.ejs` 文件，调整 HTML 结构及 CSS 类名。静态资源（如图片、样式表）请放置于 `src/assets/`，构建时会自动复制到输出目录。

Q: 该项目是否支持多语言国际化？
A: 当前版本未内置 i18n 支持，但您可以通过在 `config/` 下创建不同语言的 YAML 文件（如 `links.zh.yaml`、`links.en.yaml`），并在构建命令中指定 `--lang` 参数来切换内容源。多语言路由需自行配置 Web 服务器进行路径重写。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:29:47
