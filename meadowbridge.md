# BlogNav 技术文章导航站

BlogNav 是一个面向开发者与技术研究人员的结构化技术文章外链聚合与导航系统。该项目并不直接托管或存储任何文章内容，而是通过人工筛选与自动化校验相结合的方式，对互联网上散布的高质量技术博文、教程、案例分析与工程实践文档进行系统化收录、分类与索引。

本项目主要解决以下问题：技术从业者在阅读与学习过程中经常面临优质内容分散、检索成本高、链接失效不可用、缺乏上下文关联等痛点。BlogNav 通过建立严谨的资源收录标准与清晰的导航层级，帮助用户以最低的时间成本找到高价值的技术参考资料，并降低因孤立链接导致的信息丢失风险。

本项目适用于需要持续跟踪特定技术领域动态的架构师、需要查阅实现方案的一线开发人员、以及希望系统化整理个人知识库的技术写作者。

## 功能概览

**结构化分类体系** 资源按技术领域、应用场景与难度层级进行多维度划分，支持用户按图索骥快速定位目标内容。

**链接存活校验机制** 系统定期对已收录的外链进行可用性检测，标记异常链接并生成报告，确保导航库的有效性。

**全文元数据提取** 对每一条收录资源自动提取标题、发布时间、作者信息及正文摘要，形成标准化的资源卡片。

**多关键字组合检索** 支持按标题关键词、文章编号、所属分类及时间范围进行精确或模糊检索，返回结果按相关度排序。

**资源引用计数与热度排序** 记录每条链接在项目内的引用次数与外部访问频次，提供热门资源排行榜。

**标签系统与关联推荐** 每条资源可关联多个自定义标签，系统根据标签重叠度自动生成相关文章推荐列表。

**外链导出与报告生成** 支持将筛选结果导出为 Markdown 表格或 CSV 格式，便于离线阅读与团队内部分享。

**访问统计与日志审计** 记录资源的访问来源与请求时间，提供基础的使用分析数据用于优化导航结构。

## 应用场景

**技术团队内部知识库建设** 团队技术负责人可将 BlogNav 作为团队知识导航的起点，将经过验证的外部优质资源集中收录，替代散落在聊天记录或邮件中的零散链接，降低新成员上手的信息获取难度。

**个人技术博客的延伸阅读体系** 独立博客作者可在每篇博文末尾引用 BlogNav 中相关的扩展阅读链接，帮助读者深入了解相关技术背景，而不必在单篇文章中容纳过长的背景介绍。

**培训机构与教育平台的课后参考资料** 技术培训讲师可将 BlogNav 按课程阶段生成定制化的资源列表，学员在课后可根据列表顺序进行延伸学习，避免因自主搜索带来的信息过载。

**开源项目文档中的外部引用管理** 开源项目维护者可在项目文档中嵌入 BlogNav 的资源入口，当需要引用外部设计决策或技术方案时，使用 BlogNav 的永久链接代替原始易失效链接，保证引用的长期可追溯性。

## 快速开始

以下指令帮助您在本地环境中快速启动 BlogNav 导航站实例。

```bash
# 克隆项目仓库至本地
git clone https://github.com/your-organization/blognav.git

# 进入项目根目录并安装依赖
cd blognav
pip install -r requirements.txt

# 初始化本地数据库并导入基础资源索引
python manage.py migrate
python manage.py loaddata initial_resources.json

# 启动开发服务器
python manage.py runserver
```

服务启动后，访问本地端口 8000 即可进入导航站首页。默认管理员账号请参阅 `docs/quickstart.md` 中的初始化说明。

## 安装要求

本项目基于 Python 3.10 及以上版本开发，以下为完整的运行环境依赖列表。

| 依赖组件 | 必需版本 | 说明 |
|---|---|---|
| Python | 3.10.0 或更高 | 核心运行环境，低于此版本将导致类型提示与异步语法错误 |
| Django | 4.2 LTS | Web 应用框架，用于路由、ORM 与模板渲染 |
| PostgreSQL | 14.0 或更高 | 生产环境推荐数据库，用于存储资源索引与用户数据 |
| Redis | 7.0 或更高 | 缓存与任务队列后端，用于链接状态检测与访问计数 |
| Celery | 5.3.0 或更高 | 异步任务调度器，配合 Redis 执行周期性链接校验 |
| django-cors-headers | 4.3.0 或更高 | 处理跨域请求，支持前端独立部署时的 API 调用 |
| Pygments | 2.15.0 或更高 | 代码语法高亮渲染，用于资源详情页中的代码片段展示 |
| lxml | 4.9.0 或更高 | HTML 解析库，用于提取外链资源的元数据与正文摘要 |
| requests | 2.31.0 或更高 | HTTP 客户端，用于执行链接可用性探测与内容抓取 |
| python-dotenv | 1.0.0 或更高 | 环境变量管理，用于区分开发与生产配置 |

## 文档导航

以下表格概括了项目文档的主要层次结构与各文档所对应的问题域，建议新用户按顺序阅读。

| 层面 | 目录文件 | 回答的问题 |
|---|---|---|
| 用户入门 | `docs/quickstart.md` | 如何最快在本地跑起服务并看到首页资源列表？ |
| 运营维护 | `docs/administration.md` | 如何添加新资源、编辑已有条目、处理失效链接？ |
| 开发指南 | `docs/development.md` | 项目的代码结构是怎样的？如何扩展新的资源解析器？ |
| 部署手册 | `docs/deployment.md` | 如何将服务部署到生产环境，包括 Nginx 配置与 HTTPS 设置？ |
| API 参考 | `docs/api_reference.md` | 前后端分离时，前端如何调用资源检索与统计接口？ |
| 数据库模型 | `docs/database_schema.md` | 资源表、标签表、访问日志表之间的关联关系是怎样的？ |

## 资源列表

本项目已收录第 186/280 批次资源共计 250 条外链，以下按原始收录顺序全部列出。所有链接均保持用户提供的原始格式，未做任何协议补全或域名修改。

### 本批次核心文章资源

http://www.blog.nzfnve.cn/Article/details/20691.sHtML
http://www.blog.nzfnve.cn/Article/details/03239.sHtML
http://www.blog.nzfnve.cn/Article/details/848448.sHtML
http://www.blog.nzfnve.cn/Article/details/010893.sHtML
http://www.blog.nzfnve.cn/Article/details/5782.sHtML
http://www.blog.nzfnve.cn/Article/details/4364854.sHtML
http://www.blog.nzfnve.cn/Article/details/7303.sHtML
http://www.blog.nzfnve.cn/Article/details/58774.sHtML
http://www.blog.nzfnve.cn/Article/details/7516430.sHtML
http://www.blog.nzfnve.cn/Article/details/5645.sHtML
http://www.blog.nzfnve.cn/Article/details/7639.sHtML
http://www.blog.nzfnve.cn/Article/details/1975.sHtML
http://www.blog.nzfnve.cn/Article/details/6423.sHtML
http://www.blog.nzfnve.cn/Article/details/50787.sHtML
http://www.blog.nzfnve.cn/Article/details/2423.sHtML
http://www.blog.nzfnve.cn/Article/details/62758.sHtML
http://www.blog.nzfnve.cn/Article/details/699563.sHtML
http://www.blog.nzfnve.cn/Article/details/131458.sHtML
http://www.blog.nzfnve.cn/Article/details/3293.sHtML
http://www.blog.nzfnve.cn/Article/details/220443.sHtML
http://www.blog.nzfnve.cn/Article/details/1388302.sHtML
http://www.blog.nzfnve.cn/Article/details/26351.sHtML
http://www.blog.nzfnve.cn/Article/details/313149.sHtML
http://www.blog.nzfnve.cn/Article/details/52188.sHtML
http://www.blog.nzfnve.cn/Article/details/58881.sHtML
http://www.blog.nzfnve.cn/Article/details/13114.sHtML
http://www.blog.nzfnve.cn/Article/details/4949.sHtML
http://www.blog.nzfnve.cn/Article/details/969118.sHtML
http://www.blog.nzfnve.cn/Article/details/50602.sHtML
http://www.blog.nzfnve.cn/Article/details/04769.sHtML
http://www.blog.nzfnve.cn/Article/details/77588.sHtML
http://www.blog.nzfnve.cn/Article/details/4272.sHtML
http://www.blog.nzfnve.cn/Article/details/80131.sHtML
http://www.blog.nzfnve.cn/Article/details/83517.sHtML
http://www.blog.nzfnve.cn/Article/details/77641.sHtML
http://www.blog.nzfnve.cn/Article/details/408060.sHtML
http://www.blog.nzfnve.cn/Article/details/647800.sHtML
http://www.blog.nzfnve.cn/Article/details/2516.sHtML
http://www.blog.nzfnve.cn/Article/details/95769.sHtML
http://www.blog.nzfnve.cn/Article/details/827888.sHtML
http://www.blog.nzfnve.cn/Article/details/4396.sHtML
http://www.blog.nzfnve.cn/Article/details/4925.sHtML
http://www.blog.nzfnve.cn/Article/details/6581.sHtML
http://www.blog.nzfnve.cn/Article/details/1436.sHtML
http://www.blog.nzfnve.cn/Article/details/95607.sHtML
http://www.blog.nzfnve.cn/Article/details/19068.sHtML
http://www.blog.nzfnve.cn/Article/details/506683.sHtML
http://www.blog.nzfnve.cn/Article/details/8529410.sHtML
http://www.blog.nzfnve.cn/Article/details/445609.sHtML
http://www.blog.nzfnve.cn/Article/details/0129025.sHtML
http://www.blog.nzfnve.cn/Article/details/9934208.sHtML
http://www.blog.nzfnve.cn/Article/details/8421.sHtML
http://www.blog.nzfnve.cn/Article/details/2874.sHtML
http://www.blog.nzfnve.cn/Article/details/65772.sHtML
http://www.blog.nzfnve.cn/Article/details/9061534.sHtML
http://www.blog.nzfnve.cn/Article/details/6358.sHtML
http://www.blog.nzfnve.cn/Article/details/079079.sHtML
http://www.blog.nzfnve.cn/Article/details/268272.sHtML
http://www.blog.nzfnve.cn/Article/details/59223.sHtML
http://www.blog.nzfnve.cn/Article/details/58021.sHtML
http://www.blog.nzfnve.cn/Article/details/66625.sHtML
http://www.blog.nzfnve.cn/Article/details/6106793.sHtML
http://www.blog.nzfnve.cn/Article/details/596937.sHtML
http://www.blog.nzfnve.cn/Article/details/8303576.sHtML
http://www.blog.nzfnve.cn/Article/details/59968.sHtML
http://www.blog.nzfnve.cn/Article/details/0764986.sHtML
http://www.blog.nzfnve.cn/Article/details/04040.sHtML
http://www.blog.nzfnve.cn/Article/details/96363.sHtML
http://www.blog.nzfnve.cn/Article/details/0412938.sHtML
http://www.blog.nzfnve.cn/Article/details/05141.sHtML
http://www.blog.nzfnve.cn/Article/details/04691.sHtML
http://www.blog.nzfnve.cn/Article/details/511640.sHtML
http://www.blog.nzfnve.cn/Article/details/7003.sHtML
http://www.blog.nzfnve.cn/Article/details/4527294.sHtML
http://www.blog.nzfnve.cn/Article/details/6279218.sHtML
http://www.blog.nzfnve.cn/Article/details/664168.sHtML
http://www.blog.nzfnve.cn/Article/details/274488.sHtML
http://www.blog.nzfnve.cn/Article/details/704572.sHtML
http://www.blog.nzfnve.cn/Article/details/7155261.sHtML
http://www.blog.nzfnve.cn/Article/details/93591.sHtML
http://www.blog.nzfnve.cn/Article/details/6488.sHtML
http://www.blog.nzfnve.cn/Article/details/139287.sHtML
http://www.blog.nzfnve.cn/Article/details/3099.sHtML
http://www.blog.nzfnve.cn/Article/details/56466.sHtML
http://www.blog.nzfnve.cn/Article/details/4472.sHtML
http://www.blog.nzfnve.cn/Article/details/95315.sHtML
http://www.blog.nzfnve.cn/Article/details/71766.sHtML
http://www.blog.nzfnve.cn/Article/details/224596.sHtML
http://www.blog.nzfnve.cn/Article/details/6244709.sHtML
http://www.blog.nzfnve.cn/Article/details/8475751.sHtML
http://www.blog.nzfnve.cn/Article/details/80064.sHtML
http://www.blog.nzfnve.cn/Article/details/1180.sHtML
http://www.blog.nzfnve.cn/Article/details/86287.sHtML
http://www.blog.nzfnve.cn/Article/details/0921.sHtML
http://www.blog.nzfnve.cn/Article/details/07308.sHtML
http://www.blog.nzfnve.cn/Article/details/1782.sHtML
http://www.blog.nzfnve.cn/Article/details/648792.sHtML
http://www.blog.nzfnve.cn/Article/details/6003190.sHtML
http://www.blog.nzfnve.cn/Article/details/3776892.sHtML
http://www.blog.nzfnve.cn/Article/details/7082.sHtML
http://www.blog.nzfnve.cn/Article/details/5596959.sHtML
http://www.blog.nzfnve.cn/Article/details/90635.sHtML
http://www.blog.nzfnve.cn/Article/details/117417.sHtML
http://www.blog.nzfnve.cn/Article/details/559747.sHtML
http://www.blog.nzfnve.cn/Article/details/36670.sHtML
http://www.blog.nzfnve.cn/Article/details/167537.sHtML
http://www.blog.nzfnve.cn/Article/details/15459.sHtML
http://www.blog.nzfnve.cn/Article/details/0920870.sHtML
http://www.blog.nzfnve.cn/Article/details/7944.sHtML
http://www.blog.nzfnve.cn/Article/details/3339.sHtML
http://www.blog.nzfnve.cn/Article/details/871430.sHtML
http://www.blog.nzfnve.cn/Article/details/759920.sHtML
http://www.blog.nzfnve.cn/Article/details/810984.sHtML
http://www.blog.nzfnve.cn/Article/details/9696.sHtML
http://www.blog.nzfnve.cn/Article/details/595620.sHtML
http://www.blog.nzfnve.cn/Article/details/87512.sHtML
http://www.blog.nzfnve.cn/Article/details/0770056.sHtML
http://www.blog.nzfnve.cn/Article/details/69137.sHtML
http://www.blog.nzfnve.cn/Article/details/8500.sHtML
http://www.blog.nzfnve.cn/Article/details/666051.sHtML
http://www.blog.nzfnve.cn/Article/details/688746.sHtML
http://www.blog.nzfnve.cn/Article/details/428837.sHtML
http://www.blog.nzfnve.cn/Article/details/070928.sHtML
http://www.blog.nzfnve.cn/Article/details/501014.sHtML
http://www.blog.nzfnve.cn/Article/details/1300033.sHtML
http://www.blog.nzfnve.cn/Article/details/3905.sHtML
http://www.blog.nzfnve.cn/Article/details/04958.sHtML
http://www.blog.nzfnve.cn/Article/details/495098.sHtML
http://www.blog.nzfnve.cn/Article/details/7490.sHtML
http://www.blog.nzfnve.cn/Article/details/252849.sHtML
http://www.blog.nzfnve.cn/Article/details/3600.sHtML
http://www.blog.nzfnve.cn/Article/details/3736110.sHtML
http://www.blog.nzfnve.cn/Article/details/52958.sHtML
http://www.blog.nzfnve.cn/Article/details/232827.sHtML
http://www.blog.nzfnve.cn/Article/details/2059.sHtML
http://www.blog.nzfnve.cn/Article/details/61442.sHtML
http://www.blog.nzfnve.cn/Article/details/1607454.sHtML
http://www.blog.nzfnve.cn/Article/details/061322.sHtML
http://www.blog.nzfnve.cn/Article/details/70660.sHtML
http://www.blog.nzfnve.cn/Article/details/145534.sHtML
http://www.blog.nzfnve.cn/Article/details/4426652.sHtML
http://www.blog.nzfnve.cn/Article/details/508235.sHtML
http://www.blog.nzfnve.cn/Article/details/3505882.sHtML
http://www.blog.nzfnve.cn/Article/details/48366.sHtML
http://www.blog.nzfnve.cn/Article/details/61540.sHtML
http://www.blog.nzfnve.cn/Article/details/10298.sHtML
http://www.blog.nzfnve.cn/Article/details/2745.sHtML
http://www.blog.nzfnve.cn/Article/details/83033.sHtML
http://www.blog.nzfnve.cn/Article/details/552259.sHtML
http://www.blog.nzfnve.cn/Article/details/55997.sHtML
http://www.blog.nzfnve.cn/Article/details/0681.sHtML
http://www.blog.nzfnve.cn/Article/details/948740.sHtML
http://www.blog.nzfnve.cn/Article/details/333237.sHtML
http://www.blog.nzfnve.cn/Article/details/64380.sHtML
http://www.blog.nzfnve.cn/Article/details/7660.sHtML
http://www.blog.nzfnve.cn/Article/details/3717.sHtML
http://www.blog.nzfnve.cn/Article/details/210110.sHtML
http://www.blog.nzfnve.cn/Article/details/130006.sHtML
http://www.blog.nzfnve.cn/Article/details/6778.sHtML
http://www.blog.nzfnve.cn/Article/details/74032.sHtML
http://www.blog.nzfnve.cn/Article/details/3455.sHtML
http://www.blog.nzfnve.cn/Article/details/2403.sHtML
http://www.blog.nzfnve.cn/Article/details/755353.sHtML
http://www.blog.nzfnve.cn/Article/details/85254.sHtML
http://www.blog.nzfnve.cn/Article/details/695556.sHtML
http://www.blog.nzfnve.cn/Article/details/5905389.sHtML
http://www.blog.nzfnve.cn/Article/details/2463454.sHtML
http://www.blog.nzfnve.cn/Article/details/262036.sHtML
http://www.blog.nzfnve.cn/Article/details/31906.sHtML
http://www.blog.nzfnve.cn/Article/details/8656.sHtML
http://www.blog.nzfnve.cn/Article/details/40118.sHtML
http://www.blog.nzfnve.cn/Article/details/428707.sHtML
http://www.blog.nzfnve.cn/Article/details/685647.sHtML
http://www.blog.nzfnve.cn/Article/details/3850427.sHtML
http://www.blog.nzfnve.cn/Article/details/31819.sHtML
http://www.blog.nzfnve.cn/Article/details/1897941.sHtML
http://www.blog.nzfnve.cn/Article/details/7795027.sHtML
http://www.blog.nzfnve.cn/Article/details/2332763.sHtML
http://www.blog.nzfnve.cn/Article/details/0197121.sHtML
http://www.blog.nzfnve.cn/Article/details/959783.sHtML
http://www.blog.nzfnve.cn/Article/details/05804.sHtML
http://www.blog.nzfnve.cn/Article/details/4623.sHtML
http://www.blog.nzfnve.cn/Article/details/9385.sHtML
http://www.blog.nzfnve.cn/Article/details/9409048.sHtML
http://www.blog.nzfnve.cn/Article/details/3270152.sHtML
http://www.blog.nzfnve.cn/Article/details/75617.sHtML
http://www.blog.nzfnve.cn/Article/details/22846.sHtML
http://www.blog.nzfnve.cn/Article/details/9887967.sHtML
http://www.blog.nzfnve.cn/Article/details/329747.sHtML
http://www.blog.nzfnve.cn/Article/details/064928.sHtML
http://www.blog.nzfnve.cn/Article/details/236450.sHtML
http://www.blog.nzfnve.cn/Article/details/03849.sHtML
http://www.blog.nzfnve.cn/Article/details/6201.sHtML
http://www.blog.nzfnve.cn/Article/details/662263.sHtML
http://www.blog.nzfnve.cn/Article/details/5507546.sHtML
http://www.blog.nzfnve.cn/Article/details/6137571.sHtML
http://www.blog.nzfnve.cn/Article/details/8730091.sHtML
http://www.blog.nzfnve.cn/Article/details/593427.sHtML
http://www.blog.nzfnve.cn/Article/details/7662479.sHtML
http://www.blog.nzfnve.cn/Article/details/24344.sHtML
http://www.blog.nzfnve.cn/Article/details/1411027.sHtML
http://www.blog.nzfnve.cn/Article/details/843280.sHtML
http://www.blog.nzfnve.cn/Article/details/75709.sHtML
http://www.blog.nzfnve.cn/Article/details/2793325.sHtML
http://www.blog.nzfnve.cn/Article/details/6348566.sHtML
http://www.blog.nzfnve.cn/Article/details/365951.sHtML
http://www.blog.nzfnve.cn/Article/details/150230.sHtML
http://www.blog.nzfnve.cn/Article/details/13323.sHtML
http://www.blog.nzfnve.cn/Article/details/2438939.sHtML
http://www.blog.nzfnve.cn/Article/details/28698.sHtML
http://www.blog.nzfnve.cn/Article/details/4171642.sHtML
http://www.blog.nzfnve.cn/Article/details/72424.sHtML
http://www.blog.nzfnve.cn/Article/details/0129.sHtML
http://www.blog.nzfnve.cn/Article/details/7162774.sHtML
http://www.blog.nzfnve.cn/Article/details/3159609.sHtML
http://www.blog.nzfnve.cn/Article/details/001870.sHtML
http://www.blog.nzfnve.cn/Article/details/6204409.sHtML
http://www.blog.nzfnve.cn/Article/details/8545589.sHtML
http://www.blog.nzfnve.cn/Article/details/62166.sHtML
http://www.blog.nzfnve.cn/Article/details/48372.sHtML
http://www.blog.nzfnve.cn/Article/details/910366.sHtML
http://www.blog.nzfnve.cn/Article/details/307519.sHtML
http://www.blog.nzfnve.cn/Article/details/7747540.sHtML
http://www.blog.nzfnve.cn/Article/details/239634.sHtML
http://www.blog.nzfnve.cn/Article/details/4450.sHtML
http://www.blog.nzfnve.cn/Article/details/804632.sHtML
http://www.blog.nzfnve.cn/Article/details/92053.sHtML
http://www.blog.nzfnve.cn/Article/details/7952.sHtML
http://www.blog.nzfnve.cn/Article/details/9040158.sHtML
http://www.blog.nzfnve.cn/Article/details/51357.sHtML
http://www.blog.nzfnve.cn/Article/details/534373.sHtML
http://www.blog.nzfnve.cn/Article/details/88717.sHtML
http://www.blog.nzfnve.cn/Article/details/7377.sHtML
http://www.blog.nzfnve.cn/Article/details/960990.sHtML
http://www.blog.nzfnve.cn/Article/details/650468.sHtML
http://www.blog.nzfnve.cn/Article/details/282533.sHtML
http://www.blog.nzfnve.cn/Article/details/634485.sHtML
http://www.blog.nzfnve.cn/Article/details/0203317.sHtML
http://www.blog.nzfnve.cn/Article/details/7113.sHtML
http://www.blog.nzfnve.cn/Article/details/7611773.sHtML
http://www.blog.nzfnve.cn/Article/details/0817241.sHtML
http://www.blog.nzfnve.cn/Article/details/51239.sHtML
http://www.blog.nzfnve.cn/Article/details/301019.sHtML
http://www.blog.nzfnve.cn/Article/details/83253.sHtML
http://www.blog.nzfnve.cn/Article/details/357437.sHtML
http://www.blog.nzfnve.cn/Article/details/2694.sHtML
http://www.blog.nzfnve.cn/Article/details/32041.sHtML
http://www.blog.nzfnve.cn/Article/details/4551.sHtML
http://www.blog.nzfnve.cn/Article/details/27397.sHtML
http://www.blog.nzfnve.cn/Article/details/54535.sHtML

## 项目结构

以下为 BlogNav 项目核心目录与文件组织方式，标注了各模块的主要职责。

```
blognav/
├── manage.py                     # Django 项目管理入口，执行 migrate/runserver 等命令
├── requirements.txt              # Python 依赖清单，包含运行时与开发环境所需包
├── .env.example                  # 环境变量模板，包含数据库连接串与 Redis 地址
├── .gitignore                    # 版本控制忽略文件列表，排除缓存与本地配置
│
├── blognav/                      # 项目主配置目录
│   ├── __init__.py
│   ├── settings.py               # 基础设置，包含应用注册、中间件、模板与国际化配置
│   ├── settings_dev.py           # 开发环境专有配置，启用调试与本地数据库
│   ├── settings_prod.py          # 生产环境配置，关闭调试并配置日志级别
│   ├── urls.py                   # 根路由分发，将请求映射至各子应用
│   └── asgi.py / wsgi.py         # 异步与同步网关接口，用于部署服务器对接
│
├── apps/                         # 所有功能应用存放目录
│   ├── resources/                # 资源管理核心应用
│   │   ├── models.py             # Resource, Tag, Category 等数据模型定义
│   │   ├── views.py              # 资源列表、详情、检索、导出等视图逻辑
│   │   ├── serializers.py        # RESTful API 序列化器，用于前后端数据交换
│   │   ├── admin.py              # Django 后台管理界面定制，用于运营人员操作
│   │   └── urls.py               # 资源相关路由，包含 /api/resources 与 /export
│   ├── crawler/                  # 外链元数据抓取与解析模块
│   │   ├── fetcher.py            # 基于 requests 的 HTTP 请求封装与重试逻辑
│   │   ├── parser.py             # 使用 lxml 提取标题、正文与发布时间
│   │   └── checksum.py           # 内容指纹计算，用于检测页面更新
│   ├── tasks/                    # Celery 异步任务定义
│   │   ├── periodic.py           # 定时任务：每日凌晨执行全量链接可用性检测
│   │   └── manual.py             # 手动触发任务：单条资源刷新与重新解析
│   ├── users/                    # 用户认证与权限管理
│   │   ├── models.py             # 扩展用户模型，包含 API 访问令牌
│   │   └── permissions.py        # 基于角色的访问控制，区分普通用户与管理员
│   └── stats/                    # 访问统计与日志分析
│       ├── middleware.py         # 请求拦截中间件，记录访问路径与来源 IP
│       └── aggregator.py         # 按日/周/月聚合访问数据，生成趋势报表
│
├── templates/                    # Django 模板文件，用于服务端渲染页面
│   ├── base.html                 # 基础骨架，包含公共导航与页脚
│   └── resources/                # 资源相关页面模板，如列表、详情与搜索页
│
├── static/                       # 静态资源文件
│   ├── css/                      # 基于 Bootstrap 5 自定义样式表
│   ├── js/                       # 前端交互脚本，包含即时搜索与标签过滤
│   └── images/                   # Logo 与默认占位图
│
├── docs/                         # 项目文档，与前述文档导航表格对应
│   ├── quickstart.md
│   ├── administration.md
│   ├── development.md
│   ├── deployment.md
│   ├── api_reference.md
│   └── database_schema.md
│
├── scripts/                      # 运维与数据迁移辅助脚本
│   ├── import_resources.py       # 批量导入本批次 250 条资源链接至数据库
│   ├── export_markdown.py        # 将数据库内容导出为 Markdown 资源列表
│   └── health_check.sh           # 系统健康检查脚本，验证服务与数据库连通性
│
└── tests/                        # 单元测试与集成测试
    ├── test_models.py            # 数据模型测试用例
    ├── test_api.py               # API 接口返回状态与数据正确性测试
    └── test_crawler.py           # 抓取器与解析器在异常页面场景下的鲁棒性测试
```

## 贡献指南

我们欢迎并鼓励社区开发者参与 BlogNav 的改进与扩展。请按照以下流程提交贡献。

第一步：提交 Issue 或发起讨论。在开始任何代码修改之前，请先在 GitHub Issues 中描述您希望解决的问题或新增的功能，等待项目维护者的确认以避免重复劳动或方向偏离。

第二步：Fork 仓库并创建特性分支。将本项目 Fork 至您的个人账户，并在本地切换到新分支，分支命名格式为 `feature/简述改动` 或 `fix/简述问题`，例如 `feature/add-pdf-export`。

第三步：编写代码并添加测试。确保您的代码符合 PEP 8 编码规范，并为新增功能或修复的逻辑编写对应的单元测试，保证测试覆盖率达到 85% 以上。

第四步：提交 Pull Request。在 PR 描述中清晰关联对应的 Issue 编号，列出改动摘要与影响范围，并确保所有 CI 检查通过。

第五步：代码审查与合并。项目维护者将在 3 个工作日内进行审查，可能需要您根据反馈进行修改。合并后您的提交将进入主分支并随下一个版本发布。

## 常见问题

**问：部分外链无法访问，页面返回 404 或超时错误，该如何处理？**

答：BlogNav 系统每天凌晨自动执行全量链接健康检查，若某条链接连续三次检测失败，该资源将被标记为“异常”状态并在前台界面以灰色标识。用户可点击资源卡片上的“报告失效”按钮主动提交异常反馈，运营人员会在收到反馈后人工核实并决定是否移除或替换该条目。对于个人维护的实例，您也可以手动运行 `python manage.py check_links --force` 命令立即触发重新检测。

**问：如何将本项目部署到内网环境，不连接外网也能正常使用？**

答：BlogNav 的核心导航功能完全依赖本地数据库中的资源索引，因此在内网部署时无需访问外网即可正常检索与浏览。但需要注意两点：其一，链接健康检查功能需要外网访问能力来探测目标站点，若内网受限，请通过 `settings.py` 中的 `LINK_CHECK_ENABLED = False` 关闭该功能；其二，首次部署时需要将所有资源数据导入本地数据库，导入过程不依赖外网，您只需确保 `fixtures/initial_resources.json` 文件完整即可。

**问：我想在导航站中收录自己的博客文章，应该如何操作？**

答：您可以通过两种方式添加自定义资源。第一种方式是通过 Django 后台管理界面，在登录管理员账户后进入“资源管理”模块，点击“添加”并填写标题、原始链接、分类与标签信息，提交后立即生效。第二种方式是通过命令行工具，将待添加链接整理为 CSV 文件并执行 `python manage.py import_resources --csv your_file.csv` 进行批量导入。请注意，添加外部链接时请遵守目标网站的 robots.txt 规定，并在合理频率内抓取元数据。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:28:28
