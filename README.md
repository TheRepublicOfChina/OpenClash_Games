# OpenClash游戏分流规则

本项目基本在香港、台湾等国家的全局代理环境下抓的游戏IP，不保证其它国家同样适用。

战地5亚服：Battlefield V(Asia)

英雄联盟台服、金铲铲手游台服(Teamfight Tactics)：League of Legends(TW)

手游绝地求生亚服：PUBG MOBILE(Asia)

绝地求生亚服：PUBG(Asia)

用法：

在openclash配置文件中

rules段添加：
```yaml
  - RULE-SET,PUBG-Asia,🎮 游戏加速
  - RULE-SET,Battlefield_V-Asia,🎮 游戏加速
  - RULE-SET,League_of_Legends-TW,🎮 游戏加速
  - RULE-SET,PubgMobile-Asia,🎮 游戏加速
```
rule-providers段添加：
```yaml
  PUBG-Asia:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/TheRepublicOfChina/OpenClash_Games/main/PUBG-Asia.yaml"
    path: ./ruleset/PUBG-Asia.yaml

  PubgMobile-Asia:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/TheRepublicOfChina/OpenClash_Games/main/PubgMobile-Asia.yaml"
    path: ./ruleset/PubgMobile-Asia.yaml

  Battlefield_V-Asia:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/TheRepublicOfChina/OpenClash_Games/main/Battlefield_V-Asia.yaml"
    path: ./ruleset/Battlefield_V-Asia.yaml

  League_of_Legends-TW:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/TheRepublicOfChina/OpenClash_Games/main/League_of_Legends-TW.yaml"
    path: ./ruleset/League_of_Legends-TW.yaml
```

