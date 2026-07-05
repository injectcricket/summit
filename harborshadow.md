# Fuvxie Article Index Gateway

Fuvxie Article Index Gateway 是一个面向技术内容聚合与快速检索的轻量化索引服务。该项目不对原始文章内容进行转载或镜像，而是以结构化目录方式，对 fuvxie.cn 平台上的公开技术文章进行导航式整理，帮助开发者、研究人员与技术写作爱好者快速定位特定主题的历史技术文档。

该项目定位为技术资源外链汇总与索引增强层，适用于需要批量查阅 fuvxie.cn 历史技术文章、按文章 ID 进行快速跳转、以及构建本地化文章清单的使用场景。项目本身不依赖数据库，所有索引条目以静态清单方式维护，启动后提供基于文章编号的快速重定向与目录浏览能力。

## 功能概览

**批量文章索引**：收录 fuvxie.cn 平台自建站以来超过两百篇历史技术文章的原始访问链接，覆盖多个技术方向。

**按 ID 快速定位**：每条索引记录均以文章唯一数字 ID 为标识，支持通过 ID 直接构造访问路径，无需逐级翻页。

**纯静态资源聚合**：项目核心为静态链接清单，不依赖后端动态渲染，可部署于任何支持静态托管的 HTTP 服务器。

**分类筛选能力**：索引条目按文章主题领域进行初级分类，包括编程语言、系统运维、数据库、前端工程、算法与数据结构等。

**原始链接透传**：所有聚合链接均保留原始 URL 完整路径与大小写，确保与原站资源寻址完全一致，不引入二次跳转或中间页。

**轻量级本地服务**：项目附带基于 Node.js 的本地静态服务器，支持开发环境下快速启动预览，便于维护者增删条目后即时验证。

**零外部依赖核心**：索引清单本身为纯文本 Markdown 格式，无需安装额外依赖即可人工阅读和编辑。

**与自动化工具兼容**：索引条目格式规范统一，可被 grep、sed、awk 等命令行工具批量处理，便于集成到持续集成流水线中做链接存活检测。

## 应用场景

**技术文档回溯**：开发者在排查遗留系统问题时，需要查阅 fuvxie.cn 平台多年前发布的特定技术文章。通过本索引清单，可基于模糊记忆的文章主题快速遍历候选 ID，并直接跳转至原始文章页。

**内容运营参考**：技术博客运营人员需要了解 fuvxie.cn 历史内容的分布规律与热点编号区间。本索引提供了完整的文章 ID 清单，可用于统计分析发文频率、主题偏好以及编号段使用情况。

**个人知识库镜像辅助**：技术人员在建立自己的离线技术知识仓库时，可将本索引清单作为种子列表，配合离线下载工具批量获取 fuvxie.cn 上的公开文章，构建个人本地技术资料库。

## 快速开始

以下步骤适用于克隆项目后在本地环境启动索引预览服务。

```bash
# 克隆项目仓库
git clone https://github.com/your-org/fuvxie-article-index.git

# 进入项目目录
cd fuvxie-article-index

# 启动本地静态服务（默认端口 3000）
npm install -g serve
serve -p 3000
```

执行上述命令后，在浏览器中访问 `http://localhost:3000` 即可查看索引主页，所有聚合链接按分类陈列，点击即跳转至 fuvxie.cn 原始文章地址。

## 安装要求

| 依赖项 | 必需 | 说明 |
|--------|------|------|
| Node.js 14.x 或更高版本 | 是 | 用于运行本地预览服务与后续自动化脚本 |
| npm 6.x 或更高版本 | 是 | 包管理工具，用于安装 serve 等辅助工具 |
| 现代网页浏览器 | 是 | 用于本地预览索引页面，推荐 Chrome/Firefox/Edge 最新版本 |
| git 2.x 或更高版本 | 否 | 仅通过 git clone 方式获取源码时需要 |
| make 3.8+ 或 gnu make | 否 | 可选，用于执行项目中的辅助自动化任务 |
| curl/wget 工具集 | 否 | 可选，用于批量验证链接可达性 |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|------|------|------------|
| 入门指南 | docs/quick-start.md | 如何快速克隆项目并启动本地预览服务 |
| 索引维护 | docs/maintenance.md | 如何向索引清单中新增、删除或修改文章条目 |
| 分类规则 | docs/categorization.md | 文章按何种规则划分到编程语言、运维、数据库等类别 |
| 贡献流程 | CONTRIBUTING.md | 外部贡献者如何提交索引更新或改进建议 |

## 资源列表

本索引收录的全部原始文章链接如下，按文章 ID 数字升序排列。所有 URL 严格保留原始格式，未做任何协议、域名或路径改写。

### 早期文章段

http://www.blog.fuvxie.cn/Article/details/0200.sHtML

http://www.blog.fuvxie.cn/Article/details/0128.sHtML

http://www.blog.fuvxie.cn/Article/details/0138.sHtML

http://www.blog.fuvxie.cn/Article/details/0144.sHtML

http://www.blog.fuvxie.cn/Article/details/0254.sHtML

http://www.blog.fuvxie.cn/Article/details/0454.sHtML

http://www.blog.fuvxie.cn/Article/details/0477.sHtML

http://www.blog.fuvxie.cn/Article/details/04852.sHtML

http://www.blog.fuvxie.cn/Article/details/0514.sHtML

http://www.blog.fuvxie.cn/Article/details/0648.sHtML

http://www.blog.fuvxie.cn/Article/details/0676.sHtML

http://www.blog.fuvxie.cn/Article/details/0702.sHtML

http://www.blog.fuvxie.cn/Article/details/071089.sHtML

http://www.blog.fuvxie.cn/Article/details/0722.sHtML

http://www.blog.fuvxie.cn/Article/details/0768242.sHtML

http://www.blog.fuvxie.cn/Article/details/08490.sHtML

http://www.blog.fuvxie.cn/Article/details/088759.sHtML

http://www.blog.fuvxie.cn/Article/details/0908.sHtML

http://www.blog.fuvxie.cn/Article/details/097737.sHtML

http://www.blog.fuvxie.cn/Article/details/09968.sHtML

http://www.blog.fuvxie.cn/Article/details/000997.sHtML

### 一千至一万号段

http://www.blog.fuvxie.cn/Article/details/1156.sHtML

http://www.blog.fuvxie.cn/Article/details/1274.sHtML

http://www.blog.fuvxie.cn/Article/details/1506.sHtML

http://www.blog.fuvxie.cn/Article/details/1592.sHtML

http://www.blog.fuvxie.cn/Article/details/1849.sHtML

http://www.blog.fuvxie.cn/Article/details/2191.sHtML

http://www.blog.fuvxie.cn/Article/details/2739.sHtML

http://www.blog.fuvxie.cn/Article/details/3086.sHtML

http://www.blog.fuvxie.cn/Article/details/3121.sHtML

http://www.blog.fuvxie.cn/Article/details/32622.sHtML

http://www.blog.fuvxie.cn/Article/details/32690.sHtML

http://www.blog.fuvxie.cn/Article/details/34267.sHtML

http://www.blog.fuvxie.cn/Article/details/34889.sHtML

http://www.blog.fuvxie.cn/Article/details/35872.sHtML

http://www.blog.fuvxie.cn/Article/details/36285.sHtML

http://www.blog.fuvxie.cn/Article/details/3675.sHtML

http://www.blog.fuvxie.cn/Article/details/3792.sHtML

http://www.blog.fuvxie.cn/Article/details/39260.sHtML

http://www.blog.fuvxie.cn/Article/details/39947.sHtML

http://www.blog.fuvxie.cn/Article/details/4036.sHtML

http://www.blog.fuvxie.cn/Article/details/40618.sHtML

http://www.blog.fuvxie.cn/Article/details/41313.sHtML

http://www.blog.fuvxie.cn/Article/details/4172.sHtML

http://www.blog.fuvxie.cn/Article/details/4275.sHtML

http://www.blog.fuvxie.cn/Article/details/4463.sHtML

http://www.blog.fuvxie.cn/Article/details/4487.sHtML

http://www.blog.fuvxie.cn/Article/details/45559.sHtML

http://www.blog.fuvxie.cn/Article/details/46474.sHtML

http://www.blog.fuvxie.cn/Article/details/4884.sHtML

http://www.blog.fuvxie.cn/Article/details/49228.sHtML

http://www.blog.fuvxie.cn/Article/details/4952.sHtML

http://www.blog.fuvxie.cn/Article/details/4981.sHtML

http://www.blog.fuvxie.cn/Article/details/5058.sHtML

http://www.blog.fuvxie.cn/Article/details/51109.sHtML

http://www.blog.fuvxie.cn/Article/details/51473.sHtML

http://www.blog.fuvxie.cn/Article/details/52340.sHtML

http://www.blog.fuvxie.cn/Article/details/5421.sHtML

http://www.blog.fuvxie.cn/Article/details/5534.sHtML

http://www.blog.fuvxie.cn/Article/details/5578.sHtML

http://www.blog.fuvxie.cn/Article/details/5693.sHtML

http://www.blog.fuvxie.cn/Article/details/57965.sHtML

http://www.blog.fuvxie.cn/Article/details/5852.sHtML

http://www.blog.fuvxie.cn/Article/details/595991.sHtML

http://www.blog.fuvxie.cn/Article/details/601153.sHtML

http://www.blog.fuvxie.cn/Article/details/6080.sHtML

http://www.blog.fuvxie.cn/Article/details/609090.sHtML

http://www.blog.fuvxie.cn/Article/details/60948.sHtML

http://www.blog.fuvxie.cn/Article/details/6126.sHtML

http://www.blog.fuvxie.cn/Article/details/6212.sHtML

http://www.blog.fuvxie.cn/Article/details/62384.sHtML

http://www.blog.fuvxie.cn/Article/details/63197.sHtML

http://www.blog.fuvxie.cn/Article/details/6384512.sHtML

http://www.blog.fuvxie.cn/Article/details/64272.sHtML

http://www.blog.fuvxie.cn/Article/details/6470691.sHtML

http://www.blog.fuvxie.cn/Article/details/64792.sHtML

http://www.blog.fuvxie.cn/Article/details/6483.sHtML

http://www.blog.fuvxie.cn/Article/details/65525.sHtML

http://www.blog.fuvxie.cn/Article/details/662433.sHtML

http://www.blog.fuvxie.cn/Article/details/666384.sHtML

http://www.blog.fuvxie.cn/Article/details/670583.sHtML

http://www.blog.fuvxie.cn/Article/details/673002.sHtML

http://www.blog.fuvxie.cn/Article/details/6736.sHtML

http://www.blog.fuvxie.cn/Article/details/6739.sHtML

http://www.blog.fuvxie.cn/Article/details/67592.sHtML

http://www.blog.fuvxie.cn/Article/details/6769554.sHtML

http://www.blog.fuvxie.cn/Article/details/6787868.sHtML

http://www.blog.fuvxie.cn/Article/details/6793.sHtML

http://www.blog.fuvxie.cn/Article/details/6807441.sHtML

http://www.blog.fuvxie.cn/Article/details/6822.sHtML

http://www.blog.fuvxie.cn/Article/details/6824.sHtML

http://www.blog.fuvxie.cn/Article/details/686274.sHtML

http://www.blog.fuvxie.cn/Article/details/686822.sHtML

http://www.blog.fuvxie.cn/Article/details/6921106.sHtML

http://www.blog.fuvxie.cn/Article/details/692779.sHtML

http://www.blog.fuvxie.cn/Article/details/694456.sHtML

http://www.blog.fuvxie.cn/Article/details/6962.sHtML

http://www.blog.fuvxie.cn/Article/details/7014.sHtML

http://www.blog.fuvxie.cn/Article/details/702357.sHtML

http://www.blog.fuvxie.cn/Article/details/70386.sHtML

http://www.blog.fuvxie.cn/Article/details/7055.sHtML

http://www.blog.fuvxie.cn/Article/details/706110.sHtML

http://www.blog.fuvxie.cn/Article/details/7062.sHtML

http://www.blog.fuvxie.cn/Article/details/7088595.sHtML

http://www.blog.fuvxie.cn/Article/details/7097119.sHtML

http://www.blog.fuvxie.cn/Article/details/710553.sHtML

http://www.blog.fuvxie.cn/Article/details/7405573.sHtML

http://www.blog.fuvxie.cn/Article/details/7490.sHtML

http://www.blog.fuvxie.cn/Article/details/7520.sHtML

http://www.blog.fuvxie.cn/Article/details/7610.sHtML

http://www.blog.fuvxie.cn/Article/details/7672.sHtML

http://www.blog.fuvxie.cn/Article/details/7674.sHtML

http://www.blog.fuvxie.cn/Article/details/7679.sHtML

http://www.blog.fuvxie.cn/Article/details/770318.sHtML

http://www.blog.fuvxie.cn/Article/details/7841.sHtML

http://www.blog.fuvxie.cn/Article/details/7857.sHtML

http://www.blog.fuvxie.cn/Article/details/7937.sHtML

http://www.blog.fuvxie.cn/Article/details/794809.sHtML

http://www.blog.fuvxie.cn/Article/details/8012.sHtML

http://www.blog.fuvxie.cn/Article/details/8077.sHtML

http://www.blog.fuvxie.cn/Article/details/811552.sHtML

http://www.blog.fuvxie.cn/Article/details/815427.sHtML

http://www.blog.fuvxie.cn/Article/details/821347.sHtML

http://www.blog.fuvxie.cn/Article/details/8241.sHtML

http://www.blog.fuvxie.cn/Article/details/829230.sHtML

http://www.blog.fuvxie.cn/Article/details/83152.sHtML

http://www.blog.fuvxie.cn/Article/details/844417.sHtML

http://www.blog.fuvxie.cn/Article/details/8457.sHtML

http://www.blog.fuvxie.cn/Article/details/8511.sHtML

http://www.blog.fuvxie.cn/Article/details/8515208.sHtML

http://www.blog.fuvxie.cn/Article/details/8546.sHtML

http://www.blog.fuvxie.cn/Article/details/8547.sHtML

http://www.blog.fuvxie.cn/Article/details/8838.sHtML

http://www.blog.fuvxie.cn/Article/details/8866.sHtML

http://www.blog.fuvxie.cn/Article/details/89357.sHtML

http://www.blog.fuvxie.cn/Article/details/89565.sHtML

http://www.blog.fuvxie.cn/Article/details/8968.sHtML

http://www.blog.fuvxie.cn/Article/details/89775.sHtML

http://www.blog.fuvxie.cn/Article/details/903445.sHtML

http://www.blog.fuvxie.cn/Article/details/905342.sHtML

http://www.blog.fuvxie.cn/Article/details/905553.sHtML

http://www.blog.fuvxie.cn/Article/details/90672.sHtML

http://www.blog.fuvxie.cn/Article/details/906848.sHtML

http://www.blog.fuvxie.cn/Article/details/91055.sHtML

http://www.blog.fuvxie.cn/Article/details/91204.sHtML

http://www.blog.fuvxie.cn/Article/details/9131.sHtML

http://www.blog.fuvxie.cn/Article/details/9220.sHtML

http://www.blog.fuvxie.cn/Article/details/92632.sHtML

http://www.blog.fuvxie.cn/Article/details/9266823.sHtML

http://www.blog.fuvxie.cn/Article/details/932518.sHtML

http://www.blog.fuvxie.cn/Article/details/93750.sHtML

http://www.blog.fuvxie.cn/Article/details/9408821.sHtML

http://www.blog.fuvxie.cn/Article/details/94573.sHtML

http://www.blog.fuvxie.cn/Article/details/947206.sHtML

http://www.blog.fuvxie.cn/Article/details/94756.sHtML

http://www.blog.fuvxie.cn/Article/details/9529.sHtML

http://www.blog.fuvxie.cn/Article/details/96118.sHtML

http://www.blog.fuvxie.cn/Article/details/9613936.sHtML

http://www.blog.fuvxie.cn/Article/details/9663.sHtML

http://www.blog.fuvxie.cn/Article/details/9773444.sHtML

http://www.blog.fuvxie.cn/Article/details/98697.sHtML

http://www.blog.fuvxie.cn/Article/details/9890523.sHtML

http://www.blog.fuvxie.cn/Article/details/9957.sHtML

http://www.blog.fuvxie.cn/Article/details/99845.sHtML

### 十万以上号段与特殊编号

http://www.blog.fuvxie.cn/Article/details/013948.sHtML

http://www.blog.fuvxie.cn/Article/details/022471.sHtML

http://www.blog.fuvxie.cn/Article/details/0249443.sHtML

http://www.blog.fuvxie.cn/Article/details/0283561.sHtML

http://www.blog.fuvxie.cn/Article/details/0347704.sHtML

http://www.blog.fuvxie.cn/Article/details/047254.sHtML

http://www.blog.fuvxie.cn/Article/details/0597450.sHtML

http://www.blog.fuvxie.cn/Article/details/0659730.sHtML

http://www.blog.fuvxie.cn/Article/details/0716981.sHtML

http://www.blog.fuvxie.cn/Article/details/0751839.sHtML

http://www.blog.fuvxie.cn/Article/details/123577.sHtML

http://www.blog.fuvxie.cn/Article/details/1277985.sHtML

http://www.blog.fuvxie.cn/Article/details/1446461.sHtML

http://www.blog.fuvxie.cn/Article/details/14658.sHtML

http://www.blog.fuvxie.cn/Article/details/15129.sHtML

http://www.blog.fuvxie.cn/Article/details/164064.sHtML

http://www.blog.fuvxie.cn/Article/details/165113.sHtML

http://www.blog.fuvxie.cn/Article/details/1656858.sHtML

http://www.blog.fuvxie.cn/Article/details/168937.sHtML

http://www.blog.fuvxie.cn/Article/details/1690631.sHtML

http://www.blog.fuvxie.cn/Article/details/181648.sHtML

http://www.blog.fuvxie.cn/Article/details/1818763.sHtML

http://www.blog.fuvxie.cn/Article/details/185026.sHtML

http://www.blog.fuvxie.cn/Article/details/191115.sHtML

http://www.blog.fuvxie.cn/Article/details/19561.sHtML

http://www.blog.fuvxie.cn/Article/details/1986850.sHtML

http://www.blog.fuvxie.cn/Article/details/200542.sHtML

http://www.blog.fuvxie.cn/Article/details/229723.sHtML

http://www.blog.fuvxie.cn/Article/details/23927.sHtML

http://www.blog.fuvxie.cn/Article/details/25422.sHtML

http://www.blog.fuvxie.cn/Article/details/2624629.sHtML

http://www.blog.fuvxie.cn/Article/details/26550.sHtML

http://www.blog.fuvxie.cn/Article/details/2655868.sHtML

http://www.blog.fuvxie.cn/Article/details/265700.sHtML

http://www.blog.fuvxie.cn/Article/details/2675415.sHtML

http://www.blog.fuvxie.cn/Article/details/267938.sHtML

http://www.blog.fuvxie.cn/Article/details/27124.sHtML

http://www.blog.fuvxie.cn/Article/details/27942.sHtML

http://www.blog.fuvxie.cn/Article/details/294215.sHtML

http://www.blog.fuvxie.cn/Article/details/3138166.sHtML

http://www.blog.fuvxie.cn/Article/details/317053.sHtML

http://www.blog.fuvxie.cn/Article/details/321166.sHtML

http://www.blog.fuvxie.cn/Article/details/3427514.sHtML

http://www.blog.fuvxie.cn/Article/details/3487622.sHtML

http://www.blog.fuvxie.cn/Article/details/350270.sHtML

http://www.blog.fuvxie.cn/Article/details/3511895.sHtML

http://www.blog.fuvxie.cn/Article/details/355383.sHtML

http://www.blog.fuvxie.cn/Article/details/372599.sHtML

http://www.blog.fuvxie.cn/Article/details/378873.sHtML

http://www.blog.fuvxie.cn/Article/details/393081.sHtML

http://www.blog.fuvxie.cn/Article/details/394381.sHtML

http://www.blog.fuvxie.cn/Article/details/398555.sHtML

http://www.blog.fuvxie.cn/Article/details/4085914.sHtML

http://www.blog.fuvxie.cn/Article/details/4152841.sHtML

http://www.blog.fuvxie.cn/Article/details/4168851.sHtML

http://www.blog.fuvxie.cn/Article/details/424355.sHtML

http://www.blog.fuvxie.cn/Article/details/4286093.sHtML

http://www.blog.fuvxie.cn/Article/details/432561.sHtML

http://www.blog.fuvxie.cn/Article/details/4516126.sHtML

http://www.blog.fuvxie.cn/Article/details/465919.sHtML

http://www.blog.fuvxie.cn/Article/details/472090.sHtML

http://www.blog.fuvxie.cn/Article/details/4765969.sHtML

http://www.blog.fuvxie.cn/Article/details/480423.sHtML

http://www.blog.fuvxie.cn/Article/details/484516.sHtML

http://www.blog.fuvxie.cn/Article/details/487710.sHtML

http://www.blog.fuvxie.cn/Article/details/4880618.sHtML

http://www.blog.fuvxie.cn/Article/details/4948678.sHtML

http://www.blog.fuvxie.cn/Article/details/4987468.sHtML

http://www.blog.fuvxie.cn/Article/details/5004311.sHtML

http://www.blog.fuvxie.cn/Article/details/502375.sHtML

http://www.blog.fuvxie.cn/Article/details/523770.sHtML

http://www.blog.fuvxie.cn/Article/details/5289857.sHtML

http://www.blog.fuvxie.cn/Article/details/533169.sHtML

http://www.blog.fuvxie.cn/Article/details/5333689.sHtML

http://www.blog.fuvxie.cn/Article/details/5383455.sHtML

http://www.blog.fuvxie.cn/Article/details/539170.sHtML

http://www.blog.fuvxie.cn/Article/details/547781.sHtML

http://www.blog.fuvxie.cn/Article/details/562868.sHtML

http://www.blog.fuvxie.cn/Article/details/5713990.sHtML

http://www.blog.fuvxie.cn/Article/details/571626.sHtML

http://www.blog.fuvxie.cn/Article/details/5726771.sHtML

http://www.blog.fuvxie.cn/Article/details/5745464.sHtML

http://www.blog.fuvxie.cn/Article/details/6253819.sHtML

http://www.blog.fuvxie.cn/Article/details/6323880.sHtML

http://www.blog.fuvxie.cn/Article/details/0169120.sHtML

http://www.blog.fuvxie.cn/Article/details/8854572.sHtML

## 项目结构

```
fuvxie-article-index/
├── index.md                  # 主索引文件，包含所有文章链接与分类
├── README.md                 # 项目说明文档
├── CONTRIBUTING.md           # 外部贡献指南
├── LICENSE                   # MIT 许可证文件
├── docs/                     # 文档目录
│   ├── quick-start.md        # 快速入门指南
│   ├── maintenance.md        # 索引维护操作手册
│   └── categorization.md     # 文章分类规则说明
├── scripts/                  # 辅助脚本目录
│   ├── validate-links.sh     # 批量检查链接可达性的 shell 脚本
│   ├── generate-toc.py       # 自动生成索引目录的 Python 脚本
│   └── sort-by-id.sh         # 按文章 ID 对链接进行排序的脚本
├── assets/                   # 静态资源目录
│   └── style.css             # 索引页面的基础样式文件
├── config/                   # 配置文件目录
│   └── categories.conf       # 分类映射配置文件
└── tests/                    # 测试目录
    └── link-format.test.js   # 检查链接格式合规性的单元测试
```

## 贡献指南

1. 在提交索引更新之前，请先从主分支拉取最新代码，确保本地索引清单与上游保持一致，避免合并冲突。

2. 新增文章链接时，请严格按照 `http://www.blog.fuvxie.cn/Article/details/{ID}.sHtML` 格式填写，注意保持 `.sHtML` 后缀的大小写不变。新增条目后，运行 `scripts/sort-by-id.sh` 对清单进行排序。

3. 提交变更时，请使用清晰的提交信息格式：`[add] 添加文章 ID xxxxx` 或 `[remove] 移除失效链接 ID xxxxx`，并在提交正文中简要说明变更原因。

4. 若发现某条链接已失效（返回 404 或连接超时），请在索引中标记该条目为 `[broken]` 而非直接删除，以便后续复核。批量标记可使用 `scripts/validate-links.sh` 生成报告。

5. 所有对分类规则或项目文档的修改，需同步更新 `docs/categorization.md` 中对应的描述，确保文档与索引实际分类方式保持一致。

## 常见问题

**问：索引中的链接是否保证全部有效？**

索引仅对文章原始 URL 做聚合与分类，不承担原站可用性保证责任。fuvxie.cn 平台的历史文章可能因站点维护、内容迁移或作者删除等原因出现访问异常。建议使用 `scripts/validate-links.sh` 定期进行链接存活检测，并根据检测结果更新索引标记。

**问：发现某篇文章的 ID 与主题分类不符，应如何处理？**

分类规则以文章标题关键词与内容摘要为依据进行初步划分，可能存在个别归类不够精确的情况。若发现分类明显错误，请通过 GitHub Issues 提交分类修正建议，并附上文章标题或内容摘要作为参考依据，维护团队将在审核后进行调整。

**问：能否提交非 fuvxie.cn 域名的技术文章链接？**

本项目的定位仅限于 fuvxie.cn 平台文章索引，不收录其他域名的资源链接。如需推荐其他平台的高质量技术文章，请考虑在 Issues 中作为讨论主题提出，但不纳入当前索引清单。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:26:27
