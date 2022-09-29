## 概述

OpenCore EFI，定期更新，欢迎关注。

## 配置

| 项目             | 型号                  |
| :--------------- | ---------------------|
| CPU              | AMD Ryzen 5 3600     |
| motherboard      | MSI B450M mortar max|
| GPU              | RX460 4GB   |
| WLAN/Bluetooth   | 博通 BCM943602CS    |
| Ethernet         | Realtek RTL8111    |

## 截图展示
![about this mac](https://s3.bmp.ovh/imgs/2022/06/18/644508e6070ba40b.png)
![airdrop](https://s3.bmp.ovh/imgs/2022/06/18/c83bb4b9920a223f.png)
![](https://s3.bmp.ovh/imgs/2022/06/18/84b2ac1481bc54db.png)
![](https://s3.bmp.ovh/imgs/2022/06/18/97f46e93ec16f842.png)

## 使用提示

1. ###### 三码替换

   我使用的SMBIOS为Mac Pro7，1，强烈建议替换三码。
   config.plist - > PlatformInfo -> Generic
   附上[替换教程](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html)

2. ###### kexts

   建议根据自己的机器，替换部分kext，以达到最佳设置。
   USBMap.kext ：用于识别USB接口，这是我个人的USB定制，不一定适合所有人，最好自己定制；

3. ###### 声音

   声卡驱动AppleALC使用layout-id=18，若音频异常，可自行替换layout-id。

   [教程](https://dortania.github.io/OpenCore-Post-Install/universal/audio.html)

   [查询可用layout-id](https://github.com/acidanthera/AppleALC/wiki/Supported-codecs)

## 功能测试

- ❌ 不可用

  1. 随航sidecar
     *因为是amd的cpu，缺少核显，当前版本whatever.kext还不支持强行开启随航，若macOS为10.15，实测可以开启随航，但效果不佳。*   

- ✅ 正常
  1. 隔空投送Airdrop
  2. 接力Handoff
  3. 隔空播放Airplay
  4. Wi-Fi / 蓝牙 / AirPods自动切换
  5. 声音
  6. 睡眠
  7. iCloud服务
