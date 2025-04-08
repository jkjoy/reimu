---
pubDate: "2022-04-12T15:51:00Z"
title: "黑苹果固态避坑指南"
keywords:
  - 分享
tags:
  - 黑苹果
description: "本文是一篇关于黑苹果固态硬盘兼容性的指南。文章列举了一些固态硬盘型号，指出它们在安装和运行macOS时可能会遇到问题。例如，三星PM961 / PM981 / PM981a / PM991和三星983ZET可能导致无法安装或正常运行macOS。然而，一些型号如三星970 EVO Plus在升级官方固件后可以解决兼容性问题。此外，还提到了一些与macOS兼容性不佳的型号，如英特尔600P/660P/760P系列、金士顿A2000、海力士PC601/PC611/PC711/BC501等。文章还提到了一些完全支持macOS的型号，如西部数据SN550/570/730/750/850、三星970EVO/Pro/Plus和980/980 Pro等。最后，文章还提到了一些支持macOS TRIM的型号，如西部数据SN5xx/7xx系列、英睿达Crucial P1 1TB NVME等。对于不支持TRIM的硬盘，建议将SetApfsTrimTimeout值改为0或-1以关闭TRIM功能。"
draft: "false"
---

`三星 PM961 / PM981 / PM981a / PM991` 会导致 macOS 无法安装或正常运行  
`三星 983ZET`无法安装 macOS；

2019 年 5 月以前出厂的 `三星 970 EVO Plus` 可能存在和 PM9x1 系列类似的问题，但可以通过在Windows环境升级官方固件解决 macOS 兼容问题；

`镁光 2200S` 无法安装或稳定运行 macOS；  
`爱国者 P2000 256GB` 无法通过 10.15、11.x、12.x 任何一个版本的正常安装流程，但不排除个例的可能；  
macOS 不支持使用 Intel 傲腾（Optane Memory）或镁光 3D XPoint 进行加速的笔记本电脑；  
下面的型号是与 macOS IONVMeFamily 兼容性不佳的型号（可能无故卡住或运行不正常）  
`英特尔 600P/660P/760P 系列`  
`金士顿 A2000`：配置 S5Z42105 控制器的版本必须搭配 NVMeFix.kext 1.0.8 及以上，也可能完全无法安装；  
`海力士 PC601/PC611/PC711/BC501`：主要见于联想和戴尔笔记本，部分批次正常部分会卡住；  
`技嘉 GIGABYTE M.2 PCIe SSD（比如 GP-GSM2NE8512GNTD）`  
`威刚剑鱼 ADATA Swordfish 2 TB M.2-2280`  
`海力士 SK Hynix HFS001TD9TNG-L5B0B`  
`海力士 SK Hynix P31`  
`镁光 Micron 2200V MTFDHBA512TCK` -`移速的256G`同样使用的镁光颗粒无法安装；  
`阿斯加特 Asgard AN3+ (STAR1000P)`  
`朗科 Netac NVME SSD 480`  
`西部数据 SN550/570/730/750/850` 都能正常安装和运行 macOS；  
`三星 970EVO/Pro/Plus（升级固件后）`和 `980/980 Pro` 都能正常安装和运行 macOS，但是此系列存在 TRIM 支持问题；  
`海盗船 MP400/MP600` 系列均能正常安装运行 macOS；  
绝大部分常见的 SATA 接口固态盘都能正常安装和运行 macOS；  
不完全支持 `TRIM`（主要影响特定条件下的写入速度，什么是 TRIM？），但安装运行正常的型号：  
`三星 Samsung 950 Pro`  
`三星 Samsung 960 Evo/Pro`  
`三星 Samsung 970 Evo/Pro`  
「重要提示」在 macOS 12.0 及以上版本中，OpenCore 无法再修改 APFS 文件系统的 TRIM 超时数值，部分执行 TRIM 相对较慢的固态硬盘（主要是三星的控制器）将没有足够的时间执行 TRIM 操作。不正确的设置可能导致进入系统缓慢，因此对 macOS TRIM 支持度不佳的硬盘建议将 `SetApfsTrimTimeout` 值改成 0 以关闭 TRIM，或 -1 以关闭该功能。此现象在 12.3 及以上的版本中尤其明显。  
完整支持 macOS TRIM 的型号：  
`西部数据 SN5xx/7xx` 系列（未完全测试）  
`英睿达 Crucial P1 1TB NVME（SM2263EN，未完全测试）`  
`金典 KingDian S280（SATA）`  
`浦科特 PLEXTOR M5Pro（SATA）`  
`三星 Samsung 850 PRO`（SATA，未完全测试）  
`三星 Samsung 870 EVO`（SATA，未完全测试）