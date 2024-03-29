## **OpenWrt下载说明**
- 可在 [Cloud-Openwrt](https://openwrt.115115.xyz/)下载    `VMDK` 虚拟磁盘文件
- 可直接使用系统内置的更新功能，可任意切换版本
- 文档参见： [帮助文档](https://openwrt.115115.xyz/doc)
## **发行说明**
1. 本项目集成了更新功能，让更新更便捷！
2. 默认IP：`192.168.2.200`，用户名： `root` 密码：`password`
3. `X` 版本（大全版）： `Dockerman Smartdns HelloWorld Clash Passwall AdGuardHome` 等以及更多主题
4. `Y` 版本（适中版）： 基础包、常用软件及 `Docker`
6. `Z` 版本（极简版) ： 基础包及 `Smartdns Passwall AdGuardHome`
7. 可修复 `Docker` 对 `udp` 的影响
8. 默认 `rom` 分区大小为 `800M`，`Boot` 分区为`32M`。如果自行对路由器分区后请勿随意不同的发行版本，注意确认 `rom` 分区和 `Boot` 分区一致，否则会导致丢失硬盘其余分区数据。同一发行版本请放心更新、升级
9. 本项目 `X` `Y` 版本使用 `5.10` 内核，  `Z` 版本使用 `5.4` 内核。
10. 本镜像基于 ：[AutoBuild-Action](https://github.com/Hyy2001X/AutoBuild-Actions) 项目，特别感谢!
11. 代码调试仓库为：[AutoBuild-Action](https://github.com/kokeri/AutoBuild-Actions/)

## **Tips**
由于编译Docker可能导致tproxy透明代理失效，可在` /etc/sysctl.conf `文件中加入 

`net.bridge.bridge-nf-call-ip6tables = 0`

`net.bridge.bridge-nf-call-iptables = 0`

后执行 `sysctl -p` 修复，注意，此步骤会导致 Docker 内部无法正常 DNS 解析，需要手动下发默认 DNS 服务器。

## **更新日志**

### **X-OpenWrt 2024**

务必更新至此版本，以保证网络安全。

- 20231211：1、弃用passwall，使用passwall2。2、使用AdguardHome官方发行v0.107.36，自己不编译，更稳定。3、修复一个ttyd致命安全漏洞。4、网易云音乐解锁使用`golang`版本，大幅降低编译时间。

### **X-OpenWrt 2023**
- 20211217：版本发行！详情可至 [OpenWrt X](https://www.115115.xyz) 查看
- 20211218：添加 `Y` 版本，在 `Z` 版本基础上含有 `Dockerman` 及一些常用程序。调整软件包。
- 20211222：例行更新！
- 20211224：修复 `NetData` 显示错误
- 20211225：修复 `NetData` 显示错误
- 20211230：`2021` 年的最后一版，全部采用 `5.10` 内核。更新至 `R22.1.1`
- 20220101：`2022` 新年快乐！
- 20220205：`牛辞胜岁 虎跃新程` 经过一些挫折，继续更新。优化显示，更新组件！无 `netdata`！`kernel 5.10.96`
- 20220206：`牛辞胜岁 虎跃新程` 经过一些挫折，继续更新。优化显示，更新组件！无 `netdata`！`kernel 5.10.96`
- 20220207：添加虚拟内存设置，增加 `WebDav` . 版本更新保留 `known_hosts` , `htop` 配置, 修复一些显示错误, 将 netdate 设置为默认版本
- 20220213: 更新至 `R22.2.2`
- 20220218: 例行更新
- 20220228: 全部切换至 `5.10` 内核。更新至 `R22.1.1`
- 20220307: 例行更新
- 20220308: 例行更新
- 20220315: 更新至 `R22.3.13`
- 20220322: 例行更新
- 20220327: 添加 `luci-theme-neobird` 主题, `x86` 支持 `Intel 3165 2.5G wifi`. , 添加支持 `N1` 盒子!
- 20230314: `X` 添加更多 `Intel` 网卡支持，内核更新至 `5.15.98`。`LEDE` 更新至 `R23.3.3`。`Passwall` 支持 `Xray-core 1.8.0`，支持 `Reality H2`。
- 20230430: 添加全新的主题`Edge`，内核依旧为`5.15`，LEDE正常迭代。修复了部分小bug。
