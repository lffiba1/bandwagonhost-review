# bandwagonhost测评：搬瓦工VPS真实表现、套餐对比与选购避坑指南

如果你正在搜 bandwagonhost 测评，大概率是想搞清楚两件事：这家老牌 VPS 商家到底值不值得买，以及那么多种套餐里哪一款才适合自己。本文把搬瓦工（BandwagonHost）目前官网在售的全部套餐、各机房实测表现、优惠码现状、退款和支付方式一次性讲清楚，帮你看完就能下单。

## 一、搬瓦工是什么：背景与定位

搬瓦工（BandwagonHost）隶属于加拿大 IT7 Networks，从 2004 年开始做 VPS 业务，是国内用户最早接触的一批海外 VPS 商家之一。它真正火起来，靠的是把中国电信 CN2 GIA 这种高端线路做成了相对便宜的产品，再加上自主开发的 KiwiVM 控制面板把重装系统、迁移机房、快照这些操作做得很顺，所以在国内技术圈一直有稳定的存在感。

需要先说清楚的一点是：搬瓦工走的是 self-managed（自管理）路线，价格压得低的前提是你自己搞定服务器运维。它不提供 cPanel、不代管 WordPress、不做安全加固，开出来就是一台带 SSH 的 Linux 机器。如果你需要的是"全托管建站"，搬瓦工不是合适的选择。

## 二、各机房线路与实测表现

搬瓦工的核心卖点一直是线路，而不是单纯的配置。理解它的套餐，先要理解它分了哪几条线。

**KVM 常规线路（DC2/DC4/DC8 等）**：走普通国际出口，没有 CN2 优化。延迟高、晚高峰容易抖，价格最便宜，适合做测试机、跳板、下载站这种对延迟不敏感的场景。

**CN2 GIA-E（DC6 / DC9）**：搬瓦工最有代表性的产品线，走中国电信 CN2 GIA 双程优化线路。根据第三方实测数据，DC6 CN2 GIA-E 到国内三网平均延迟通常在 130–180ms 之间，晚高峰丢包率接近 0，速度稳定。DC9 是 DC6 的"兄弟机房"，已升级 AMD+NVMe，效果接近。这两条线是搬瓦工的主力推荐，也是绝大多数国内用户买搬瓦工的理由。

**香港 / 东京 / 新加坡 / 大阪 CN2 GIA**：物理位置更近，延迟更低（日本软银 JPOS_1 实测到国内约 50–80ms），但价格也明显高一档。香港 CN2 GIA 月付 $89.99 起，年付 $899.99 起，是搬瓦工最贵的常规套餐线。

**SLA 套餐（DC5）**：在 CN2 GIA-E 基础上加了 99.99% SLA 保障和独享 CPU 核心，面向对稳定性有硬性要求的业务，价格比同配置 CN2 GIA-E 高约 30%。

> 提示：搬瓦工所有套餐都不含 DDoS 防御。如果建站被大流量攻击，IP 会被空路由（Nullrouted），需要联系客服处理或换 IP。这是它和 Cloudflare、阿里云这类有防御方案的服务商最明显的差距。

## 三、官网在售套餐全览（2026 年 8 月核验）

下面是搬瓦工官网当前公开展示的全部套餐，按产品线分组。价格和配置均来自官网 vps-hosting 页面及官方补货页面，截至 2026 年 8 月仍有效。

### KVM 常规套餐（入门线）

| 套餐 | CPU | 内存 | SSD | 月流量 | 带宽 | 可选机房 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| KVM 1GB | 2 核 | 1GB | 20GB | 1TB | 1Gbps | DC2/DC4/DC8 等 9 个机房 | $49.99/年 | [购买 KVM 1GB](https://bwh81.net/aff.php?aff=77528&pid=44) |
| KVM 2GB | 3 核 | 2GB | 40GB | 2TB | 1Gbps | 同上 | $52.99/半年，$99.99/年 | [购买 KVM 2GB](https://bwh81.net/aff.php?aff=77528&pid=45) |
| KVM 4GB | 4 核 | 4GB | 80GB | 3TB | 1Gbps | 同上 | $19.99/月，$199.99/年 | [购买 KVM 4GB](https://bwh81.net/aff.php?aff=77528&pid=46) |
| KVM 8GB | 5 核 | 8GB | 160GB | 4TB | 1Gbps | 同上 | $39.99/月，$399.99/年 | [购买 KVM 8GB](https://bwh81.net/aff.php?aff=77528&pid=47) |
| KVM 16GB | 6 核 | 16GB | 320GB | 5TB | 1Gbps | 同上 | $79.99/月，$799.99/年 | [购买 KVM 16GB](https://bwh81.net/aff.php?aff=77528&pid=48) |
| KVM 24GB | 7 核 | 24GB | 480GB | 6TB | 1Gbps | 同上 | $119.99/月，$1199.99/年 | [购买 KVM 24GB](https://bwh81.net/aff.php?aff=77528&pid=49) |

KVM 线最便宜的是 1GB 那款，年付 $49.99，约合人民币 350 元，是搬瓦工历史上最畅销的入门款。但要注意它走的是普通线路，不是 CN2。

### CN2 GIA-E 套餐（主力推荐线）

| 套餐 | CPU | 内存 | SSD | 月流量 | 带宽 | 可选机房 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CN2 GIA-E 1GB | 2 核 | 1GB | 20GB | 1TB | 2.5Gbps | DC6/DC9/JPOS_1/EUNL_9 等 14 个机房可迁移 | $49.99/季，$169.99/年 | [购买 CN2 GIA-E 1GB](https://bwh81.net/aff.php?aff=77528&pid=87) |
| CN2 GIA-E 2GB | 3 核 | 2GB | 40GB | 2TB | 2.5Gbps | 同上 | $89.99/季，$299.99/年 | [购买 CN2 GIA-E 2GB](https://bwh81.net/aff.php?aff=77528&pid=88) |
| CN2 GIA-E 4GB | 4 核 | 4GB | 80GB | 3TB | 2.5Gbps | 同上 | $56.99/月，$549.99/年 | [购买 CN2 GIA-E 4GB](https://bwh81.net/aff.php?aff=77528&pid=89) |
| CN2 GIA-E 8GB | 6 核 | 8GB | 160GB | 5TB | 5Gbps | 同上 | $86.99/月，$879.99/年 | [购买 CN2 GIA-E 8GB](https://bwh81.net/aff.php?aff=77528&pid=90) |
| CN2 GIA-E 16GB | 8 核 | 16GB | 320GB | 8TB | 5Gbps | 同上 | $159.99/月，$1599.99/年 | [购买 CN2 GIA-E 16GB](https://bwh81.net/aff.php?aff=77528&pid=91) |
| CN2 GIA-E 32GB | 10 核 | 32GB | 640GB | 10TB | 10Gbps | 同上 | $289.99/月，$2759.99/年 | [购买 CN2 GIA-E 32GB](https://bwh81.net/aff.php?aff=77528&pid=92) |
| CN2 GIA-E 64GB | 12 核 | 64GB | 1280GB | 12TB | 10Gbps | 同上 | $549.99/月，$5399.99/年 | [购买 CN2 GIA-E 64GB](https://bwh81.net/aff.php?aff=77528&pid=93) |

CN2 GIA-E 1GB 是搬瓦工最值得买的款，季付 $49.99 折合月付约 $16.66，年付 $169.99 折合月付约 $14.17，比香港 CN2 GIA 便宜一大截，又享受双程 CN2 GIA 优化。带宽 2.5Gbps 也比 KVM 的 1Gbps 高出一档。

### 香港 CN2 GIA 套餐（高端顶配线）

| 套餐 | CPU | 内存 | SSD | 月流量 | 带宽 | 可选机房 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| HK CN2 GIA 2GB | 2 核 | 2GB | 40GB | 500GB | 1Gbps | 香港 CN2 GIA（HKHK_8） | $89.99/月，$899.99/年 | [购买 HK 2GB](https://bwh81.net/aff.php?aff=77528&pid=95) |
| HK CN2 GIA 4GB | 4 核 | 4GB | 80GB | 1TB | 1Gbps | 同上 | $155.99/月，$1559.99/年 | [购买 HK 4GB](https://bwh81.net/aff.php?aff=77528&pid=96) |
| HK CN2 GIA 8GB | 6 核 | 8GB | 160GB | 2TB | 1Gbps | 同上 | $299.99/月，$2999.99/年 | [购买 HK 8GB](https://bwh81.net/aff.php?aff=77528&pid=97) |
| HK CN2 GIA 16GB | 8 核 | 16GB | 320GB | 4TB | 1Gbps | 同上 | $589.99/月，$5899.99/年 | [购买 HK 16GB](https://bwh81.net/aff.php?aff=77528&pid=98) |
| HK CN2 GIA 32GB | 10 核 | 32GB | 640GB | 6TB | 1Gbps | 同上 | $989.99/月，$9989.99/年 | [购买 HK 32GB](https://bwh81.net/aff.php?aff=77528&pid=122) |
| HK CN2 GIA 64GB | 12 核 | 64GB | 1280GB | 8TB | 1Gbps | 同上 | $1889.99/月，$18989.99/年 | [购买 HK 64GB](https://bwh81.net/aff.php?aff=77528&pid=124) |

香港线月付起步 $89.99，是搬瓦工最贵的常规套餐，但延迟最低、最适合对国内访问速度有极致要求的业务。

### 东京 CN2 GIA 套餐

| 套餐 | CPU | 内存 | SSD | 月流量 | 带宽 | 可选机房 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Tokyo CN2 GIA 2GB | 2 核 | 2GB | 40GB | 500GB | 1.2Gbps | 东京 CN2 GIA（JPTYO_8） | $89.99/月，$899.99/年 | [购买 Tokyo 2GB](https://bwh81.net/aff.php?aff=77528&pid=108) |
| Tokyo CN2 GIA 4GB | 4 核 | 4GB | 80GB | 1TB | 1.2Gbps | 同上 | $155.99/月，$1559.99/年 | [购买 Tokyo 4GB](https://bwh81.net/aff.php?aff=77528&pid=109) |
| Tokyo CN2 GIA 8GB | 6 核 | 8GB | 160GB | 2TB | 1.2Gbps | 同上 | $299.99/月，$2999.99/年 | [购买 Tokyo 8GB](https://bwh81.net/aff.php?aff=77528&pid=110) |
| Tokyo CN2 GIA 16GB | 8 核 | 16GB | 320GB | 4TB | 1.2Gbps | 同上 | $589.99/月，$5899.99/年 | [购买 Tokyo 16GB](https://bwh81.net/aff.php?aff=77528&pid=111) |
| Tokyo CN2 GIA 32GB | 10 核 | 32GB | 640GB | 6TB | 1.2Gbps | 同上 | $989.99/月，$9989.99/年 | [购买 Tokyo 32GB](https://bwh81.net/aff.php?aff=77528&pid=123) |
| Tokyo CN2 GIA 64GB | 12 核 | 64GB | 1280GB | 8TB | 1.2Gbps | 同上 | $1889.99/月，$18989.99/年 | [购买 Tokyo 64GB](https://bwh81.net/aff.php?aff=77528&pid=125) |

### 大阪 CN2 GIA 套餐

| 套餐 | CPU | 内存 | SSD | 月流量 | 带宽 | 可选机房 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Osaka CN2 GIA 2GB | 2 核 | 2GB | 40GB | 500GB | 1.5Gbps | 大阪 CN2 GIA | $49.99/月，$499.99/年 | [购买 Osaka 2GB](https://bwh81.net/aff.php?aff=77528&pid=134) |
| Osaka CN2 GIA 4GB | 4 核 | 4GB | 80GB | 1TB | 1.5Gbps | 同上 | $86.99/月，$869.99/年 | [购买 Osaka 4GB](https://bwh81.net/aff.php?aff=77528&pid=135) |
| Osaka CN2 GIA 8GB | 6 核 | 8GB | 160GB | 2TB | 1.5Gbps | 同上 | $165.99/月，$1665.99/年 | [购买 Osaka 8GB](https://bwh81.net/aff.php?aff=77528&pid=136) |
| Osaka CN2 GIA 16GB | 8 核 | 16GB | 320GB | 4TB | 1.5Gbps | 同上 | $329.99/月，$3279.99/年 | [购买 Osaka 16GB](https://bwh81.net/aff.php?aff=77528&pid=137) |
| Osaka CN2 GIA 32GB | 10 核 | 32GB | 640GB | 6TB | 1.5Gbps | 同上 | $549.99/月，$5549.99/年 | [购买 Osaka 32GB](https://bwh81.net/aff.php?aff=77528&pid=138) |
| Osaka CN2 GIA 64GB | 12 核 | 64GB | 1280GB | 8TB | 1.5Gbps | 同上 | $1059.99/月，$10559.99/年 | [购买 Osaka 64GB](https://bwh81.net/aff.php?aff=77528&pid=139) |

### 新加坡 CN2 GIA 套餐

| 套餐 | CPU | 内存 | SSD | 月流量 | 带宽 | 可选机房 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Singapore CN2 GIA 2GB | 2 核 | 2GB | 40GB | 500GB | 1.5Gbps | 新加坡 CN2 GIA（SG_8） | $49.99/月，$499.99/年 | [购买 Singapore 2GB](https://bwh81.net/aff.php?aff=77528&pid=173) |
| Singapore CN2 GIA 4GB | 4 核 | 4GB | 80GB | 1TB | 1.5Gbps | 同上 | $86.99/月，$869.99/年 | [购买 Singapore 4GB](https://bwh81.net/aff.php?aff=77528&pid=174) |
| Singapore CN2 GIA 8GB | 6 核 | 8GB | 160GB | 2TB | 2.5Gbps | 同上 | $165.99/月，$1665.99/年 | [购买 Singapore 8GB](https://bwh81.net/aff.php?aff=77528&pid=175) |
| Singapore CN2 GIA 16GB | 8 核 | 16GB | 320GB | 4TB | 2.5Gbps | 同上 | $329.99/月，$3199/年 | [购买 Singapore 16GB](https://bwh81.net/aff.php?aff=77528&pid=176) |
| Singapore CN2 GIA 32GB | 10 核 | 32GB | 640GB | 6TB | 5Gbps | 同上 | $549.99/月，$5549.99/年 | [购买 Singapore 32GB](https://bwh81.net/aff.php?aff=77528&pid=177) |
| Singapore CN2 GIA 64GB | 12 核 | 64GB | 1280GB | 8TB | 5Gbps | 同上 | $1059.99/月，$10559.99/年 | [购买 Singapore 64GB](https://bwh81.net/aff.php?aff=77528&pid=178) |

### 迪拜 ECOMMERCE 套餐

| 套餐 | CPU | 内存 | SSD | 月流量 | 带宽 | 可选机房 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Dubai 1GB | 2 核 | 1GB | 20GB | 500GB | 1Gbps | AEDXB_1 + 全部 CN2 GIA-E/KVM 机房可迁移 | $19.99/月，$169.99/年 | [购买 Dubai 1GB](https://bwh81.net/aff.php?aff=77528&pid=114) |
| Dubai 2GB | 3 核 | 2GB | 40GB | 1TB | 1Gbps | 同上 | $32.99/月，$299.99/年 | [购买 Dubai 2GB](https://bwh81.net/aff.php?aff=77528&pid=115) |
| Dubai 4GB | 4 核 | 4GB | 80GB | 2TB | 1Gbps | 同上 | $56.99/月，$549.99/年 | [购买 Dubai 4GB](https://bwh81.net/aff.php?aff=77528&pid=116) |
| Dubai 8GB | 6 核 | 8GB | 160GB | 3TB | 1Gbps | 同上 | $86.99/月，$879.99/年 | [购买 Dubai 8GB](https://bwh81.net/aff.php?aff=77528&pid=117) |
| Dubai 16GB | 8 核 | 16GB | 320GB | 4TB | 1Gbps | 同上 | $159.99/月，$1599.99/年 | [购买 Dubai 16GB](https://bwh81.net/aff.php?aff=77528&pid=118) |
| Dubai 32GB | 10 核 | 32GB | 640GB | 5TB | 1Gbps | 同上 | $289.99/月，$2759.99/年 | [购买 Dubai 32GB](https://bwh81.net/aff.php?aff=77528&pid=119) |
| Dubai 64GB | 12 核 | 64GB | 1280GB | 6TB | 1Gbps | 同上 | $549.99/月，$5399.99/年 | [购买 Dubai 64GB](https://bwh81.net/aff.php?aff=77528&pid=120) |

迪拜线是搬瓦工相对新的产品，1GB 款年付只要 $169.99，且支持迁移到 CN2 GIA-E 等机房，相当于用迪拜的低价买到 CN2 GIA-E 的访问能力，性价比突出。

### SLA 套餐（99.99% SLA 保障线）

| 套餐 | CPU | 内存 | NVMe | 月流量 | 带宽 | 可选机房 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SLA 1GB | 2 核（独享） | 1GB | 20GB | 1TB | 2.5Gbps | DC5 SLA + 99.99% SLA + 独享 IP | $65.89/季，$239.99/年 | [购买 SLA 1GB](https://bwh81.net/aff.php?aff=77528&pid=164) |
| SLA 2GB | 3 核（独享） | 2GB | 40GB | 2TB | 2.5Gbps | 同上 | $116.99/季，$399.99/年 | [购买 SLA 2GB](https://bwh81.net/aff.php?aff=77528&pid=165) |
| SLA 4GB | 4 核（独享） | 4GB | 80GB | 3TB | 2.5Gbps | 同上 | $69.99/月，$699.99/年 | [购买 SLA 4GB](https://bwh81.net/aff.php?aff=77528&pid=166) |
| SLA 8GB | 6 核（独享） | 8GB | 160GB | 5TB | 5Gbps | 同上 | $109.99/月，$1099.99/年 | [购买 SLA 8GB](https://bwh81.net/aff.php?aff=77528&pid=167) |
| SLA 16GB | 8 核（独享） | 16GB | 320GB | 8TB | 5Gbps | 同上 | $199.99/月，$1999.99/年 | [购买 SLA 16GB](https://bwh81.net/aff.php?aff=77528&pid=168) |
| SLA 32GB | 10 核（独享） | 32GB | 640GB | 10TB | 10Gbps | 同上 | $369.99/月，$3699.99/年 | [购买 SLA 32GB](https://bwh81.net/aff.php?aff=77528&pid=169) |
| SLA 64GB（12TB） | 12 核（独享） | 64GB | 1280GB | 12TB | 10Gbps | 同上 | $699.99/月，$6999.99/年 | [购买 SLA 64GB 12TB](https://bwh81.net/aff.php?aff=77528&pid=170) |
| SLA 64GB（15TB） | 12 核（独享） | 64GB | 1280GB | 15TB | 10Gbps | 同上 | $879.99/月，$8799.99/年 | [购买 SLA 64GB 15TB](https://bwh81.net/aff.php?aff=77528&pid=171) |
| SLA 64GB（20TB） | 12 核（独享） | 64GB | 1280GB | 20TB | 10Gbps | 同上 | $1159.99/月，$11598.99/年 | [购买 SLA 64GB 20TB](https://bwh81.net/aff.php?aff=77528&pid=172) |

SLA 线的核心差异是 CPU 全天独享（不限 burst）、99.99% SLA 保障和独享 IP，适合跑数据库、做生产业务这种不能被邻居挤占资源的场景。

## 四、优惠码现状：现在还能用什么码

这是 2026 年买搬瓦工最容易踩坑的地方，必须单独说。

历史上搬瓦工长期有一个 6.77% 的循环优惠码 `BWHCGLUKKB`，续费也打折，是绝大多数老用户购买时必填的码。但 2025 年 11 月双十一期间，官方主动停用了所有常规优惠码，换成限时 11% 的 `ILOVEBANDWAGON`。双十一活动结束后，这个 11% 码也失效了。

进入 2026 年后，情况是这样的：

- 2026 年 2 月，曾短暂出现 `NODESEEK2026`（6.77% 循环），来源是 NodeSeek 社区合作码，但很快被官方停用
- 2026 年 8 月，多个长期跟踪搬瓦工优惠码的站点（包括 bandwagonhost.net、banwagong.net）在最新整理中均未列出当前可用的常规循环码
- 部分第三方站点仍写着 `BWHCGLUKKB` 或 `ILOVEBANDWAGON`，但根据官方页面和多个 2026 年实测反馈，这些码在 checkout 时会提示"The promotion code entered has expired"

> 提示：本文不列出任何无法在当前官方页面确认有效的优惠码。如果你看到别的文章推荐 `BWHCGLUKKB`、`ILOVEBANDWAGON`、`BWH3HYATVBJW` 等码，建议先在结账页填入测试，提示过期就别浪费时间。搬瓦工的优惠码是循环折扣，一旦生效续费也打折，所以官方对放码很谨慎。

如果你确实想省一点，可以关注搬瓦工官方 Telegram 频道 @BandwagonHostNews 和补货站 stock.bwg.net，新码通常在这些渠道首发。

## 五、KiwiVM 控制面板：实际能做什么

KiwiVM 是搬瓦工自研的控制面板，也是它和很多同类商家的差异点。登录之后能做的事情包括：

- 查看 VPS 的 IP、SSH 端口、流量使用情况
- 开关机、重启、强制关机
- 一键重装系统（支持 AlmaLinux、RockyLinux、CentOS、Debian、Ubuntu、Fedora 等）
- 在线迁移机房（CN2 GIA-E 套餐支持在 14 个机房之间免费迁移，不丢数据）
- 创建快照备份和恢复
- 修改 root 密码、KiwiVM 密码
- 设置两步验证（2FA）
- 管理 rDNS（PTR 反向解析）
- 调用 API 做自动化操作

其中最实用的是机房迁移。比如你买了 CN2 GIA-E 1GB，默认开在 DC6，如果某天 DC6 抽风，可以在 KiwiVM 里一键迁到 DC9 或日本软银 JPOS_1，整个过程免费且不丢数据。这是搬瓦工相比很多"开机就锁死机房"的商家的明显优势。

## 六、支付与退款：买之前要知道的事

**支付方式**：搬瓦工目前支持支付宝、PayPal、信用卡（Visa/Master）。微信支付已经停用，账户余额充值也不再支持支付宝和微信，只能用 PayPal 或信用卡充。对国内用户来说，支付宝扫码是最方便的，系统自动按汇率换算成人民币扣款。

**退款政策**：搬瓦工提供 30 天无理由全额退款，但有几个硬性条件：

1. 账户创建时间不超过 30 天
2. 之前没有申请过退款
3. VPS 的 IP 可用（没被封、没被列入黑名单）
4. 月流量使用量未超过配额的 10%
5. 账户信誉良好，无违反 TOS 的记录

退款会原路返回到支付宝或信用卡，不收手续费，也不会退到搬瓦工账户余额。如果你买完发现线路不合适，30 天内申请退款是相对靠谱的兜底方案。

> 提示：注册账号时国家和基础信息尽量填真实的，个人信息可以稍作模糊但不要完全乱填；不要用 VPN 或换 IP 软件去注册和登录，容易被系统判定为高风险甚至欺诈订单，直接导致退款被拒。

## 七、真实优缺点：哪些人适合买，哪些人别买

把上面所有信息汇总一下，给一个直接的判断。

**适合买搬瓦工的人**：

- 需要 CN2 GIA 双程优化线路、对国内访问速度有要求的建站用户
- 想要长期稳定使用、看重续费价格不涨的用户（搬瓦工续费不涨价，且历史上优惠码是循环折扣）
- 需要灵活切换机房的用户（CN2 GIA-E 14 个机房免费迁移）
- 有一定 Linux 运维能力、不需要全托管的用户

**不适合买搬瓦工的人**：

- 需要 DDoS 防御的用户（搬瓦工所有套餐都不含防御）
- 需要全托管建站、cPanel、代管 WordPress 的用户
- 只想试用一个月的用户（最便宜套餐是年付，CN2 GIA-E 最低季付）
- 预算极低、对线路没要求的用户（这种场景 CloudCone、racknerd 等更便宜）
- 需要 Netflix 解锁、流媒体专线的用户（搬瓦工 IP 段被识别概率较高，不保证解锁）

**几个常见的真实缺点**：

- 便宜套餐只能年付，灵活性差
- 不含 DDoS 防御，被攻击会空路由
- GIA 出口带宽相对有限，遇到大流量攻击时整个 GIA 网络可能波动
- 优惠码不稳定，2026 年大部分时间没有可用常规码
- 超售问题存在（这是所有 VPS 商家的通病），高配套餐在极端高峰时段可能有抖动

## 八、选购建议：不同需求怎么选

如果你看到这里还是不知道买哪款，按需求对号入座：

**预算最紧、只想试试海外 VPS**：KVM 1GB，年付 $49.99，走普通线路。能跑、能用，但别指望国内访问速度。👉 [查看 KVM 1GB 套餐](https://bwh81.net/aff.php?aff=77528&pid=44)

**国内建站、博客、需要稳定访问**：CN2 GIA-E 1GB，年付 $169.99，双程 CN2 GIA，2.5Gbps 带宽，14 个机房可迁移。这是搬瓦工最经典的款，90% 的国内用户买的就是这个。👉 [查看 CN2 GIA-E 1GB 套餐](https://bwh81.net/aff.php?aff=77528&pid=87)

**小型电商、论坛、流量稍大**：CN2 GIA-E 2GB，年付 $299.99，2 核 3 线程、2TB 月流量，能撑住中小型站点。👉 [查看 CN2 GIA-E 2GB 套餐](https://bwh81.net/aff.php?aff=77528&pid=88)

**对延迟有极致要求**：香港 CN2 GIA 2GB，月付 $89.99，物理位置最近，国内访问延迟最低。预算够就上。👉 [查看香港 CN2 GIA 套餐](https://bwh81.net/aff.php?aff=77528&pid=95)

**跑数据库、生产业务、不能被挤资源**：SLA 1GB，季付 $65.89，独享 CPU + 99.99% SLA 保障。👉 [查看 SLA 套餐](https://bwh81.net/aff.php?aff=77528&pid=164)

**想要 CN2 GIA-E 但预算有限**：迪拜 1GB，年付 $169.99，开通后可迁移到 DC6/DC9 等 CN2 GIA-E 机房，相当于用迪拜的低价享受 CN2 GIA-E 线路。👉 [查看迪拜套餐](https://bwh81.net/aff.php?aff=77528&pid=114)

## 九、购买流程：从下单到开机

整个流程其实很简单，几步走完：

1. 进入 👉 [搬瓦工官网](https://bit.ly/BandWaGon)，在 vps-hosting 页面选套餐
2. 选择计费周期（年付通常比月付划算 15%–20%）和机房
3. 进入 Review & Checkout，如果有可用优惠码在"Promotional Code"填入并点"Validate Code"
4. 填写注册信息（国家、邮箱、地址），建议用真实信息
5. 选择支付方式，国内用户选支付宝，扫码付款
6. 付款后几分钟内会收到开通邮件，里面有 KiwiVM 登录地址、VPS IP 和 root 密码
7. 登录 KiwiVM 后可以重装系统、迁移机房、改 SSH 端口

如果开通后发现线路不合适，30 天内可以在 KiwiVM 里提交退款申请，符合条件会全额退回支付宝。

## 十、常见问题

**Q：搬瓦工现在还有优惠码吗？**
A：截至 2026 年 8 月，没有可靠来源确认有长期可用的常规循环码。历史上 `BWHCGLUKKB`（6.77%）和 `ILOVEBANDWAGON`（11%）都已被官方停用。建议关注官方 Telegram @BandwagonHostNews 等待新码发布。

**Q：CN2 GIA-E 和香港 CN2 GIA 怎么选？**
A：CN2 GIA-E 走美国洛杉矶，延迟 130–180ms，年付 $169.99 起，性价比高；香港 CN2 GIA 物理位置近，延迟更低，但月付 $89.99 起，年付 $899.99 起，贵了 5 倍多。预算够、对延迟敏感选香港；预算一般、要稳定选 CN2 GIA-E。

**Q：可以换机房吗？**
A：可以。CN2 GIA-E 套餐支持在 14 个机房之间免费迁移，包括 DC6、DC9、JPOS_1、EUNL_9 等，在 KiwiVM 面板一键操作，不丢数据。KVM 套餐支持 9 个机房迁移。香港、东京、新加坡、大阪 CN2 GIA 套餐只能在各自机房内，不能跨地区迁。

**Q：搬瓦工会跑路吗？**
A：搬瓦工从 2004 年运营至今，是海外 VPS 老牌商家，自有硬件和 IP 段，跑路风险相对较低。但任何 VPS 商家都不能 100% 保证，重要数据建议定期做快照备份或异地备份。

**Q：买哪个套餐最划算？**
A：90% 的国内用户选 CN2 GIA-E 1GB（年付 $169.99）就够了。如果预算紧、对线路没要求，KVM 1GB（年付 $49.99）是最便宜的入门款。如果对延迟有极致要求且预算充足，香港 CN2 GIA 是顶配选择。
