# XG All Phone v1.7

1462 款手机数据库（2012–2026）· 网页版 / Android APK / Windows EXE 三端，数据一致。
1462-phone database (2012–2026) · Web / Android APK / Windows EXE, same data on all three builds.

## 这是什么 / What is this
一款离线手机参数库与对比工具：型号库浏览、芯片天梯榜、权威对比台、AI 直达、智能一键录入。
An offline phone-spec library and comparison tool: model browser, chip ranking, Pro compare bench, AI shortcuts, smart quick-entry.

## 文件与用法 / Files & How to Use

| 文件 File | 说明 / Description | 用法 / Usage |
|---|---|---|
| `XG All Phone.html` | 中文网页版（离线内嵌，无需联网）/ Chinese web version, fully offline | 双击用浏览器打开 / Double-click to open in a browser |
| `XG All Phone EN.html` | 英文界面版（数据与中文版相同）/ English UI version, same data | 双击用浏览器打开 / Double-click to open in a browser |
| `XG All Phone.apk` | Android 安装包（com.xg.allphone, 已签名）/ signed APK | 传到手机安装 / Install on Android |
| `XG All Phone.exe` | Windows 桌面版（.NET8 单文件, WebView2, Win-x64）/ desktop build | 双击运行，需 WebView2 / Run; needs WebView2 runtime |
| `data/XG手机数据库_校对版_2012-2026.json` | 主数据库（1462 台）/ master database | 供构建与备份 / build & backup |

## 功能 / Features
- **型号库 Models**：按品牌/系列浏览，搜索框支持品牌+型号联合匹配。
- **芯片榜 Chips**：芯片天梯排名，按厂商筛选，查看搭载机型。
- **⚖️ Compare 对比**：最多 3 台手机 / 3 颗芯片同框，逐项标优、量化评分、八维雷达、分场景推荐。
- **AI Shortcuts**：直达常用 AI 站点。
- **🪄 Smart quick-entry**：粘贴文字自动识别机型/芯片参数，核对后写入。

## 数据说明 / Data Notes
- 照片离线内嵌，无外链；未补照片的机型显示灰色占位图。
- 未联网核实的参数按规则留空，不编造；海外版/Lite/T 系列无国行首发价，价格留空。
- 界面中文版与英文版数据完全相同，仅界面语言不同。

## 在线访问 / Online Access
- 中文网页（浏览器直接打开）/ Chinese web, open directly in browser: https://raw.githubusercontent.com/XweXG/XG-All-Phone/main/XG_All_Phone.html
- 英文界面版 / English UI: https://raw.githubusercontent.com/XweXG/XG-All-Phone/main/XG_All_Phone_EN.html

## 下载 / Downloads
- GitHub Release（APK + EXE 直链 / direct links）: https://github.com/XweXG/XG-All-Phone/releases/tag/v1.7
- Windows EXE (390MB) 飞书 / Feishu: https://my.feishu.cn/file/MaC1btCHJo3rwMxuwkfcRK3Tnfh
- 轻量包（含 APK 与网页版 / APK and web）飞书 / Feishu: https://my.feishu.cn/file/M4IdbPkOxoQIiVxo95WcBbwYn1g
- 蓝奏云小包 / Lanzou: https://wwayi.lanzoum.com/isC4V4gwjajg （密码 / password: 9miw）

## 重建（开发）/ Rebuild (dev)
1. `python src/build_final_html.py` 生成 HTML / build HTML
2. `python src/verify_final_html.py` 校验 / verify
3. `python src/build_apk.py` 重打 APK / repackage APK
4. `dotnet publish XGAllPhone.csproj` 重打 EXE / repackage EXE
