## 概述

###### MacOS ：Ventura 13 beta1

###### Opencore ：0.8.2

###### 更新日期 ：2022-06-18

## 配置

| 项目             | 型号                  |
| :--------------- | --------------------- |
| CPU              | AMD Ryzen 5 3600      |
| motherboard主板  | MSI B450M mortar max |
| GPU             | 蓝宝石 RX 460 4 GB    |
| WLAN/Bluetooth  | 博通 BCM94360 2CS     |
| Ethernet       |  Realtek RTL8111       |

## 截图展示
![about this mac](https://s3.bmp.ovh/imgs/2022/06/18/644508e6070ba40b.png)
![airdrop](https://s3.bmp.ovh/imgs/2022/06/18/c83bb4b9920a223f.png)
![](https://s3.bmp.ovh/imgs/2022/06/18/84b2ac1481bc54db.png)
![](https://s3.bmp.ovh/imgs/2022/06/18/97f46e93ec16f842.png)

## tips 使用提示

1. ###### 三码替换

   我使用的SMBIOS为Mac Pro7，1，安全起见，强烈建议替换三码。

   路径为：config.plist - > PlatformInfo -> Generic

   | 条目               | 内容                                 |
   | ------------------ | ------------------------------------ |
   | SystemSerialNumber | C02ZVKYAJV3Q                         |
   | MLB                | C02951600CDLNV91M                    |
   | SystemUUID         | 4284E229-FA9D-41EA-BC67-C627363F80BD |

   附上[替换教程](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html)

2. ###### kexts

   建议根据自己的机器，替换部分kext，以达到最佳设置。

   USBMap.kext ：用于识别USB接口，这是我个人的USB定制，不一定适合所有人，最好自己定制；

3. ###### 声音

   声卡驱动AppleALC默认使用layout-id=18，若音频异常，可自行替换layout-id。

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
  8. Final Cut Pro / Photoshop / PyCharm
