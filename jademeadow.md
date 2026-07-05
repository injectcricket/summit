# TechRef Navigator

TechRef Navigator 是一个面向软件工程师、技术架构师和技术文档撰写者的结构化技术资源导航项目。本项目旨在解决技术资料分散、优质中文技术文章难以检索和归类的问题，通过对特定技术博客站点的文章进行系统性梳理和索引，为开发者提供一条清晰的技术学习与参考资料路径。

本项目聚焦于收录和分类来自 puhvjy 技术博客的精选文章，该博客站覆盖了后端开发、系统架构、编程语言原理、数据库调优、算法设计、工程实践等多个技术领域。TechRef Navigator 不是一个爬虫项目或自动化采集工具，而是一个经过人工初步筛选和主题归类的资源索引库。项目维护者会根据文章内容的技术深度、实用价值和覆盖面，将其划分为不同的技术专题，并以 Markdown 表格和目录树的形式提供清晰的导航结构，方便开发者按图索骥，快速定位到所需的技术讨论。

项目定位为技术团队的知识库外挂和个人的技术成长路线图参考。无论是准备技术面试、解决生产环境中的疑难杂症，还是系统性地学习某个技术栈的底层原理，TechRef Navigator 都能提供经过整理的、可直接访问的原始资料入口。

## 功能概览

**结构化资源索引**：提供按技术领域和文章ID双重维度的资源列表，所有链接均指向原始博文，不经过任何第三方跳转或代理。

**快速本地检索**：项目根目录维护一份完整的资源映射表，用户可通过 grep 或内置脚本根据文章 ID 或关键字快速定位目标资源。

**轻量级部署**：项目本身是纯静态 Markdown 文档集合，无需数据库或后端服务即可在本地阅读，亦可托管至任意静态站点服务。

**版本化更新记录**：每次资源列表的增删改均通过 Git 提交记录体现，用户可追溯资源库的变更历史。

**多维度文档导航**：提供按技术层面（基础理论、工程实践、性能调优、运维监控）划分的文档导航表格，帮助用户根据当前面临的问题类型选择阅读材料。

**离线阅读支持**：用户可通过脚本将 Markdown 文档转换为 PDF 或离线网页包，适用于网络受限的开发环境。

## 应用场景

技术团队内部知识库建设：技术负责人可以将 TechRef Navigator 作为团队新人培训的补充阅读清单。新入职的开发者在熟悉项目业务代码之前，可以通过本导航系统阅读相关技术领域的博文，快速建立对技术栈的认知框架。

技术面试准备：求职者在准备后端开发或系统设计岗位面试时，可以利用本项目的分类导航，集中阅读分布式系统、缓存设计、消息队列等专题的文章。项目提供的结构化列表比搜索引擎的零散结果更具针对性。

生产环境问题排查：当运维或开发人员遇到线上服务性能抖动时，可以通过本项目的性能调优章节快速定位相关案例文章。虽然项目不直接提供解决方案，但索引的文章往往包含问题分析思路和诊断工具的使用方法。

技术文章写作参考：技术博主或文档撰写者在构思新文章时，可以通过本项目的资源列表了解已有内容的覆盖范围，避免重复造轮子，同时也可以参考列表中的文章结构来组织自己的技术论述。

## 快速开始

以下步骤帮助您在本地完成 TechRef Navigator 的克隆、环境配置和初始运行。

```bash
# 克隆项目仓库
git clone https://github.com/techref-navigator/techref-navigator.git
cd techref-navigator

# 安装依赖（项目依赖 Python 3 和 Markdown 渲染库）
pip install -r requirements.txt

# 执行资源映射表构建脚本，生成最新的索引文件
python build_index.py --input ./resources --output ./INDEX.md
```

## 安装要求

| 依赖 | 必需 | 说明 |
|---|---|---|
| Python 3.8 及以上 | 是 | 用于运行资源索引构建脚本和本地预览服务 |
| pip 21.0 及以上 | 是 | Python 包管理工具，用于安装项目依赖 |
| Markdown 库 3.4 及以上 | 是 | 用于渲染和验证 Markdown 文档格式 |
| PyYAML 6.0 及以上 | 是 | 用于解析资源分类配置文件 |
| Git 2.25 及以上 | 是 | 用于克隆仓库和管理版本更新 |
| make 4.2 及以上 | 否 | 可选，用于自动化执行常见任务（如构建、清理） |
| nodejs 14.x 及以上 | 否 | 可选，仅当需要使用前端预览工具时 |

## 文档导航

| 层面 | 目录 | 回答的问题 |
|---|---|---|
| 基础理论 | /docs/foundation/ | 编程语言特性、数据结构设计、网络协议原理等基础知识点在哪里查阅？ |
| 工程实践 | /docs/engineering/ | 如何设计高可用架构、如何处理分布式事务、如何进行代码重构？ |
| 性能调优 | /docs/performance/ | JVM 调优参数如何设置、数据库慢查询如何分析、缓存命中率如何提升？ |
| 运维监控 | /docs/operations/ | 服务日志如何规范管理、微服务链路如何追踪、容器化部署有哪些注意事项？ |
| 综合案例 | /docs/case-studies/ | 真实业务场景中如何组合运用多种技术解决复杂问题？ |

## 资源列表

### 全部资源索引（按收录顺序）

http://www.blog.puhvjy.cn/Article/details/2925279.sHtML
http://www.blog.puhvjy.cn/Article/details/4552.sHtML
http://www.blog.puhvjy.cn/Article/details/605555.sHtML
http://www.blog.puhvjy.cn/Article/details/3885408.sHtML
http://www.blog.puhvjy.cn/Article/details/8086.sHtML
http://www.blog.puhvjy.cn/Article/details/856397.sHtML
http://www.blog.puhvjy.cn/Article/details/4646054.sHtML
http://www.blog.puhvjy.cn/Article/details/249176.sHtML
http://www.blog.puhvjy.cn/Article/details/7480528.sHtML
http://www.blog.puhvjy.cn/Article/details/7136190.sHtML
http://www.blog.puhvjy.cn/Article/details/5616144.sHtML
http://www.blog.puhvjy.cn/Article/details/2945564.sHtML
http://www.blog.puhvjy.cn/Article/details/9468266.sHtML
http://www.blog.puhvjy.cn/Article/details/7372316.sHtML
http://www.blog.puhvjy.cn/Article/details/771266.sHtML
http://www.blog.puhvjy.cn/Article/details/94587.sHtML
http://www.blog.puhvjy.cn/Article/details/13112.sHtML
http://www.blog.puhvjy.cn/Article/details/983296.sHtML
http://www.blog.puhvjy.cn/Article/details/0128986.sHtML
http://www.blog.puhvjy.cn/Article/details/8990231.sHtML
http://www.blog.puhvjy.cn/Article/details/92677.sHtML
http://www.blog.puhvjy.cn/Article/details/8104.sHtML
http://www.blog.puhvjy.cn/Article/details/2582.sHtML
http://www.blog.puhvjy.cn/Article/details/84524.sHtML
http://www.blog.puhvjy.cn/Article/details/9871208.sHtML
http://www.blog.puhvjy.cn/Article/details/40674.sHtML
http://www.blog.puhvjy.cn/Article/details/13139.sHtML
http://www.blog.puhvjy.cn/Article/details/932959.sHtML
http://www.blog.puhvjy.cn/Article/details/42589.sHtML
http://www.blog.puhvjy.cn/Article/details/2200103.sHtML
http://www.blog.puhvjy.cn/Article/details/2667499.sHtML
http://www.blog.puhvjy.cn/Article/details/19418.sHtML
http://www.blog.puhvjy.cn/Article/details/100534.sHtML
http://www.blog.puhvjy.cn/Article/details/105967.sHtML
http://www.blog.puhvjy.cn/Article/details/5242.sHtML
http://www.blog.puhvjy.cn/Article/details/6294745.sHtML
http://www.blog.puhvjy.cn/Article/details/6417752.sHtML
http://www.blog.puhvjy.cn/Article/details/93437.sHtML
http://www.blog.puhvjy.cn/Article/details/2525448.sHtML
http://www.blog.puhvjy.cn/Article/details/20309.sHtML
http://www.blog.puhvjy.cn/Article/details/7893774.sHtML
http://www.blog.puhvjy.cn/Article/details/19290.sHtML
http://www.blog.puhvjy.cn/Article/details/9372.sHtML
http://www.blog.puhvjy.cn/Article/details/6026.sHtML
http://www.blog.puhvjy.cn/Article/details/9672475.sHtML
http://www.blog.puhvjy.cn/Article/details/86922.sHtML
http://www.blog.puhvjy.cn/Article/details/4461214.sHtML
http://www.blog.puhvjy.cn/Article/details/69341.sHtML
http://www.blog.puhvjy.cn/Article/details/7002.sHtML
http://www.blog.puhvjy.cn/Article/details/301567.sHtML
http://www.blog.puhvjy.cn/Article/details/0118.sHtML
http://www.blog.puhvjy.cn/Article/details/979283.sHtML
http://www.blog.puhvjy.cn/Article/details/658789.sHtML
http://www.blog.puhvjy.cn/Article/details/6272483.sHtML
http://www.blog.puhvjy.cn/Article/details/36155.sHtML
http://www.blog.puhvjy.cn/Article/details/05515.sHtML
http://www.blog.puhvjy.cn/Article/details/49111.sHtML
http://www.blog.puhvjy.cn/Article/details/58038.sHtML
http://www.blog.puhvjy.cn/Article/details/2679.sHtML
http://www.blog.puhvjy.cn/Article/details/6886065.sHtML
http://www.blog.puhvjy.cn/Article/details/711917.sHtML
http://www.blog.puhvjy.cn/Article/details/557538.sHtML
http://www.blog.puhvjy.cn/Article/details/51459.sHtML
http://www.blog.puhvjy.cn/Article/details/9741007.sHtML
http://www.blog.puhvjy.cn/Article/details/706286.sHtML
http://www.blog.puhvjy.cn/Article/details/351068.sHtML
http://www.blog.puhvjy.cn/Article/details/917472.sHtML
http://www.blog.puhvjy.cn/Article/details/4246.sHtML
http://www.blog.puhvjy.cn/Article/details/121051.sHtML
http://www.blog.puhvjy.cn/Article/details/409716.sHtML
http://www.blog.puhvjy.cn/Article/details/4657942.sHtML
http://www.blog.puhvjy.cn/Article/details/591550.sHtML
http://www.blog.puhvjy.cn/Article/details/4192685.sHtML
http://www.blog.puhvjy.cn/Article/details/43532.sHtML
http://www.blog.puhvjy.cn/Article/details/3669121.sHtML
http://www.blog.puhvjy.cn/Article/details/457727.sHtML
http://www.blog.puhvjy.cn/Article/details/1832.sHtML
http://www.blog.puhvjy.cn/Article/details/2507754.sHtML
http://www.blog.puhvjy.cn/Article/details/3329.sHtML
http://www.blog.puhvjy.cn/Article/details/60892.sHtML
http://www.blog.puhvjy.cn/Article/details/880209.sHtML
http://www.blog.puhvjy.cn/Article/details/5335391.sHtML
http://www.blog.puhvjy.cn/Article/details/949045.sHtML
http://www.blog.puhvjy.cn/Article/details/928273.sHtML
http://www.blog.puhvjy.cn/Article/details/0413.sHtML
http://www.blog.puhvjy.cn/Article/details/2291940.sHtML
http://www.blog.puhvjy.cn/Article/details/145274.sHtML
http://www.blog.puhvjy.cn/Article/details/422316.sHtML
http://www.blog.puhvjy.cn/Article/details/672119.sHtML
http://www.blog.puhvjy.cn/Article/details/9843777.sHtML
http://www.blog.puhvjy.cn/Article/details/35330.sHtML
http://www.blog.puhvjy.cn/Article/details/0268482.sHtML
http://www.blog.puhvjy.cn/Article/details/17549.sHtML
http://www.blog.puhvjy.cn/Article/details/3523131.sHtML
http://www.blog.puhvjy.cn/Article/details/641238.sHtML
http://www.blog.puhvjy.cn/Article/details/6170289.sHtML
http://www.blog.puhvjy.cn/Article/details/31582.sHtML
http://www.blog.puhvjy.cn/Article/details/7343437.sHtML
http://www.blog.puhvjy.cn/Article/details/078518.sHtML
http://www.blog.puhvjy.cn/Article/details/8234581.sHtML
http://www.blog.puhvjy.cn/Article/details/485585.sHtML
http://www.blog.puhvjy.cn/Article/details/34589.sHtML
http://www.blog.puhvjy.cn/Article/details/768787.sHtML
http://www.blog.puhvjy.cn/Article/details/2250.sHtML
http://www.blog.puhvjy.cn/Article/details/3386841.sHtML
http://www.blog.puhvjy.cn/Article/details/9188814.sHtML
http://www.blog.puhvjy.cn/Article/details/3286.sHtML
http://www.blog.puhvjy.cn/Article/details/2648712.sHtML
http://www.blog.puhvjy.cn/Article/details/88992.sHtML
http://www.blog.puhvjy.cn/Article/details/4235.sHtML
http://www.blog.puhvjy.cn/Article/details/5214498.sHtML
http://www.blog.puhvjy.cn/Article/details/917877.sHtML
http://www.blog.puhvjy.cn/Article/details/542155.sHtML
http://www.blog.puhvjy.cn/Article/details/6571001.sHtML
http://www.blog.puhvjy.cn/Article/details/0521205.sHtML
http://www.blog.puhvjy.cn/Article/details/774913.sHtML
http://www.blog.puhvjy.cn/Article/details/46960.sHtML
http://www.blog.puhvjy.cn/Article/details/2531113.sHtML
http://www.blog.puhvjy.cn/Article/details/5872.sHtML
http://www.blog.puhvjy.cn/Article/details/5505.sHtML
http://www.blog.puhvjy.cn/Article/details/8595.sHtML
http://www.blog.puhvjy.cn/Article/details/200061.sHtML
http://www.blog.puhvjy.cn/Article/details/47105.sHtML
http://www.blog.puhvjy.cn/Article/details/3933.sHtML
http://www.blog.puhvjy.cn/Article/details/132303.sHtML
http://www.blog.puhvjy.cn/Article/details/5311982.sHtML
http://www.blog.puhvjy.cn/Article/details/28012.sHtML
http://www.blog.puhvjy.cn/Article/details/7248.sHtML
http://www.blog.puhvjy.cn/Article/details/010045.sHtML
http://www.blog.puhvjy.cn/Article/details/84870.sHtML
http://www.blog.puhvjy.cn/Article/details/55397.sHtML
http://www.blog.puhvjy.cn/Article/details/2099256.sHtML
http://www.blog.puhvjy.cn/Article/details/08816.sHtML
http://www.blog.puhvjy.cn/Article/details/3919031.sHtML
http://www.blog.puhvjy.cn/Article/details/69809.sHtML
http://www.blog.puhvjy.cn/Article/details/685730.sHtML
http://www.blog.puhvjy.cn/Article/details/787388.sHtML
http://www.blog.puhvjy.cn/Article/details/82160.sHtML
http://www.blog.puhvjy.cn/Article/details/39561.sHtML
http://www.blog.puhvjy.cn/Article/details/044454.sHtML
http://www.blog.puhvjy.cn/Article/details/9751767.sHtML
http://www.blog.puhvjy.cn/Article/details/94859.sHtML
http://www.blog.puhvjy.cn/Article/details/0254777.sHtML
http://www.blog.puhvjy.cn/Article/details/5628315.sHtML
http://www.blog.puhvjy.cn/Article/details/6670.sHtML
http://www.blog.puhvjy.cn/Article/details/6470818.sHtML
http://www.blog.puhvjy.cn/Article/details/4845.sHtML
http://www.blog.puhvjy.cn/Article/details/417456.sHtML
http://www.blog.puhvjy.cn/Article/details/9053.sHtML
http://www.blog.puhvjy.cn/Article/details/3869518.sHtML
http://www.blog.puhvjy.cn/Article/details/5598042.sHtML
http://www.blog.puhvjy.cn/Article/details/894732.sHtML
http://www.blog.puhvjy.cn/Article/details/098054.sHtML
http://www.blog.puhvjy.cn/Article/details/63320.sHtML
http://www.blog.puhvjy.cn/Article/details/7504840.sHtML
http://www.blog.puhvjy.cn/Article/details/7134964.sHtML
http://www.blog.puhvjy.cn/Article/details/1725997.sHtML
http://www.blog.puhvjy.cn/Article/details/0633679.sHtML
http://www.blog.puhvjy.cn/Article/details/060165.sHtML
http://www.blog.puhvjy.cn/Article/details/4532.sHtML
http://www.blog.puhvjy.cn/Article/details/5494.sHtML
http://www.blog.puhvjy.cn/Article/details/0523.sHtML
http://www.blog.puhvjy.cn/Article/details/91014.sHtML
http://www.blog.puhvjy.cn/Article/details/6022920.sHtML
http://www.blog.puhvjy.cn/Article/details/8955.sHtML
http://www.blog.puhvjy.cn/Article/details/24722.sHtML
http://www.blog.puhvjy.cn/Article/details/97811.sHtML
http://www.blog.puhvjy.cn/Article/details/3936683.sHtML
http://www.blog.puhvjy.cn/Article/details/617199.sHtML
http://www.blog.puhvjy.cn/Article/details/3529.sHtML
http://www.blog.puhvjy.cn/Article/details/265075.sHtML
http://www.blog.puhvjy.cn/Article/details/5550.sHtML
http://www.blog.puhvjy.cn/Article/details/5855843.sHtML
http://www.blog.puhvjy.cn/Article/details/6867253.sHtML
http://www.blog.puhvjy.cn/Article/details/230063.sHtML
http://www.blog.puhvjy.cn/Article/details/5514764.sHtML
http://www.blog.puhvjy.cn/Article/details/96848.sHtML
http://www.blog.puhvjy.cn/Article/details/25100.sHtML
http://www.blog.puhvjy.cn/Article/details/74516.sHtML
http://www.blog.puhvjy.cn/Article/details/1198082.sHtML
http://www.blog.puhvjy.cn/Article/details/5509728.sHtML
http://www.blog.puhvjy.cn/Article/details/9356.sHtML
http://www.blog.puhvjy.cn/Article/details/72856.sHtML
http://www.blog.puhvjy.cn/Article/details/56443.sHtML
http://www.blog.puhvjy.cn/Article/details/7418.sHtML
http://www.blog.puhvjy.cn/Article/details/31509.sHtML
http://www.blog.puhvjy.cn/Article/details/69887.sHtML
http://www.blog.puhvjy.cn/Article/details/0974745.sHtML
http://www.blog.puhvjy.cn/Article/details/361753.sHtML
http://www.blog.puhvjy.cn/Article/details/31069.sHtML
http://www.blog.puhvjy.cn/Article/details/12250.sHtML
http://www.blog.puhvjy.cn/Article/details/6213.sHtML
http://www.blog.puhvjy.cn/Article/details/9557747.sHtML
http://www.blog.puhvjy.cn/Article/details/5374875.sHtML
http://www.blog.puhvjy.cn/Article/details/0927.sHtML
http://www.blog.puhvjy.cn/Article/details/558140.sHtML
http://www.blog.puhvjy.cn/Article/details/0535.sHtML
http://www.blog.puhvjy.cn/Article/details/269729.sHtML
http://www.blog.puhvjy.cn/Article/details/3012.sHtML
http://www.blog.puhvjy.cn/Article/details/3803.sHtML
http://www.blog.puhvjy.cn/Article/details/13803.sHtML
http://www.blog.puhvjy.cn/Article/details/61388.sHtML
http://www.blog.puhvjy.cn/Article/details/3791.sHtML
http://www.blog.puhvjy.cn/Article/details/845331.sHtML
http://www.blog.puhvjy.cn/Article/details/19882.sHtML
http://www.blog.puhvjy.cn/Article/details/3421.sHtML
http://www.blog.puhvjy.cn/Article/details/3643.sHtML
http://www.blog.puhvjy.cn/Article/details/193003.sHtML
http://www.blog.puhvjy.cn/Article/details/07053.sHtML
http://www.blog.puhvjy.cn/Article/details/05191.sHtML
http://www.blog.puhvjy.cn/Article/details/2599237.sHtML
http://www.blog.puhvjy.cn/Article/details/42801.sHtML
http://www.blog.puhvjy.cn/Article/details/736468.sHtML
http://www.blog.puhvjy.cn/Article/details/7480.sHtML
http://www.blog.puhvjy.cn/Article/details/5669.sHtML
http://www.blog.puhvjy.cn/Article/details/953127.sHtML
http://www.blog.puhvjy.cn/Article/details/940149.sHtML
http://www.blog.puhvjy.cn/Article/details/3197356.sHtML
http://www.blog.puhvjy.cn/Article/details/9217.sHtML
http://www.blog.puhvjy.cn/Article/details/8792455.sHtML
http://www.blog.puhvjy.cn/Article/details/812179.sHtML
http://www.blog.puhvjy.cn/Article/details/0057.sHtML
http://www.blog.puhvjy.cn/Article/details/0201.sHtML
http://www.blog.puhvjy.cn/Article/details/991242.sHtML
http://www.blog.puhvjy.cn/Article/details/2301.sHtML
http://www.blog.puhvjy.cn/Article/details/4234.sHtML
http://www.blog.puhvjy.cn/Article/details/0399.sHtML
http://www.blog.puhvjy.cn/Article/details/39204.sHtML
http://www.blog.puhvjy.cn/Article/details/71519.sHtML
http://www.blog.puhvjy.cn/Article/details/63691.sHtML
http://www.blog.puhvjy.cn/Article/details/82534.sHtML
http://www.blog.puhvjy.cn/Article/details/223906.sHtML
http://www.blog.puhvjy.cn/Article/details/3146.sHtML
http://www.blog.puhvjy.cn/Article/details/48825.sHtML
http://www.blog.puhvjy.cn/Article/details/6220758.sHtML
http://www.blog.puhvjy.cn/Article/details/48188.sHtML
http://www.blog.puhvjy.cn/Article/details/11687.sHtML
http://www.blog.puhvjy.cn/Article/details/6146725.sHtML
http://www.blog.puhvjy.cn/Article/details/796277.sHtML
http://www.blog.puhvjy.cn/Article/details/639973.sHtML
http://www.blog.puhvjy.cn/Article/details/75616.sHtML
http://www.blog.puhvjy.cn/Article/details/9841977.sHtML
http://www.blog.puhvjy.cn/Article/details/2794126.sHtML
http://www.blog.puhvjy.cn/Article/details/660948.sHtML
http://www.blog.puhvjy.cn/Article/details/98988.sHtML
http://www.blog.puhvjy.cn/Article/details/41669.sHtML
http://www.blog.puhvjy.cn/Article/details/92385.sHtML
http://www.blog.puhvjy.cn/Article/details/6645099.sHtML
http://www.blog.puhvjy.cn/Article/details/09070.sHtML
http://www.blog.puhvjy.cn/Article/details/475087.sHtML

## 项目结构

```
techref-navigator/
├── README.md                         # 项目概述、快速开始和使用说明
├── INDEX.md                          # 全量资源索引表，由构建脚本自动生成
├── requirements.txt                  # Python 依赖声明文件
├── build_index.py                    # 资源索引构建脚本，扫描 resources 目录生成 INDEX.md
├── .gitignore                        # Git 忽略规则，排除临时文件和本地配置
├── docs/                             # 文档导航主目录
│   ├── foundation/                   # 基础理论层面文档
│   │   ├── network.md                # 网络协议与通信原理相关资源导航
│   │   └── language.md               # 编程语言特性与编译原理相关资源导航
│   ├── engineering/                  # 工程实践层面文档
│   │   ├── architecture.md           # 系统架构设计模式与微服务实践
│   │   ├── database.md               # 数据库设计、ORM 使用与事务管理
│   │   └── middleware.md             # 消息队列、缓存、调度器等中间件应用
│   ├── performance/                  # 性能调优层面文档
│   │   ├── jvm-tuning.md             # Java 虚拟机参数调优与内存分析
│   │   ├── sql-optimization.md       # SQL 查询优化与执行计划分析
│   │   └── cache-strategy.md         # 缓存穿透、雪崩、一致性策略
│   ├── operations/                   # 运维监控层面文档
│   │   ├── logging.md                # 日志规范、采集与集中管理
│   │   ├── monitoring.md             # 指标采集、告警规则与可视化
│   │   └── container.md              # 容器化部署、编排与服务发现
│   └── case-studies/                 # 综合案例文档
│       ├── ecommerce.md              # 电商场景下的技术组合实践
│       └── fintech.md                # 金融级高可用与数据一致性方案
├── resources/                        # 原始资源映射目录，按技术领域分类存放 .url 文件
│   ├── backend/                      # 后端开发相关资源
│   ├── frontend/                     # 前端工程化与性能优化资源
│   ├── devops/                       # 持续集成、部署与自动化运维资源
│   └── algorithm/                    # 数据结构与算法分析资源
├── scripts/                          # 辅助工具脚本
│   ├── fetch_meta.py                 # 批量获取文章标题和摘要的辅助脚本
│   └── generate_toc.py               # 为各个文档目录生成目录表格
└── tests/                            # 单元测试与链接可达性测试
    ├── test_index.py                 # 验证 INDEX.md 格式与链接完整性
    └── test_links.py                 # 检查资源链接的可访问性
```

## 贡献指南

我们欢迎开发者以多种方式参与 TechRef Navigator 的改进。请遵循以下步骤提交贡献。

第一，Fork 本仓库并克隆到本地。在您的 Fork 版本中创建一个新的功能分支，分支名称应简要描述您要进行的改动，例如 `feature/add-resource-category` 或 `fix/update-broken-links`。

第二，在 `resources/` 目录下按照既有的分类结构添加新的资源文件，或更新 `docs/` 目录下对应技术层面的 Markdown 导航文档。所有新增资源链接必须来源于用户提供的原始 URL 列表，且不得修改 URL 的拼写、大小写或协议前缀。

第三，运行本地的索引构建脚本 `python build_index.py --input ./resources --output ./INDEX.md`，确保 INDEX.md 文件能够正确生成且无报错。随后执行测试套件 `pytest tests/`，确认所有单元测试通过，特别是链接可达性测试不应将新增链接标记为不可达（除非目标站点临时维护）。

第四，提交代码并推送至您的远程仓库。提交信息应当采用语义化格式，例如 `docs: add 20 new resource entries to performance category` 或 `fix: correct the case of URL in INDEX.md`。提交后在本仓库的 Issues 页面创建一个新的 Pull Request，详细描述您的改动内容和测试结果。

第五，等待项目维护者的代码审查。审查过程中可能会要求您对分类进行调整或补充说明，请及时响应反馈。合并后您的贡献将被记录在项目的贡献者列表中。

## 常见问题

**问：项目中的 URL 为何全部来自同一个博客站点？未来是否会收录其他技术站点？**

答：TechRef Navigator 第一阶段的定位是针对 puhvjy 技术博客的深度索引，因为该站点内容覆盖面广且技术深度足够。未来项目路线图包括增加其他高质量技术博客的导航分支，但会保持每个站点的链接独立性和原始格式不变。我们不会对任何 URL 进行重定向、短链转换或内容转载，所有资源均指向原始出处。

**问：我发现某个资源链接已经失效或内容被删除，应该如何处理？**

答：由于我们收录的是第三方站点内容，链接失效属于外部不可控因素。如果您发现失效链接，请在本项目的 Issues 中提交问题报告，并附上具体的 URL 和访问错误码。项目维护者会定期检查链接可达性，对于确认失效的链接，会在 INDEX.md 中标记为 [ARCHIVED] 状态并保留原 URL，同时尝试寻找替代的有效链接（若存在）。我们不会擅自删除失效链接，以保持资源列表的完整历史记录。

**问：我能否使用本项目的资源列表来构建自己的技术导航站或博客聚合页？**

答：本项目采用 MIT 许可证，您完全可以使用本项目的资源列表作为您自己项目的数据源。但请注意，项目中的 URL 指向的内容版权归属于原始作者，我们不主张对这些内容的任何权利。在您的项目中重新分发这些 URL 时，请务必保持链接的原始格式，并注明数据来源为本项目。我们不建议对链接进行任何形式的篡改或包装，以尊重原始内容提供者的劳动成果。

## 许可证

MIT

> 外链数量: 250 | 生成时间: 2026-07-05 16:29:44
