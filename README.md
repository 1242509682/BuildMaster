## 插件说明
```
作者：豆沙  
修改：羽学  
源码地址：https://www.bbstr.net/r/117/  

这是一个Tshock服务器插件主要基于：  
MiniGamesAPI框架开发，
它的玩法类似于MC中的小游戏(速建大比拼)。
玩家将需要在一定时间内完成相对应主题的建筑，时间到后将由每位玩家进行评分，
得分会在游戏结束后进行一个排名。快来发挥你的想象力，把建筑搞起来！
注意：该插件必须依赖于MiniGamesAPI运行


```

## 插件版本
```
更新日志  
v1.0:  
适配Tshock 5.2.0
```
## 命令
```
/bm list 查看房间列表  
/bm join [房间ID] 加入房间  
/bm leave 离开房间  
/bm ready 准备/未准备  
/bm vote [主题] 投票主题  

/bma list 列出所有房间  
/bma create [房间名] 创建房间  
/bma remove [房间ID] 移除指定房间  
/bma start [房间ID] 开启指定房间  
/bma stop [房间ID] 关闭指定房间  
/bma smp [房间ID] [人数] 设置房间最大玩家数  
/bma sdp [房间ID] [人数] 设置房间最小玩家数  
/bma swt [房间ID] [时间] 设置等待时间(单位：秒)  
/bma sgt [房间ID] [时间] 设置游戏时间(单位：秒)  
/bma sst [房间ID] [时间] 设置评分时间(单位：秒)  
/bma sp [1/2] 选取点1/2  
/bma sr [房间ID] 设置房间的游戏区域  
/bma addt [房间ID] [主题名] 添加主题  
/bma sh [房间ID] [高] 设置小区域高  
/bma sw [房间ID] [宽] 设置小区域宽  
/bma sg [房间ID] [间隔] 设置小区域间隔  
/bma dp [玩家名字] 设置基础建造背包  
/bma ep 设置评分套装  
/bma reload 重载配置文件非房间文件  
```
## 权限
```
bm.user  
bm.admin  
```
## 权限示例
```
/group addperm default bm.user  

```

## 配置示例
```json
Config.json  
  
{
  "UnlockAll": true,
  "Range": {},
  "BanItem": []
}
```
```json
default.json  

{
  "Name": "基础套",
  "ID": 2,
  "UnlockedBiomeTorches": 0,
  "HappyFunTorchTime": 0,
  "UsingBiomeTorches": 0,
  "QuestsCompleted": 0,
  "HideVisuals": [
    false,
    false,
    false,
    false,
    false,
    false,
    false,
    false,
    false,
    false
  ],
  "EyeColor": {
    "packedValue": 4283128425,
    "R": 105,
    "G": 90,
    "B": 75,
    "A": 255,
    "PackedValue": 4283128425
  },
  "SkinColor": {
    "packedValue": 4284120575,
    "R": 255,
    "G": 125,
    "B": 90,
    "A": 255,
    "PackedValue": 4284120575
  },
  "ShoeColor": {
    "packedValue": 4282149280,
    "R": 160,
    "G": 105,
    "B": 60,
    "A": 255,
    "PackedValue": 4282149280
  },
  "UnderShirtColor": {
    "packedValue": 4292326560,
    "R": 160,
    "G": 180,
    "B": 215,
    "A": 255,
    "PackedValue": 4292326560
  },
  "ShirtColor": {
    "packedValue": 4287407535,
    "R": 175,
    "G": 165,
    "B": 140,
    "A": 255,
    "PackedValue": 4287407535
  },
  "HairColor": {
    "packedValue": 4287407535,
    "R": 175,
    "G": 165,
    "B": 140,
    "A": 255,
    "PackedValue": 4287407535
  },
  "PantsColor": {
    "packedValue": 4287407535,
    "R": 175,
    "G": 165,
    "B": 140,
    "A": 255,
    "PackedValue": 4287407535
  },
  "Hair": 0,
  "SkinVariant": 0,
  "ExtraSlots": 0,
  "SpawnY": -1,
  "SpawnX": -1,
  "Exists": true,
  "MaxMana": 20,
  "Mana": 20,
  "MaxHP": 100,
  "HP": 100,
  "HairDye": 0,
  "Items": []
}
```
```json
eva.json

{
  "Name": "评分套",
  "ID": 3,
  "UnlockedBiomeTorches": 0,
  "HappyFunTorchTime": 0,
  "UsingBiomeTorches": 0,
  "QuestsCompleted": 0,
  "HideVisuals": [
    false,
    false,
    false,
    false,
    false,
    false,
    false,
    false,
    false,
    false
  ],
  "EyeColor": {
    "packedValue": 4283128425,
    "R": 105,
    "G": 90,
    "B": 75,
    "A": 255,
    "PackedValue": 4283128425
  },
  "SkinColor": {
    "packedValue": 4284120575,
    "R": 255,
    "G": 125,
    "B": 90,
    "A": 255,
    "PackedValue": 4284120575
  },
  "ShoeColor": {
    "packedValue": 4282149280,
    "R": 160,
    "G": 105,
    "B": 60,
    "A": 255,
    "PackedValue": 4282149280
  },
  "UnderShirtColor": {
    "packedValue": 4292326560,
    "R": 160,
    "G": 180,
    "B": 215,
    "A": 255,
    "PackedValue": 4292326560
  },
  "ShirtColor": {
    "packedValue": 4287407535,
    "R": 175,
    "G": 165,
    "B": 140,
    "A": 255,
    "PackedValue": 4287407535
  },
  "HairColor": {
    "packedValue": 4287407535,
    "R": 175,
    "G": 165,
    "B": 140,
    "A": 255,
    "PackedValue": 4287407535
  },
  "PantsColor": {
    "packedValue": 4287407535,
    "R": 175,
    "G": 165,
    "B": 140,
    "A": 255,
    "PackedValue": 4287407535
  },
  "Hair": 0,
  "SkinVariant": 0,
  "ExtraSlots": 0,
  "SpawnY": -1,
  "SpawnX": -1,
  "Exists": true,
  "MaxMana": 20,
  "Mana": 20,
  "MaxHP": 100,
  "HP": 100,
  "HairDye": 0,
  "Items": []
}
```
```json
rooms.json

[]
```
