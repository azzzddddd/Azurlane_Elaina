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

### 一、新功能

【自定义帧率上限】
配置项：Misc.FPS（数字）
· 设为 0：保持游戏原版 30 / 60 帧选项
· 设为大于 0 的数值（如 90、120、144）：可突破 60 帧上限
· 需同时开启 Misc.Enabled

【随机秘书组 × 展示舰】
· 展示舰可参与「常用角色」「锁定角色」「自定义秘书组」三种随机模式
· 常用 / 锁定标记会本地保存，重启后仍然有效
· 自定义随机秘书组编辑界面可显示全部展示舰及特殊秘书舰，并支持加入秘书组

【秘书舰优化（optimizeSecretary）】
· 新增主界面秘书舰加载缓存优化
· 开启后可减少动态立绘与 Live2D 切换时的卡顿和闪烁，整体切换更加流畅

【皮肤功能增强】
· 开启 Skins 后，特殊秘书舰的全部外形模块视为已解锁
· 无需完成对应养成进度、结局或商店条件即可切换外形
· 优化皮肤商店的试穿、预览和穿戴流程

【自定义加载界面】
· 可在 Elaina.json 同目录新建「Loading Screen」文件夹，放入本地图片作为加载背景
· 支持随机切换，并保持图片原始比例不变形
· 支持通过 URL 获取自定义加载图，并缓存到本地
· URL 图片不可用时会自动回退到本地加载图或官方默认加载图

---

### 二、功能优化

【展示舰 / 全舰娘预览】
· 舰坞中展示舰排序更加稳定，已拥有舰娘始终排在展示舰上方
· 优化秘书位、详情页左右滑动、换肤后的即时刷新体验

【秘书组】
· 展示舰担任秘书时，切换回普通舰娘后不再被旧数据覆盖
· 重新登录、返回主界面时，随机秘书组可正确识别本地保存的展示舰
· 随机秘书组开启 / 关闭与官方流程兼容，不影响每日定时更换

【循环模式（LoopModeUnlock）】
· 恢复并稳定了未完成章节的本地循环模式相关能力
· 减少对主线困难编队界面的误干扰，困难本编队体验更加稳定
· 优化活动关卡循环时的无效操作处理

【困难模式限制解除（RemoveHardModeStatLimit）】
· 优化实现方式，在解除属性限制的同时尽量不影响困难本编队界面正常显示
· 保持主线困难模式正常运行
· 活动关卡困难限制解除更加完整
· 优化与循环模式的兼容性，减少无效操作提示

【稳定性与兼容性】
· 修复多处因展示舰数据与舰坞、仓库、编队界面交叉导致的闪退或界面异常
· 优化 DEBUG 日志开关，默认关闭时不产生调试文件，减轻性能开销
· 持续修复展示舰误入普通编队、困难本空白舰队等边界问题
· 改善登录、切换秘书舰、切换皮肤、进入详情页等常用流程的兼容性

【特殊秘书舰】
· 新增 SpecialSecretary.json，用于独立保存特殊秘书舰外形选择
· 重新登录后可安全恢复保存的特殊秘书舰外形

【展示舰 / 随机秘书组】
· 添加 / 删除确认弹窗不再显示白色空白舰娘卡片
· 展示舰参与随机秘书组时，重登、切换及确认弹窗显示更加稳定

【主界面与舰坞体验】
· 主界面长按展示舰秘书时，可直接进入对应舰娘详情，不再进入默认详情后无限加载
· 优化换肤、隐藏背景及返回主界面后的刷新表现

---

### 三、配置说明

在 Elaina.json 的 Misc 区块中：

```json
"FPS": 0
```

自定义帧率上限，0 为关闭。

```json
"Skins": false
```

开启后可解锁特殊秘书舰外形。

```json
"UnlockAllShips": false
```

展示舰相关功能总开关。

```json
"CustomLoadingScreen": false
```

启用自定义加载界面。

```json
"optimizeSecretary": false
```

启用主界面秘书舰加载缓存优化。
随机秘书组相关的展示舰常用、锁定及自定义列表保存在 `UnlockAllShips.json` 中，无需手动编辑。

- **[新增]** “文件提供器”（File Provider），方便免 Root 用户修改文件。
- **[New]** Added "File Provider", making it easier for non-root users to modify files.

### 🪄使用方法
- [注入文件提供器](https://mt2.cn/guide/reverse/inject-documents-provider.html#%E6%B7%BB%E5%8A%A0%E6%9C%AC%E5%9C%B0%E5%AD%98%E5%82%A8)
- [Data Files Provider](https://mt2.cn/guide/reverse/inject-documents-provider.html#%E6%B7%BB%E5%8A%A0%E6%9C%AC%E5%9C%B0%E5%AD%98%E5%82%A8)

</details>