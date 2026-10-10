***

## 1. 项目信息

- **参考脚本**：<https://github.com/ZqinKing/wrt_release.git>
- **源码来源**：<https://github.com/VIKINGYFY/immortalwrt.git> - main
- **设备支持**：Link\_NN6000V2，内核分区 12m（固件包含带 WiFi 和不带 WiFi 版本）
- **固件发布**：[点击下载](https://github.com/zk6685/zk_NN6000-12m/releases/latest)
- **包 管 理**：2026-10-09 已经切换到APK，不在支持IPK。
- **Build by**：zk6685

***

## 2. 固件配置

### 2.1 系统配置

| 配置项          | 默认值         | 说明                                       |
| ------------ | ----------- | ---------------------------------------- |
| **LAN IP**   | `10.0.0.1`  | (nn6000v2/scripts/update.sh) |
| **WiFi 名称**  | `500/5`     | (nn6000v2/patches/992\_network\_config.sh) |
| **WiFi 密码**  | `147258369` | 无线密码                                     |
| **WiFi 状态**  | **禁用**      | 首次启动需手动开启                                |
| **PPPoE 账号** | **未配置**     | (nn6000v2/patches/992\_network\_config.sh)    |
| **PPPoE 状态** | **自动拨号**    | 配置账号密码后自动拨号，无需手动开启                                 |

***

### 2.2 预装插件（32 个）

| 插件名称                     | 功能说明          |
| ------------------------ | ------------- |
| **luci-app-argon**       | Argon 主题      |
| **luci-app-istorex**     | 应用商店          |
| **luci-app-dockerman**   | Docker        |
| **luci-app-adguardhome** | 广告过滤          |
| **luci-app-mini_diskmanager**     | 磁盘管理          |
| **luci-app-smartdns**    | DNS 加速        |
| **luci-app-autoreboot**  | 定时重启          |
| **luci-app-sqm**         | QoS 智能队列      |
| **luci-app-upnp**        | UPnP 端口映射     |
| **luci-app-hd-idle**     | 硬盘休眠          |
| **luci-app-p910nd**      | USB 打印机共享     |
| **luci-app-tailscale-community**    | Tailscale 虚拟组网 |
| **luci-app-zerotier**    | ZeroTier 虚拟组网 |
| **luci-app-lucky**       | 多功能网络代理插件            |
| **luci-app-oaf**         | 应用过滤-默认禁用        |
| **luci-app-ttyd**        | 终端            |
| **luci-app-quickfile**   | 文件管理          |
| **luci-app-samba4**      | SMB 文件共享      |
| **luci-app-pbr**         | 策略路由          |
| **luci-app-passwall**    | 科学上网          |
| **luci-app-daed**        | eBPF 高性能透明代理（dae Web 面板版） |
| **luci-app-nikki**       | Mihomo/Clash Meta 代理 |
| **luci-app-openclash**   | OpenClash 代理  |
| **luci-app-mosdns**      | DNS 分流转发      |
| **luci-app-gecoosac**    | 集客无线 AC 控制器 |
| **luci-app-mosquitto**   | MQTT 消息 Broker（含 SSL） |
| **luci-app-vlmcsd**      | KMS 激活服务器    |
| **luci-app-openlist2**   | OpenList 网盘挂载  |
| **luci-app-filebrowser-go** | File Browser 文件管理（Go 版） |
| **luci-app-clouddrive2** | CloudDrive2 网盘挂载（二进制版） |
| **zram-swap**            | ZRAM 内存压缩交换  |
| **luci-app-cpufreq**     | CPU 频率调节     |

***

## 3. 插件来源

- 官方 feed：<https://github.com/VIKINGYFY/immortalwrt>
- 部分插件源自：<https://github.com/kenzok8/openwrt-packages>
- daed：<https://github.com/kenzok8/openwrt-daede>
- gecoosac：<https://github.com/laipeng668/luci-app-gecoosac>
- openlist2/filebrowser-go/mosdns/clouddrive2：<https://github.com/xuanranran/openwrt-packages>
- nikki：<https://github.com/nikkinikki-org/OpenWrt-nikki>
- openclash：<https://github.com/vernesong/OpenClash>

***

## 4. 项目结构

```
zk_NN6000-12m/
└── nn6000v2/              # 设备专用目录
    ├── configs/           # 固件配置文件目录
    ├── patches/           # 设备补丁目录
    │   ├── cpuusage       # CPU 使用率补丁
    │   ├── hnatusage      # HNA 使用率补丁
    │   ├── smp_affinity   # SMP 中断平衡补丁
    │   └── tempinfo       # 温度信息补丁
    └── scripts/           # 编译脚本目录
        ├── build.sh       # 编译脚本
        ├── feeds.sh       # feeds 配置脚本
        ├── general.sh     # 通用设置脚本
        ├── packages.sh    # 包管理脚本
        ├── system.sh      # 系统配置脚本
        └── update.sh      # 更新脚本
```

***

## ImmortalWrt

<div align="center">

![ImmortalWrt](immortalwrt.png)

</div>

***
