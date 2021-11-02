[点我下载](https://github.com/jeffylong/B450M-Hackintosh/releases/download/oc0.7.4_macOS12.0.1/EFI_B450M_oc0.7.4_macOS12.0.1.zip)
## 概述

###### MacOS ：Monterey 12.0.1

###### Opencore ：0.7.4

###### 更新日期 ：2021-11-02

###### 功能 ：除随航sidecar外均正常



## 配置

| 项目             | 型号                  |
| :--------------- | --------------------- |
| CPU              | AMD Ryzen 5 3600      |
| 主板             | 微星 B450M 迫击炮 max |
| 显卡             | 蓝宝石 RX 460 4 GB    |
| 无线网卡         | 博通 BCM94360 2CS     |
| 板载网卡（有线） | Realtek RTL8111       |


## 使用提示

1. ###### 三码替换

   我使用的SMBIOS为iMac 19,1，安全起见，强烈建议替换三码，修改config.plist。

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

   RealtekRTL8111.kext ： 用于驱动主板的有线网卡，若板载网卡与我配置不同，可替换为相应的。

   

3. ###### 声音

   声卡驱动AppleALC默认使用layout-id=18，若音频异常，可自行替换layout-id。

   [教程](https://dortania.github.io/OpenCore-Post-Install/universal/audio.html)

   [查询可用layout-id](https://github.com/acidanthera/AppleALC/wiki/Supported-codecs)


## 截图展示
![软件](https://s3.bmp.ovh/imgs/2021/11/64cbfc52a577adc6.png)


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



