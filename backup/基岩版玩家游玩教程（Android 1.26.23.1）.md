## 一、版本与设备要求

本服务器的基岩版固定使用：

- Minecraft Bedrock `1.26.23.1`
- 安卓 `arm64-v8a` 版本
- Android 8.0 或更高版本
- 安装包大小：`660316388` 字节（约 630MB）

这个安装包只能用于 64 位 ARM 安卓手机和平板。Intel/x86 设备、32 位 ARM 设备以及 Windows、iPhone/iPad 不能安装此 APK。

## 二、下载安装包

### 国内加速下载

[下载 Minecraft PE 1.26.23.1 arm64-v8a](https://gh-proxy.com/https://github.com/CSXianShi/CSXianShi.github.io/releases/download/bedrock-1.26.23.1/Minecraft.PE.1.26.23.1.v8a.2.apk)

### GitHub 备用下载

[GitHub Release 原始下载](https://github.com/CSXianShi/CSXianShi.github.io/releases/download/bedrock-1.26.23.1/Minecraft.PE.1.26.23.1.v8a.2.apk)

文件校验值：

```text
SHA256: 3ca6f30695a6ec9c6900fba17cf0e71bec3968b22507c9000d16806dec9f0c1b
```

该文件的包名为 `com.mojang.minecraftpe`，版本号为 `1.26.23.1`。它使用第三方证书重新签名，不是 Microsoft/Mojang 官方商店签名，因此通常不能直接覆盖从应用商店安装的版本。

## 三、安装前备份

如果手机里已经安装过 Minecraft，请先备份世界。卸载旧版本可能同时删除本地世界。

世界文件通常位于：

```text
Android/data/com.mojang.minecraftpe/files/games/com.mojang/minecraftWorlds
```

不同手机系统的文件管理器权限不同。如果无法打开 `Android/data`，可以先在游戏内把重要世界导出为 `.mcworld` 文件。

## 四、安装 APK

1. 下载完成后，在浏览器下载记录或文件管理器中找到 APK。
2. 点击文件，按系统提示允许浏览器或文件管理器“安装未知应用”。
3. 选择“安装”，等待安装完成。
4. 如果提示“应用未安装”或“签名冲突”，先确认世界已经备份，再卸载手机中原有的 Minecraft，然后重新安装此 APK。
5. 如果提示设备不兼容，请确认设备是 64 位 ARM 架构并且系统不低于 Android 8.0。

## 五、首次启动

1. 打开 Minecraft，等待资源初始化完成。
2. 按提示登录 Microsoft/Xbox 账号。
3. 如果多人游戏不可用，请在 Xbox 隐私设置中允许“加入多人游戏”和“与跨平台玩家游玩”。
4. 进入主界面后，确认右下角显示的版本为 `1.26.23.1`。

## 六、添加服务器

1. 点击“游戏”。
2. 打开“服务器”选项卡。
3. 滑到服务器列表底部，点击“添加服务器”。
4. 填写：

```text
服务器名称：生存服
服务器地址：ragame.top
端口：23068
```

5. 保存后点击服务器即可进入。

基岩版必须把地址和端口分开填写，不要在地址输入框中写 `ragame.top:23068`。Java 玩家仍使用 `play.ultra-x.top`。

## 七、首次进入注册

服务器使用 Floodgate 让基岩玩家进入 Java 服务器，同时使用 AuthMe 保护玩家账号。

第一次进入后打开聊天栏，输入：

```text
/register 自定义密码 自定义密码
```

以后进入时输入：

```text
/login 你的密码
```

基岩玩家在服务器内部的名称前会自动带一个英文句点，例如 Xbox 名称是 `Steve`，服务器中可能显示为 `.Steve`。其他玩家使用 `/tpa` 等指令指定你时，需要输入服务器实际显示的完整名称。

## 八、常见问题

### 显示“无法连接到世界”

确认版本为 `1.26.23.1`，地址只填写 `ragame.top`，端口单独填写 `23068`。服务器维护或重启期间请稍后重试。

### 看不到“添加服务器”按钮

部分主机平台会限制自定义服务器。本文提供的 APK 适用于安卓手机和平板；主机玩家需要使用局域网转发或 DNS 工具，操作方式不同。

### 安装时提示签名不一致

这是因为手机里的旧 Minecraft 与该 APK 使用了不同签名。备份世界后卸载旧版本，再安装固定版本。

### Java 与基岩玩家能否一起玩

可以。服务器通过 Geyser 和 Floodgate 实现互通，Java 与基岩玩家进入的是同一个世界，可以正常聊天、传送和生存游玩。
