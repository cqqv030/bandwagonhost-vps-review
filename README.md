# BandwagonHost VPS review：值不值得买？先看懂 CN2 GIA 线路、全套餐价格和这几条硬限制

搜「BandwagonHost VPS review」的人，大多卡在同一个问题上：这家起步价只要几十美元一年的老牌 VPS，到底是真的香，还是便宜没好货？尤其是它家反复出现的 CN2 GIA、CN2 GIA-E、SLA 这些线路名词，看完一圈介绍反而更糊涂了。这篇文章把套餐、价格、线路区别和真正的短板一次讲清楚，帮你判断它适不适合你，以及下手时该选哪一档。

**先说结论：它适合谁，不适合谁**

BandwagonHost（搬瓦工）是一家运营超过 20 年的加拿大 VPS 服务商（背后公司为 IT7 Networks），主打 KVM 架构的自管理 VPS，最大卖点是中国方向的网络路由质量，也就是俗称的 CN2 GIA 线路。它的入门款 20G KVM 套餐年付 **$49.99**，折合每月约 $4.17，但机房位置、线路质量不同，价格差异可以拉到几百美元一个月，所以「买哪条线」比「买不买」更重要。

适合考虑它的情况很明确：你需要一台从中国大陆访问质量较好的海外 VPS，比如跑外贸网站、跨境业务、开发测试机或自建网络服务；同时你不怕命令行，能自己装系统、自己运维。

以下情况建议直接绕开：你想要 cPanel 那种点点鼠标就能建站的托管主机；你需要月付灵活随开随停的低配机器（它家最便宜的档位只按年卖）；或者你指望工单客服帮你管服务器——它家官网在套餐页面写得很直白，"Strictly self-managed service"，纯粹自助。

**BandwagonHost 是一家什么样的服务商**

用几个官方事实勾勒一下轮廓。它的所有套餐都跑在 KVM 虚拟化上，控制面板是自研的 KiwiVM，支持开关机、重装系统、VNC 应急控制台、rDNS 设置、机房迁移、快照、用量统计和 API。系统模板覆盖 AlmaLinux、RockyLinux、Debian、Ubuntu、CentOS 系和 Fedora，也支持手动挂载 ISO 安装。

在线率承诺分三档：官网首页写的是 99.9%，普通套餐页面标注 99.95%，而 E-Commerce SLA 系列直接给出 99.99% 的服务水平协议（SLA）——不过官方注明目前只有洛杉矶 USCA_5 机房提供 99.99% SLA。退款政策是 30 天，官方知识库明确有 30 天退款保证，但需符合服务条款，常见要求包括新购订单、在规定时间内提交申请，不是无条件的。

机房方面，官网宣传全球近 20 个数据中心，不同产品线开放的数量不一样：入门 KVM 套餐目前开放 6 个机房，CN2 GIA-E 套餐可以在 16 个机房之间切换。还有一点在同类服务里很少见：VPS 可以在机房之间免费迁移，不丢数据，KiwiVM 面板里选个目标机房就行。

硬件最近也在更新。官网新闻显示，纽约、洛杉矶 DC9、香港 HK3/HK8 等机房已陆续上线 AMD EPYC 服务器搭配 NVMe RAID-10 存储，KiwiVM 也新加了 Ubuntu 26.04 和 Debian 13 系统模板。SLA 系列则直接用 AMD 专属核心加本地 NVMe。

**全套餐与价格：四条产品线，差距全在线路上**

BandwagonHost 当前在售的套餐分四条产品线：KVM PROMO（常规多机房）、CN2 GIA ECOMMERCE（简称 CN2 GIA-E）、E-Commerce SLA，以及香港/东京/大阪/新加坡等亚洲 CN2 GIA 专线。核心差异在网络：KVM 走普通线路 1Gbps，GIA-E 走中国优化线路 2.5Gbps 起步，SLA 在此基础上叠加 99.99% SLA 和更高级的机房设施。

先看产品线总览：

| 产品线 | 起步配置 | 起步价格 | 带宽 | 可选机房 | 参考链接 |
| --- | --- | --- | --- | --- | --- |
| KVM PROMO | 1GB / 2核 / 20GB / 1TB | $49.99/年 | 1Gbps | 6 个多机房 | [ 查看全部 KVM 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=44) |
| CN2 GIA-E | 1GB / 2核 / 20GB / 1TB | $49.99/季 | 2.5Gbps | 16 个机房 | [ 查看 CN2 GIA-E 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=87) |
| E-Commerce SLA | 1GB ECC / 2核AMD / 20GB NVMe / 1TB | $65.89/季 | 2.5Gbps | 洛杉矶（99.99% SLA） | [ 购买 E-Commerce SLA 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=164) |
| 香港 CN2 GIA | 2GB / 2核 / 40GB / 500GB | $89.99/月 | 1Gbps | 香港 | [ 查看香港 CN2 GIA 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=95) |
| 东京 CN2 GIA | 2GB / 2核 / 40GB / 500GB | $89.99/月 | 1.2Gbps | 东京 | [ 查看东京 CN2 GIA 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=108) |
| 大阪 CN2 GIA | 2GB / 2核 / 40GB / 500GB | $49.99/月 | 1.5Gbps | 大阪 | [ 查看大阪 CN2 GIA 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=134) |
| 新加坡 CN2 GIA | 2GB / 2核 / 40GB / 500GB | $49.99/月 | 1.5Gbps | 新加坡 | [ 查看新加坡 CN2 GIA 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=173) |

下面是各条产品线的完整档位明细。KVM PROMO 全部 6 档（年付是最省的计费周期）：

| 档位 | CPU | 内存 | SSD（RAID-10） | 月流量 | 带宽 | 起步价格 | 年付价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 20G KVM | 2核 | 1GB | 20GB | 1TB | 1Gbps | $49.99/年 | 同左 | [ 购买 20G KVM 年付套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=44) |
| 40G KVM | 3核 | 2GB | 40GB | 2TB | 1Gbps | $52.99/半年 | $99.99 | [ 购买 40G KVM 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=45) |
| 80G KVM | 4核 | 4GB | 80GB | 3TB | 1Gbps | $19.99/月 | $199.99 | [ 购买 80G KVM 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=46) |
| 160G KVM | 5核 | 8GB | 160GB | 4TB | 1Gbps | $39.99/月 | $399.99 | [ 购买 160G KVM 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=47) |
| 320G KVM | 6核 | 16GB | 320GB | 5TB | 1Gbps | $79.99/月 | $799.99 | [ 购买 320G KVM 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=48) |
| 480G KVM | 7核 | 24GB | 480GB | 6TB | 1Gbps | $119.99/月 | $1,199.99 | [ 购买 480G KVM 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=49) |

CN2 GIA-E 全部 7 档（这条线是多数中国用户的主力选择，全部档位都可在 16 个机房间免费切换）：

| 档位 | CPU | 内存 | SSD | 月流量 | 带宽 | 起步价格 | 年付价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 20G | 2核 | 1GB | 20GB | 1TB | 2.5Gbps | $49.99/季 | $169.99 | [ 购买 CN2 GIA-E 20G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=87) |
| 40G | 3核 | 2GB | 40GB | 2TB | 2.5Gbps | $89.99/季 | $299.99 | [ 购买 CN2 GIA-E 40G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=88) |
| 80G | 4核 | 4GB | 80GB | 3TB | 2.5Gbps | $56.99/月 | $549.99 | [ 购买 CN2 GIA-E 80G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=89) |
| 160G | 6核 | 8GB | 160GB | 5TB | 5Gbps | $86.99/月 | $879.99 | [ 购买 CN2 GIA-E 160G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=90) |
| 320G | 8核 | 16GB | 320GB | 8TB | 5Gbps | $159.99/月 | $1,599.99 | [ 购买 CN2 GIA-E 320G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=91) |
| 640G | 10核 | 32GB | 640GB | 10TB | 10Gbps | $289.99/月 | $2,759.99 | [ 购买 CN2 GIA-E 640G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=92) |
| 1280G | 12核 | 64GB | 1.28TB | 12TB | 10Gbps | $549.99/月 | $5,499.99 | [ 购买 CN2 GIA-E 1280G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=93) |

E-Commerce SLA 全部 9 档（目前仅洛杉矶机房，99.99% SLA，AMD 专属核心 + NVMe，支持每两周一次免费换 IP）：

| 档位 | CPU | 内存 | SSD | 月流量 | 起步价格 | 年付价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 20G | 2核 AMD | 1GB ECC | 20GB NVMe | 1TB | $65.89/季 | $239.99 | [ 购买 SLA 20G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=164) |
| 40G | 3核 AMD | 2GB ECC | 40GB NVMe | 2TB | $116.99/季 | $399.99 | [ 购买 SLA 40G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=165) |
| 80G | 4核 AMD | 4GB ECC | 80GB NVMe | 3TB | $69.99/月 | $699.99 | [ 购买 SLA 80G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=166) |
| 160G | 6核 AMD | 8GB ECC | 160GB NVMe | 5TB | $109.99/月 | $1,099.99 | [ 购买 SLA 160G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=167) |
| 320G | 8核 AMD | 16GB ECC | 320GB NVMe | 8TB | $199.99/月 | $1,999.99 | [ 购买 SLA 320G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=168) |
| 640G | 10核 AMD | 32GB ECC | 640GB NVMe | 10TB | $369.99/月 | $3,699.99 | [ 购买 SLA 640G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=169) |
| 1280G（12TB） | 12核 AMD | 64GB ECC | 1.28TB NVMe | 12TB | $699.99/月 | $6,999.99 | [ 购买 SLA 1280G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=170) |
| 1280G（15TB） | 12核 AMD | 64GB ECC | 1.28TB NVMe | 15TB | $879.99/月 | $8,799.99 | [ 购买 SLA 1280G 15TB 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=171) |
| 1280G（20TB） | 12核 AMD | 64GB ECC | 1.28TB NVMe | 20TB | $1,159.99/月 | $11,598.99 | [ 购买 SLA 1280G 20TB 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=172) |

香港、东京、大阪、新加坡四条亚洲 CN2 GIA 专线，每个城市各有 6 档，配置阶梯一致（从 2GB/40GB/500GB 一路到 64GB/1.28TB/8TB），起步档价格如下，完整档位可在下单页切换查看：

> [👉 查看香港 CN2 GIA 全部档位（2GB 档 $89.99/月起）](https://bandwagonhost.com/aff.php?aff=79616&pid=95)
> [👉 查看东京 CN2 GIA 全部档位（2GB 档 $89.99/月起）](https://bandwagonhost.com/aff.php?aff=79616&pid=108)
> [👉 查看大阪 CN2 GIA 全部档位（2GB 档 $49.99/月起）](https://bandwagonhost.com/aff.php?aff=79616&pid=134)
> [👉 查看新加坡 CN2 GIA 全部档位（2GB 档 $49.99/月起）](https://bandwagonhost.com/aff.php?aff=79616&pid=173)

另外，官网站内还出现过迪拜等更小众的特殊线路，是否在售、什么价，以下单页实时列表为准。限量抢购类套餐（如 MINIBOX、MINICHICKEN 这类年付 $19 档的迷你机型）长期处于售罄状态，补货几小时内就会被抢完，这类套餐还对 CPU 使用率有额外限制（官方注册页注明 MINIBOX 限单核 20%、BIGGERBOX 限单核 25%）。

> 提醒一句：同一配置下，KVM 和 CN2 GIA-E 的差价主要买的是线路。如果你对国内访问速度没要求，KVM 年付 $49.99 那档性价比最高；如果建站给国内用户访问，CN2 GIA-E 是公认的起点，别为了省每季十几美元选错线。

**CN2 GIA 到底是什么，为什么有人愿意多花钱**

CN2 是中国电信的下一代骨干网（AS4809），GIA 是其中定位最高的产品线，从机房出口到国内全程走电信精品网，避免绕路和跨境拥塞节点。BandwagonHost 官方对其 SLA 机房的描述是：回程覆盖中国电信 CN2 GIA/CTGNet（AS4809/AS23764）、联通精品网（AS10099）、移动 CMIN2（AS58807）三大运营商线路，并与 Apple、Google、Facebook、字节跳动等网络直连对等互联，多条 100Gbps 上联自动故障切换。

翻译成人话：晚高峰时段，普通线路的跨境流量容易拥堵掉速，而 CN2 GIA 的目标是这时段也能保持较低的延迟和可用的速度。这也是它和 Vultr、DigitalOcean 这类通用云最本质的区别——后者同价位给的是更高的通用配置，但没有针对中国方向的路由优化。

代价也写得明明白白。官方 CN2 GIA 介绍页提到，这条线路的 IP 转发成本非常高（举例称每兆可达 120 美元量级），所以 GIA 系列套餐贵、流量给得少（起步档每月 1TB 甚至 500GB），这钱本质上是在买路由质量而不是买算力。另外线路质量也受你所在地区和运营商影响，Reddit 上有用户反馈即便 CN2 GIA，某些地区晚高峰也只能跑到 5Mbps 左右的速率——下单前不妨先用官网提供的测速节点试试本地实际表现。

**日常使用是什么样的**

KiwiVM 面板是体验里被提起最多的部分。开箱流程是：下单后进 KiwiVM，选系统模板或挂 ISO 安装，几分钟后就能 SSH 登录，root 权限完整。面板里能做的事包括开关机、重装、VNC 应急、快照、rDNS、API 操作等。

备份这块目前给得挺大方：套餐页明确标注「免费自动备份 + 免费快照」，不用额外付费。需要注意快照的保留规则——按国内搬瓦工教程站的整理，手动快照默认保留 30 天，每台 VPS 可以设置两个永久快照，自动备份则由系统按周期执行。重要数据建议再做异地备份，这是任何 VPS 的通用原则，不只是它家。

机房迁移是另一个实用功能。16 机房的 CN2 GIA-E 套餐可以在面板里把 VPS 从洛杉矶 DC6 搬到 DC9、搬到日本或欧洲节点，免费且不丢数据。IP 质量不理想时，SLA 系列还支持每两周一次免费换 IP（官方页面标注），其他系列的面板内也有换 IP 入口，规则以下单页说明为准。

升级不太方便这一点要提前知道：标准 KVM 线路不支持无缝升配，第三方指南的做法是直接买更大的套餐，再通过 KiwiVM 的迁移功能把数据搬过去。选套餐时宁可稍微留点余量，也别按刚刚好的配置下单。

**优惠码和省钱技巧**

搬瓦工的优惠码是循环折扣码，购买和续费都能用，折扣力度通常在 6.77% 上下。综合 2026 年多个优惠码汇总站的信息：

- **NODESEEK2026**：2026 年多个时间点被报道可用的循环码，折扣 6.77%，新购和续费同享；
- **BWHCGLUKKB**：社区流传多年的老牌循环码，折扣 6.77%，多个 2026 年汇总页仍列为可用；
- 另有站点给出 **ILOVEBANDWAGON**（约 11% 折扣）的说法，但只有单一来源提及，与其他「老码已过期」的汇总存在冲突，下单前建议在结账页实测。

大促节点主要看双 11 和黑五，力度通常比日常码大一些。社区还会用第三方库存监控页（如 stock.bwg.net）蹲限量套餐的补货。

省钱的核心逻辑其实和优惠码关系不大，在于计费周期：它家长周期单价明显更低，比如 40G KVM 半年付 $52.99、年付只要 $99.99，相当于月均 $8.33 对 $8.83；CN2 GIA-E 20G 季付 $49.99、年付 $169.99，年付每月省约 $2.8。确定会长期用，直接年付；只是想试用，季付的 GIA-E 或月付的 80G KVM 更稳妥，反正 30 天内退款有兜底。

**和 Vultr、DigitalOcean 这类云主机比，怎么选**

横向比较时先明确一件事：它们不是同类竞品。Vultr、DigitalOcean 按小时计费，$5-6/月就有 1GB 内存机型，机房多、部署快，适合全球分布的通用业务；BandwagonHost 的价值集中在「中国大陆方向的访问质量」这一件事上，外加免费机房迁移和长周期低价。

VPSBenchmarks 等测试站对两者做过跑分对比，通用性能维度互有胜负，但这类测试通常不覆盖中国方向的晚高峰表现，而这恰恰是选搬瓦工的人最关心的指标。Reddit 的 web hosting 社区里，讨论中国大陆访问质量时 CN2 GIA 是被推荐频率很高的方案之一，同时也有用户提醒高峰期速度受地区影响。所以判断标准很简单：业务面向国内用户，优先 CN2 GIA-E；业务面向海外，Vultr/DO 这类按需云通常更灵活也更便宜；两头都要，那就国内方向用搬瓦工、海外部分交给通用云。

**下单前必须知道的几个短板**

- **纯粹自管理**：没有控制面板、没有托管服务，官方连「我们因此才能压低价格」都写在了首页。完全没碰过 Linux 的人，上手成本不低。
- **入门档只按年卖**：最便宜的 20G KVM 没有月付选项，想低成本试错只能靠 30 天退款政策。
- **升级要手动搬数据**：标准 KVM 线路没有原地升配，容量规划要提前做。
- **快照默认保留 30 天**：长期快照每台只能设两个，重要数据别全押在面板功能上。
- **限量套餐极难抢**：$19/年那类传奇套餐基本是补货秒空，按常价套餐做预算才现实。
- **线路不是万能保险**：CN2 GIA 也会受本地运营商和高峰期影响，极端情况下 IP 被墙也是这类业务的固有风险。

**购买流程走一遍**

流程本身不复杂：注册账号后进入服务订购页，选产品线和档位；关键的两步是选计费周期（Billing Cycle）和机房（Location）——GIA-E 记得选洛杉矶 DC9 或 DC6 等优化节点；结账页填写优惠码；支付方式包括信用卡、PayPal，国内用户常用的支付宝也有大量 2026 年的购买教程覆盖，以结账页实际显示为准。付款后几分钟内开通，收到邮件后进 KiwiVM 装系统就能用了。下单入口在这里：[👉 进入 BandwagonHost 核对实时库存与价格](https://bit.ly/BandwagonHost)。

**常见问题**

**30 天内真的能退款吗？** 官方知识库确认有 30 天退款保证，但需符合服务条款，常见条件包括新购订单、按时提交申请。特定支付方式（如加密货币）是否可退，下单前先看条款或问客服确认。

**没有Linux 基础能用吗？** 能买，但会难受。它的定位是给会基础运维的人省钱，如果你需要面板建站，带 cPanel 的托管主机是更好的起点。

**能装 Windows 吗？** 官方模板列表里只有各类 Linux 发行版，没有官方 Windows 模板，许可证也要自己解决。

**IP 被墙了怎么办？** SLA 系列支持每两周一次免费换 IP；其他系列的换 IP 规则以 KiwiVM 面板和官方说明为准。选择机房时避开拥堵节点、平时做好数据备份，是更实际的风险管理。

**最后怎么选**

一句话版本：预算有限、对国内速度要求不高，KVM 年付 $49.99 闭眼入；建站或业务面向国内用户，CN2 GIA-E 季付 $49.99 起步，先试用再转年付；跑关键业务、需要 99.99% SLA 和 NVMe，看 E-Commerce SLA 系列；香港东京这类极致低延迟的专线，先想清楚每月 $89.99 起的预算是否花得值。优惠码记得填，年付记得选，限量套餐的补货就随缘吧。
