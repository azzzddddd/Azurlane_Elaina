<details>
<summary>中文安装说明 - 点击展开</summary>

1. 在下方列表中找到你需要的版本前缀，下载该服务器名称前缀的所有以 `7z.00*` 结尾的分卷文件。
2. 解压时，只需要右键选择 `XXX.7z.001` 进行解压，解压软件会自动处理后续分卷。
3. 在解压后的文件夹中找到对应的安装包并安装（具体安装方法请自行查阅相关教程）。

</details>

<details>
<summary>English Installation Instructions - Click to expand</summary>

1. Find the version prefix you need in the list below, and download all files ending with `7z.00*` that share the same server name prefix.
2. When extracting, simply select the `XXX.7z.001` file to decompress, and the software will automatically process the rest of the volumes.
3. Find the installation package in the extracted folder and install it (please refer to relevant tutorials for installation methods).

</details>

<details>
<summary>📝 更新日志 / Changelog - 点击展开</summary>

# 3.7.0 更新日志

本版本由 3.6.0 升级而来，主要变化是新增了一整套「自动任务」功能，以及对循环模式、皮肤穿戴等已有功能的优化。

## 一、新增功能

### 【自动领取资源（AutoClaim）】
#### 开启位置：Tasks → AutoClaim（默认关闭）
* 登录游戏后自动领取「食堂」的石油、「小卖部」的物资、「讲堂」的学院资源。
* 全程自动完成，不需要你打开任何界面，也不用点一下。
* 资源已经满了会自动跳过，不会白白操作一次。
* 与任务总开关 Tasks.Enabled 配合使用。

### 【自动委托（AutoDelegation）】
#### 开启位置：Tasks → AutoDelegation（默认关闭）
* 自动领取已经完成的委托。
* 领取完成后，按优先级自动派出新的委托，并自动使用推荐的舰船编队。
* 可单独设置委托的优先顺序：Tasks.AutoDelegationPriority
  默认顺序为：日常活动 → 钻石(8小时) → 钻石(4小时) → 钻石(2小时) → 魔方 → 大型委托 → 日常芯片 → 日常资源 → 其他。
* 可单独设置是否派发大型委托：Tasks.AutoDelegationDoMajor（默认关闭）。

### 【自动科研（AutoResearch）】
#### 开启位置：Tasks → AutoResearch（默认关闭）
* 自动领取已经完成的科研项目。
* 自动开始新项目、自动把项目加入队列。
* 五个队列槽位全部占满后，还会额外启动一个未排队的项目；该项目完成后再自动接上一个，如此循环。
* 项目选择按主流的科研优先级，石油与金币的消耗也会自动判断。
* 需要时会自动刷新科研列表（会消耗物资）。
* 与自动委托互不影响，可以只开其中一个。

### 【任务奖励自动领取（AutoClaimMissions）】
#### 开启位置：Tasks → AutoClaimMissions（默认关闭）
* 自动领取任务、每周任务的奖励。
* 会自动跳过「需要你自己选择奖励」的任务。
* 也会跳过领取后会弹出「仓库已满」确认框的任务，避免流程卡住。

### 【自动退役（AutoRetire）】
#### 开启位置：Tasks → AutoRetire（默认关闭）
* 船坞满员时自动退役，选船规则完全按照你在游戏里保存的「一键退役」设置来。
* 稀有度、等级、满星保留、数量上限等，全部沿用你自己的游戏设置。
* 不打开任何界面，也不会在你正在查看舰船、或者刚获得新船的时候动手。
* 退役前会做安全检查，不会误删有价值的舰船；退役后装备会自动回到仓库。

### 【每日任务自动完成（AutoDailyLevel）】
#### 开启位置：Tasks → AutoDailyLevel（默认关闭）
* 登录后自动完成当天开放的每日任务：
  商船护送、海域突进、斩首行动、破交作战、战术研修、兵装训练。
* 自动选择你能打的最高难度。
* 只在已经满足「快速战斗」条件的关卡上执行，不会占用你的正常出击。
* 已经过期、或者属于活动页面的条目会自动跳过。
* 周常任务（破交作战、兵装训练）也会按次数自动完成。

### 【战术学院自动管理（AutoTactics）】
#### 开启位置：Tasks → AutoTactics（默认关闭）
* 自动领取已经学完的课程。
* 自动安排下一门课程：刚学完的舰船会继续学它的下一个技能。
* 教室空出来后，会自动安排新舰船进来学习。
* 自动使用匹配的教材，优先选择与技能类型对应、等级更高的教材。
* 快要满级时会自动避免经验浪费，改用更合适的教材。
* 不会选择：正在学习的舰船、META 舰船、活动 NPC 舰船、展示舰。
* 附加设置：
  * Tasks.AutoTacticsAddNewShip（默认开启）：是否自动安排新舰船进教室。
  * Tasks.AutoTacticsMinShipLevel（默认 50）：自动挑选舰船时的最低等级。

### 【三星关卡自动完成（ThreeStarStages）】
#### 开启位置：Misc → ThreeStarStages（默认关闭）
* 需要同时开启 Misc.LoopModeUnlock。
* 自动优先处理关卡里还没完成的三星目标：全歼敌人、击败护卫舰队、击败旗舰。
* 只调整移动路线，不会直接修改成就或通关数据。
* 适合用来补齐那些已经通关、但三星目标还没做完的关卡。
* 三星已达成的关卡不会修改移动路线。

### 【自动跳过剧情（SkipStory）】
#### 开启位置：Misc → SkipStory（默认关闭）
* 自动跳过所有剧情和对话，不用再手动点跳过。
* 覆盖全部剧情形式：对话、CG、视频、旁白、轮播等。
* 剧情奖励、分支选择、剧情更新记录都照常生效，不会漏内容。
* 受总开关 Misc.Enabled 影响：需要同时开启 Misc.Enabled 与 Misc.SkipStory 才会生效。

### 【演习场专属功能】
* 演习无敌：Misc → ExerciseGodmode（默认关闭）
  演习中我方舰船不会掉血。
* 演习敌人无技能：Misc → ExerciseEnemyNoSkill（默认关闭）
  演习中敌人不会释放技能、也不会获得增益。
* 演习伤害倍率：Misc → ExerciseDamageMul（默认 1.0，即关闭）
  可以调整你对敌人造成的伤害。
* 以上功能只在演习场生效，推图、活动等玩法完全不受影响。
* 感谢Van提供源码

### 【秒杀生效范围可自定义】
#### 开启位置：Enemies → InstakillBattleTypes
* 默认值："1,2,3,8,9,15,16,17,51"
* 可以用一串编号，指定「秒杀」在哪些战斗类型里生效。
* 每个编号对应的关卡如下：

  编号|   对应关卡|
  ---- |  ------------------------------------|
  1     | 主线关卡（主线章节图）|
  2     | 日常关卡（每日任务里的关卡）|
  3    |  演习（竞技场）|
  8     | 活动世界BOSS关|
  9     | 共斗活动世界BOSS关（血量共享）|
  15    | 活动BOSS SP关|
  16    | 单体BOSS关|
  17    | 可变单体BOSS关|
  51   |  大世界（大型作战）|

* 想让秒杀在所有战斗中都生效，直接填 *
* 想在演习场里关闭秒杀，把列表里的 3 去掉即可（例如改成 "1,2,8,9,15,16,17,51"）。

---

## 二、功能优化

### 【新增任务总开关 Tasks】
* 新增顶层 Tasks 区块，Tasks.Enabled 是任务类功能的总开关。
* 包含：自动领取、自动委托、自动科研、任务奖励领取、每日任务、战术学院、自动退役。
* 从旧版本升级时，你原来的设置会自动迁移过去，不会丢失。

### 【皮肤商店穿戴优化】
* 皮肤商店点击「穿戴」后，会打开官方的换装页面，由你自己选择要穿到哪艘船上。
* 修复了换装页面偶尔打不开的问题。

### 【循环模式修复】
* 修复了进入关卡后，舰队任务选择（例如「第一舰队全歼」）被重置回默认的问题。
* 进度已经 100% 的关卡改用游戏官方的循环流程，运行更加稳定。

### 【后台任务自动重试】
* 任务类功能现在每小时会随机在 55~65 分钟之间重新检查一次。
* 即使某次刷新被错过，也能在之后自动补上。

### 【功能调整与移除】
* 移除了旧版「船坞满自动退役」的界面操作方案，以及配套的自动确认选项。
* 由全新的自动退役功能取代，更安全，也不会干扰你的正常操作。

---

## 三、配置说明

所有功能都可以在 Elaina.json 中开关。

任务类功能统一放在 Tasks 区块：

```json
"Tasks": {
    "Enabled": false,
    "AutoClaim": false,
    "AutoDelegation": false,
    "AutoDelegationPriority": "DailyEvent > Gem-8 > Gem-4 > Gem-2 > Cube > Major > DailyChip > DailyResource > Other",
    "AutoDelegationDoMajor": false,
    "AutoResearch": false,
    "AutoClaimMissions": false,
    "AutoDailyLevel": false,
    "AutoTactics": false,
    "AutoTacticsAddNewShip": true,
    "AutoTacticsMinShipLevel": 50,
    "AutoRetire": false
}
```

其他功能放在 Misc 区块：

```json
"Misc": {
    "Enabled": false,
    "ExerciseGodmode": false,
    "ExerciseEnemyNoSkill": false,
    "ExerciseDamageMul": 1.0,
    "SkipStory": false,
    "LoopModeUnlock": false,
    "ThreeStarStages": false
}
```

战斗相关：

```json
"Enemies": {
    "InstakillBattleTypes": "1,2,3,8,9,15,16,17,51"
}
```

## 提示：
* 如果你是从旧版本升级，Elaina.json 会自动补齐这些新选项，原有设置不会丢失。
* 如果出现异常，把 Elaina.json 删除后重启游戏，即可恢复默认配置。

- **[新增]** “文件提供器”（File Provider），方便免 Root 用户修改文件。
- **[New]** Added "File Provider", making it easier for non-root users to modify files.

### 🪄使用方法
- [注入文件提供器](https://mt2.cn/guide/reverse/inject-documents-provider.html#%E6%B7%BB%E5%8A%A0%E6%9C%AC%E5%9C%B0%E5%AD%98%E5%82%A8)
- [Data Files Provider](https://mt2.cn/guide/reverse/inject-documents-provider.html#%E6%B7%BB%E5%8A%A0%E6%9C%AC%E5%9C%B0%E5%AD%98%E5%82%A8)

</details>
