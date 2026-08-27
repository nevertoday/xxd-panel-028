<p align="center">
  <img src="./assets/banner.svg" alt="XXD Panel 028 项目横幅" width="1200">
</p>

<div align="center">

# 🦁 XXD Panel 028

### 把照片安放成一件源图配色的等距纸上微缩景观

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-d75d32?style=flat-square)](#四种输出共享同一种纸上微缩逻辑)
[![Raster Output](https://img.shields.io/badge/Output-PNG-3c6f67?style=flat-square)](#边界与信任)

<strong>简体中文</strong> · <a href="README.en.md">English</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.ar.md">العربية</a>

</div>

<!-- xxd-human-intro:start -->
## 先说人话

你是不是也遇到过：照片明明很好，一交给 AI 做设计，就只剩一层千篇一律的“滤镜感”？主体还在，但那张照片原本的关系、情绪和小细节全丢了。

我做 **Panel 028**，就是想解决这个别扭。它不是给照片硬套模板，而是先认出照片里真正不能丢的东西，再把它翻译成：**把照片安放成一件源图配色的等距纸上微缩景观**。

### 30 秒看懂它

- **给它什么：** 一张照片、一个图片文件夹，或者一个只说了大概方向的想法。
- **它会做什么：** 保住人物、物件、动作和关系，再用这一号 Panel 独有的视觉语言重新设计。
- **最后拿到什么：** 可直接使用的 PNG；可以做对照图、纯设计图，也可以一次生成多种比例或整套壁纸。

### 最省事的试法

不需要先读完下面所有参数。丢一张图给 Agent，然后说：

> 用 XXD Panel 028 帮我处理这张图，先推荐最合适的构图和尺寸。

想先确认审美，就看下面的样张；想马上开做，直接跳到 [开始使用](#开始使用)。完整模式、尺寸和参数都保留在后面的折叠资料里，需要时再查。
<!-- xxd-human-intro:end -->

## 样张 · 来自 X

<table>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090447110168822128"><img src="./assets/examples/sample-01.jpg" alt="XXD Panel 028 样张 1"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090447110168822128"><img src="./assets/examples/sample-02.jpg" alt="XXD Panel 028 样张 2"></a></td>
  </tr>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090447110168822128"><img src="./assets/examples/sample-03.jpg" alt="XXD Panel 028 样张 3"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090447110168822128"><img src="./assets/examples/sample-04.jpg" alt="XXD Panel 028 样张 4"></a></td>
  </tr>
  <tr>
    <td colspan="2"><img src="./assets/examples/sample-05.png" alt="XXD Panel 028 样张 5"></td>
  </tr>
  <tr>
    <td width="33%"><img src="./assets/examples/sample-06.png" alt="XXD Panel 028 样张 6"></td>
    <td width="33%"><img src="./assets/examples/sample-07.png" alt="XXD Panel 028 样张 7"></td>
    <td width="33%"><img src="./assets/examples/sample-08.png" alt="XXD Panel 028 样张 8"></td>
  </tr>
</table>

> [小小东（@xiaoxiaodong01）](https://x.com/xiaoxiaodong01/status/2090447110168822128) · 2026-08-20<br>
> GPT2 x 立体 x 模型 x 微缩 x 美学提示词 x VOL.028

<p align="center"><a href="https://x.com/xiaoxiaodong01/status/2090447110168822128">查看原推文与完整提示词 →</a></p>

这些样张用于展示 028 的美学动机，不会把样张中的主体、构图、配色、文案或旧画幅变成生成参考或当前默认值。

> 正交等距 · 微缩基座 · 源图限定色盘 · 精细墨线 · 纸上编辑插画

XXD Panel 028 是一个面向 Codex 与兼容 Agent 的图像生成 Skill。它把照片中最可辨认的身份、轮廓、姿态与关系概括为一件正交等距微缩模型或建筑沙盘，安放在一小块源图有依据的纸面基座上。

清晰体块、边缘裁切、轻微投影和极少量微型细节建立尺度感、孤独感与收藏感，周围保留大面积开放纸面。色彩完全从源图提取、归纳、提纯、柔化；精细墨线、扁平色面、轻影与极浅纸粒形成安静、克制的编辑插画质感。

## 原始提示词 · 五种语言

[打开统一的多语言目录](references/original-prompt/)： [简体中文原文](references/original-prompt/zh-CN.md) · [English](references/original-prompt/en.md) · [日本語](references/original-prompt/ja.md) · [한국어](references/original-prompt/ko.md) · [العربية](references/original-prompt/ar.md)

简体中文文件保存小小东提供的逐字原文，并且是运行时唯一审美权威；其他四个版本是忠实的阅读译文，方便国际读者理解和转发，不会反过来改写生图提示词。

<!-- xxd-panel-benefit:start -->
## 快速判断：XXD Panel 028 适合你吗？

| 你关心的问题 | 这套风格给你的回答 |
|---|---|
| **你会得到什么** | 把照片安放成一件源图配色的等距纸上微缩景观 |
| **一眼可辨的特点** | 正交等距 · 微缩基座 · 源图限定色盘 · 精细墨线 · 纸上编辑插画 |
| **它如何尊重你的输入** | 保留输入中可辨认的身份、关系、结构与事实；风格化负责重新组织视觉语言，不把你的内容替换成无关模板。 |
| **可以用在哪里** | 可生成上下、左右、纯设计画面和四端壁纸，并支持多个比例与准确尺寸；交付形式会变化，这套 Panel 的风格身份不会被稀释。 |
<!-- xxd-panel-benefit:end -->

## 它如何把你的输入变成独特成品

普通“等距微缩”很容易退化成繁忙玩具小镇、现成游戏资产或一套与照片无关的薄荷绿和珊瑚红。

028 的顺序完全相反：

```text
锁定身份／轮廓／姿态／关系 → 概括为正交等距体块与有限层级 → 放在一块源图有依据的纸面基座 → 以边缘裁切、轻影与极少细节建立尺度 → 从源图归纳并柔化有限色盘 → 用精细墨线、扁平色面和浅纸粒完成
```

如果换成一张无关照片，微缩轮廓、体块层级、基座形状、尺度线索、综合色盘和文字关系仍然成立，这张图就不属于 028。

## 成品中最容易识别的风格特点

- **源图专属微缩：** 至少三个身份、轮廓、姿态、动作、功能、开口、尺度或关系线索进入同一个微缩模型。
- **一块纸面基座：** 主体落在源图有依据的纸片、低基座或微型地块上，周围保留大面积开放纸面。
- **克制尺度细节：** 体量对比、边缘裁切、轻影和极少人物、栏杆、树、轨道或小物件建立尺度，不形成第二焦点。
- **正交等距：** 相机干净、体块清楚、层级简洁，不做摄影透视、不可能空间、繁忙城市或游戏关卡。
- **源图限定色盘：** 从照片中提取最有识别度的颜色，归纳、提纯、柔化并保留原有冷暖性格，绝不套固定粉彩。
- **纸上材质：** 精细墨线、扁平哑光色面、同色阶、邻近色、轻微投影和极浅纸粒共同建立结构。
- **纤细编辑文字：** 一个短标题和极少微字沿留白边缘、主体基座、水平轴线或等距结构排列。

<details>
<summary><strong>完整能力与参数（需要时再展开）</strong></summary>

## 原始提示词优先，而不是二次导演

`references/original-prompt/zh-CN.md` 是本项目唯一的创作与审美权威。Skill 不再额外总结或扩写它，也不会统一规划颜色、色板、美学动机、标题或微文案。原始提示词要求怎样处理颜色、材料、构图、留白与文字，GPT Image 2 就按那套逻辑执行。

模式与尺寸会完整替换原始提示词旧有的 3:4 上下交付容器，但不改写它的转译美学。每张成品只向 GPT Image 2 发送一个已选模式的最终契约，不再把四种模式放进同一个通用模板让模型自行猜测。

## 四种可组合输出模式

模式可以单选或多选：`top-bottom`、`left-right`、`design-only`、`wallpaper-pack`；多选时，每个模式分别生成、分别拥有自己的提示词。

- `top-bottom`：整张画面由上方现实画面与下方设计转译两个主要部分组成。
- `left-right`：整张画面从顶部到底部保持完整左右结构，原图在左、设计在右；文字融入这两个区域，不再生成横跨全宽的第三块底栏。左右宽度可以不对称，由模型自主构图。
- `design-only`：原图只作为不可见的身份、结构、颜色与事实依据；整张成品的每个可见元素都必须属于该 Skill 自己的设计转译语言。
- `wallpaper-pack`：每台设备分别生成完整画布的设计转译壁纸，原图不作为照片区域出现。

上下或左右都不做分界线、中线百分比或像素坐标检测。只有用户明确要求像素级分区或原片逐像素不变时，才使用确定性拼合。

普通成品尺寸同样可以多选：自动适配、跟随原图、1:1、3:4、4:3、4:5、5:4、2:3、3:2、9:16、16:9、21:9、5:7、7:5，或自定义比例／准确像素。没有静默默认尺寸；每个不同比例都会基于同一份原始提示词独立重构。

壁纸套装可选“连贯”或“四张独立”。连贯模式先生成一张定调图，其余设备同时参考原图与定调图重新构图；不会把一张图机械裁成四种尺寸。

每次调用只建立一个任务目录，所有最终 PNG 直接放在该目录中，不再按来源、模式、尺寸或设备创建子文件夹。文件名使用 `source-序号-原文件名-模式-比例-像素.png`；壁纸额外包含连贯关系与设备，例如 `source-001-street-left-right-3x2-2160x1440.png`、`source-001-street-wallpaper-linked-phone-1440x3200.png`。

直接传入一个图片目录时，这个士兵 Skill 会自动批量处理目录中的图片，并让每张图片都使用 Panel 028 的同一套原始审美。默认递归扫描常见位图，先报告数量，再统一确认一次模式、尺寸、文字和语言；每张图片独立生成，互不借用内容或文案。整批仍然只创建一个扁平任务目录，单张失败会被记录，但不会静默跳过后续图片。

## 文字方式

正式生图前只确认三种选择：

1. **模型根据原始提示词生成文字**：用户只指定语言或地区，文字内容、数量、气质与排版由 GPT Image 2 按原始提示词生成；所有文字都从当前图片的内容、气质或隐喻中自然生长，任何事实或资料式信息都必须有用户输入、图片可见内容或已核实信息作为依据。
2. **使用我的准确文字**：逐字传给图像模型，不改写、不翻译、不补标题；排版仍遵循原始提示词。
3. **不要文字**：严格禁止文字与伪文字。

外层 Skill 不再预编标题、微文案或文案包。文字语言与操作语言分开确认，不根据人物、场景或文件名猜测国家与受众。

## 完整画布优先与位图边界

图像模型负责整张成品的审美重构，双联也默认一次直出完整画布。`scripts/compose_panel.py` 只保留为条件明确的兜底、无创尺寸校准和只读审计工具，不再预先规划每次任务，也不评价审美是否成功。

全部交付为 PNG 位图。每次调用都在 `~/Desktop/xxd/` 下创建新任务；已配置图像通道只返回脱敏状态，不公开供应商、端点、凭据、请求头、提示词、响应或账户信息。SVG、HTML、Canvas、图表和程序绘图不能替代最终作品。

## 能力自适应问询与快捷参数

同一个 Skill 会根据宿主真正提供的交互能力选择界面，不会把文本符号伪装成可点击控件：

- **Claude Code 提供 `AskUserQuestion + multiSelect: true` 时**：模式和尺寸使用真正的 checkbox；文字方式与壁纸关系使用单选。常用尺寸会按方形、竖版、横版分组展示，并累计多组选项；自定义尺寸进入自由输入。
- **Codex 只提供 `request_user_input` 时**：它只用于文字方式、壁纸关系等互斥单选，不拿来伪装模式或尺寸多选。模式与尺寸改用清楚的组合输入。
- **没有交互工具时**：使用两轮文字问询。第一轮选择一个或多个模式；第二轮填写尺寸与文字方式。Skill 不显示假的 `- [ ]`，也不会为了获得表单要求用户切换 Plan mode。

默认第二轮只展示“智能推荐／跟随原图／常用比例／自定义”四个入口；只有选择常用比例时，才展开完整比例库：方形 `1:1`，竖版 `3:4、4:5、2:3、9:16、5:7`，横版 `4:3、5:4、3:2、16:9、21:9、7:5`。所有比例都可组合，也可直接输入准确像素。

全部设置都可以直接作为参数传入：

```text
/xxd-panel-028 photo.jpg --mode top-bottom,design-only --size auto,3:4,9:16 --text prompt --locale ja-JP
```

支持 `--mode`、可重复或逗号分隔的 `--size`、`--text prompt|exact|none`、`--locale`、`--copy`、`--wallpaper linked|independent`、`--wallpaper-size`、`--out` 和 `--prefs`。参数齐全时跳过全部问询；参数不完整时只询问缺失项。

### 继承上次偏好，或全新配置

检测到历史偏好时，Skill 会先展示上次的模式、尺寸、文字与语言、壁纸关系和输出位置，再提供三个互斥选项：**直接沿用**、**沿用并修改**、**全新配置**。本次明确说出的要求始终优先；完整参数仍然直接执行。

可使用 `--prefs last|edit|new|off|clear` 直接指定行为：

```text
/xxd-panel-028 photo.jpg --prefs last
/xxd-panel-028 photo.jpg --prefs edit
/xxd-panel-028 photo.jpg --prefs new
```

偏好只保存交付设置，不保存原图、准确文案、生成结果、Panel 选择、模型通道、API 凭据或其他敏感信息。

`photo.jpg` 也可以直接替换为图片目录路径；目录输入会自动进入批量，不需要额外的 `--batch` 开关。

### 参数速查

| 参数 | 用途 | 常用值或格式 |
|---|---|---|
| `--mode` | 选择一种或多种成品用途 | `top-bottom`、`left-right`、`design-only`、`wallpaper-pack` |
| `--size` | 普通模式的比例或准确像素，可多选 | `auto`、`source`、`3:4`、`9:16`、`2160x3840` |
| `--text` | 文字来源 | `prompt`、`exact`、`none` |
| `--locale` | 画面中文字的语言或地区 | `zh-CN`、`en-GB`、`ja-JP`、`ko-KR`、`ar-SA` |
| `--copy` | 逐字使用用户文案，并启用 `--text exact` | `--copy "准确文案"` |
| `--wallpaper` | 四端壁纸之间的关系 | `linked`、`independent` |
| `--wallpaper-size` | 按设备覆盖壁纸分辨率 | `phone=...`、`ipad=...`、`desktop=...`、`watch=...` |
| `--out` | 指定输出根目录，仍会新建本次任务目录 | 文件夹路径 |
| `--prefs` | 处理上次偏好或关闭本次记忆 | `last`、`edit`、`new`、`off`、`clear` |

`photo.jpg` 可以替换为本地图片路径、已上传图片、图片目录或用户明确给出的其他来源。目录会自动进入批量处理。

### 按用途复制命令

```text
# 上下对照：智能推荐画幅，模型按原始提示词生成简体中文文字
/xxd-panel-028 photo.jpg --mode top-bottom --size auto --text prompt --locale zh-CN

# 左右对照：3:2 横版，无文字
/xxd-panel-028 photo.jpg --mode left-right --size 3:2 --text none

# 只要设计图：9:16 手机竖版，日语文字
/xxd-panel-028 photo.jpg --mode design-only --size 9:16 --text prompt --locale ja-JP

# 四端连贯壁纸：先建立一张定调图，再按设备分别重构
/xxd-panel-028 photo.jpg --mode wallpaper-pack --wallpaper linked --text none

# 四张独立壁纸：同时指定四台设备的准确分辨率
/xxd-panel-028 photo.jpg --mode wallpaper-pack --wallpaper independent --wallpaper-size phone=1440x3200,ipad=2048x2732,desktop=3840x2160,watch=1024x1024 --text none

# 跟随原图比例
/xxd-panel-028 photo.jpg --mode design-only --size source --text none

# 同一用途生成方形、竖版和横版三种完整构图
/xxd-panel-028 photo.jpg --mode design-only --size 1:1,3:4,16:9 --text none

# 自定义比例与准确像素可以一起多选
/xxd-panel-028 photo.jpg --mode design-only --size 11:14,2160x3840,3840x2160 --text none

# 模型依照原始提示词决定文字，只限定语言
/xxd-panel-028 photo.jpg --mode design-only --size 3:4 --text prompt --locale en-GB

# 使用准确文案，不改写、不翻译、不补标题
/xxd-panel-028 photo.jpg --mode design-only --size 3:4 --copy "让风经过这里" --locale zh-CN

# 两种模式 × 三种尺寸，共生成六张独立完整构图
/xxd-panel-028 photo.jpg --mode top-bottom,design-only --size 1:1,3:4,9:16 --text prompt --locale zh-CN

# 整个目录统一使用 Panel 028；公共设置只解析一次
/xxd-panel-028 "/path/to/photos" --mode design-only --size auto,9:16 --text prompt --locale zh-CN

# 重复参数也会累积，并把本次任务放到指定根目录
/xxd-panel-028 photo.jpg --mode top-bottom --mode left-right --size 3:4 --size 16:9 --text none --out ./deliveries
```

## 生图模型优先级

GPT Image 2 是默认首选，并继续执行本项目现有的高保真垫图、生成前确认整张画幅、双联一次生成完整画布、脚本仅作条件式兜底等逻辑。

当当前工具或已配置兼容通道确实可用，并能满足原图保真、整张成品比例、目标语言文字和连贯壁纸多图参考等要求时，也支持 Seedance 5.0 Pro、Nano Banana Pro（Gemini Image Pro）、Nano Banana 2（Gemini Image Flash）或其他兼容位图模型。备用模型只替换生成通道，不得改变模式、画幅、文案、语言、壁纸关系和完整画布优先策略。

如果没有合适的生图通道，Skill 会请用户启用生图工具或提供 API Key。用户主动提供的凭据可以用于当前任务，但不得在回复或日志中回显、展示或泄露；未经用户明确要求，不会长期保存凭据或修改供应商、账户、计费及全局路由配置。

</details>

## 开始使用

```bash
git clone https://github.com/nevertoday/xxd-panel-028.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/xxd-panel-028" ~/.codex/skills/xxd-panel-028
```

Claude Code 用户可以把同一目录链接到 `~/.claude/skills/xxd-panel-028`。安装后重新启动 Agent 会话。

```text
$xxd-panel-028
把这张照片做成左右双联，文案由你根据照片内涵创作，使用自然韩语。
```

只上传照片也可以调用。Skill 会先用分行编号菜单询问一个或多个模式，再询问文字设置；选择壁纸时还会确认连贯或独立以及设备尺寸。

完整规范：

- [Skill 工作流](SKILL.md)
- [中文运行适配器](references/xxd-panel-028-prompt.zh-CN.md)
- [英文运行适配器](references/xxd-panel-028-prompt.en.md)
- [原始风格提示词](references/original-prompt/zh-CN.md)

## 边界与信任

- 每张照片只在自己的任务中使用，不借用其他输入、旧成品或样张里的主体、颜色、文案和构图。
- 每次调用都创建新的任务子文件夹；相同原图和参数也要重新生成，旧成品不能冒充当前任务。
- 最终交付为 PNG 位图，不是 SVG、HTML、Canvas 或程序绘图替代品。
- 已配置位图桥接只返回脱敏状态，不显示供应商、端点、请求头、凭据、提示词或服务器响应正文。
- 每个所选普通模式各返回一张；若选择 `wallpaper-pack`，再返回四张独立壁纸。选择 `全部` 时每张原图共返回 7 个 PNG，分处四个同级模式文件夹，绝不生成拼贴总览。

本地拼版需要 Python 3 和 Pillow。安全位图桥接使用 Python 3.11+ 的 `tomllib`。图像生成仍需要主机 Agent 的内置位图能力或已经配置好的兼容位图路径。

## 项目结构

```text
xxd-panel-028/
├── SKILL.md
├── README.md / README.en.md / README.ja.md / README.ko.md / README.ar.md
├── agents/openai.yaml
├── assets/
│   ├── banner.svg
│   └── examples/（未来本地样张占位）
├── scripts/
│   ├── compose_panel.py
│   └── configured_imagegen.py
└── references/
    ├── xxd-panel-028-prompt.zh-CN.md
    ├── xxd-panel-028-prompt.en.md
    └── 028-source.md
```

<!-- xxd-panel-catalog:start -->
## XXD Panel 全系列项目

60 个 Panel 各自保留独立的原始提示词与审美逻辑。下面列出全部项目地址和核心风格特点；当前项目以粗体标出。

| 项目地址 | 风格特点 |
|---|---|
| [xxd-panel-001](https://github.com/nevertoday/xxd-panel-001) | 稚拙线条 · 复古纸感 · 混合媒材 · 轻巧隐喻 · 暖色留白 |
| [xxd-panel-002](https://github.com/nevertoday/xxd-panel-002) | 叙事轮廓 · 迟疑手线 · 近似色调 · 局部夸张 · 套印文字 |
| [xxd-panel-003](https://github.com/nevertoday/xxd-panel-003) | 连续黑线 · 公共议题 · 受力结点 · 留白沉默 · 向外释放 |
| [xxd-panel-004](https://github.com/nevertoday/xxd-panel-004) | 在地现实 · 精准单线 · 几何透视 · 主题配色 · 城市品牌文字 |
| [xxd-panel-005](https://github.com/nevertoday/xxd-panel-005) | 钝拙体块 · 暗色结构场 · 局部显形 · 三层色阶 · 丝网印刷 × 粉蜡笔 |
| [xxd-panel-006](https://github.com/nevertoday/xxd-panel-006) | 小主体 · 80%–90% 纸面留白 · 纤细手线 · 四色以内 · 丙烯平涂 |
| [xxd-panel-007](https://github.com/nevertoday/xxd-panel-007) | 实物小图 · 局部／剖面／重复 · 错位留白 · 细黑手写 · 扫描纸感 |
| [xxd-panel-008](https://github.com/nevertoday/xxd-panel-008) | 正交等距 · 平台／台阶／门洞 · 空间悖论 · 动态粉彩 · 极净哑光 3D |
| [xxd-panel-009](https://github.com/nevertoday/xxd-panel-009) | 极小主体 · 巨大留白 · 单一空间关系 · 专色体系 · Halftone 丝网印刷 |
| [xxd-panel-010](https://github.com/nevertoday/xxd-panel-010) | 粗黑剪影 · 内部白色特征区 · 干媒介纸感 · 极少环境记号 · 童书编辑小字 |
| [xxd-panel-011](https://github.com/nevertoday/xxd-panel-011) | 一个核心意象 · 一组关系 · 连续黑线 · 主动留白 · 一抹记忆点色 |
| [xxd-panel-012](https://github.com/nevertoday/xxd-panel-012) | 高密聚合 · 外围稀释 · 几何约束 · 一种生命主线色 · 黑灰微排版 |
| [xxd-panel-013](https://github.com/nevertoday/xxd-panel-013) | 一张横向票体 · 74/26 分区 · 治愈水彩 · 象牙白留白 · 本地化信息票根 |
| [xxd-panel-014](https://github.com/nevertoday/xxd-panel-014) | 折叠与切面 · 层叠与嵌套 · 源图重心构图 · 真实纸纤维 · 可读纸艺文字 |
| [xxd-panel-015](https://github.com/nevertoday/xxd-panel-015) | 解构—筛选—提炼—重构 · 少量形体 · 严格色彩角色 · 象牙色留白 · 艺术书微排版 |
| [xxd-panel-016](https://github.com/nevertoday/xxd-panel-016) | ONE SUBJECT · ONE MOTION · A LARGE FIELD OF AIR |
| [xxd-panel-017](https://github.com/nevertoday/xxd-panel-017) | 圆润形体 · 粗糙断线 · 纯色平涂 · 明亮色场 · 轻快不对称 |
| [xxd-panel-018](https://github.com/nevertoday/xxd-panel-018) | 一个视觉锚点 · 前中后少量纸层 · 暖象牙留白 · 哑光纸触感 · 完整微排版 |
| [xxd-panel-019](https://github.com/nevertoday/xxd-panel-019) | RECOGNISE FIRST · REDUCE WITH INTENT · COMPOSE WITH TYPE |
| [xxd-panel-020](https://github.com/nevertoday/xxd-panel-020) | 解构—筛选—提炼—重构 · 少量形体 · 严格色彩角色 · 象牙色留白 · 艺术书微排版 |
| [xxd-panel-021](https://github.com/nevertoday/xxd-panel-021) | 纯黑矩形 · 主体大部入场 · 一个特征越界 · 抖动复印线 · 白色负形与微灰面 |
| [xxd-panel-022](https://github.com/nevertoday/xxd-panel-022) | 纯黑矩形 · 主体大部入场 · 一个特征越界 · 流畅稳定线 · 唯一单点彩色 |
| [xxd-panel-023](https://github.com/nevertoday/xxd-panel-023) | 源图择窗 · 浅色呼吸背景 · 柔和有色光影 · 喷绘颗粒 · 虚实投影与微排版 |
| [xxd-panel-024](https://github.com/nevertoday/xxd-panel-024) | 真实摄影主体 · 窄长浅色窗口 · 横／竖／斜向自适应 · 东方留白 · 高级商业编辑 |
| [xxd-panel-025](https://github.com/nevertoday/xxd-panel-025) | 一眼主体 · 第二眼隐藏意象 · 正负形反转 · 2–4 色莫兰迪 · 真实丝网触感 |
| [xxd-panel-026](https://github.com/nevertoday/xxd-panel-026) | RECOGNISE QUIETLY · REDUCE GENTLY · LET THE PAPER BREATHE |
| [xxd-panel-027](https://github.com/nevertoday/xxd-panel-027) | 乳白厚纸 · 浅凸浅凹 · 极简线刻 · 哑金焦点 · 博物馆展陈 |
| **[xxd-panel-028](https://github.com/nevertoday/xxd-panel-028)** | 正交等距 · 微缩基座 · 源图限定色盘 · 精细墨线 · 纸上编辑插画 |
| [xxd-panel-029](https://github.com/nevertoday/xxd-panel-029) | 横向色域 · 浅色蜡粉笔 · 粗纤维手工纸 · Risograph 颗粒 · 松弛手写 |
| [xxd-panel-030](https://github.com/nevertoday/xxd-panel-030) | 真实自然材料 · 矩形色域 · 自然越界 · 极少黑线 · 编辑留白 |
| [xxd-panel-031](https://github.com/nevertoday/xxd-panel-031) | 一个核心母题 · 源图几何母体 · 民俗图录 · 内部粗粝印痕 · 外部精确秩序 |
| [xxd-panel-032](https://github.com/nevertoday/xxd-panel-032) | 图文一体 · 原生文字结构 · 源图特征嵌入 · 视觉字距 · 高级留白 |
| [xxd-panel-033](https://github.com/nevertoday/xxd-panel-033) | 可识别母题 · 平面拼贴 · 尺度对比 · 源图鲜明配色 · 封面排版 |
| [xxd-panel-034](https://github.com/nevertoday/xxd-panel-034) | 小尺度章印 · 2–4 种专色 · 手刻线 · 暖色纸张 · 田野注释 |
| [xxd-panel-035](https://github.com/nevertoday/xxd-panel-035) | 单一积木主体 · 明艳源图色 · 哑光 ABS · 安静背景 · 模块文字 |
| [xxd-panel-036](https://github.com/nevertoday/xxd-panel-036) | 一个关系 · 纤细连续线 · 二至四色域 · 水彩渗化 · 柔软留白 |
| [xxd-panel-037](https://github.com/nevertoday/xxd-panel-037) | 一枚徽章 · 源图珐琅色 · 白金属外框 · 流金细节 · 实体短影 |
| [xxd-panel-038](https://github.com/nevertoday/xxd-panel-038) | 源图布色 · 真实毛边 · 手缝针脚 · 主动留白 · 隐藏情绪 |
| [xxd-panel-039](https://github.com/nevertoday/xxd-panel-039) | 一图一核 · 中国丝线 · 针向层次 · 洁净底色 · 东方留白 |
| [xxd-panel-040](https://github.com/nevertoday/xxd-panel-040) | 真实主体 · 黑线小人 · 微型叙事 · 大量留白 |
| [xxd-panel-041](https://github.com/nevertoday/xxd-panel-041) | 主题隐喻 · 等距秩序 · 淡手稿 · 日系清透色 · 东方留白 |
| [xxd-panel-042](https://github.com/nevertoday/xxd-panel-042) | 原始视角 · 二至五层 · 稳定锚点 · 透明水彩 · 编辑注释 |
| [xxd-panel-043](https://github.com/nevertoday/xxd-panel-043) | 真实皂沫 · 正面平视 · 源图深底 · 细密泡缘 · 安静空间 |
| [xxd-panel-044](https://github.com/nevertoday/xxd-panel-044) | 薄层纯金 · 正面平面 · 源图深底 · 锤纹压痕 · 安静秩序 |
| [xxd-panel-045](https://github.com/nevertoday/xxd-panel-045) | 圆润模块 · 源图色彩 · 等距纵深 · 哑光触感 · 编辑微排版 |
| [xxd-panel-046](https://github.com/nevertoday/xxd-panel-046) | 明亮白底 · 鲜活厚涂 · 微缩实体 · 斜向色带 · 温暖光感 |
| [xxd-panel-047](https://github.com/nevertoday/xxd-panel-047) | 等距微缩 · 主题厚涂 · 真实接触 · 暖白纸面 · 明亮色彩 |
| [xxd-panel-048](https://github.com/nevertoday/xxd-panel-048) | 透明结构 · 科学图解 · 清透单色 · 精确注释 · 编辑留白 |
| [xxd-panel-049](https://github.com/nevertoday/xxd-panel-049) | 限色木刻 · 手工刀痕 · 哑光套印 · 温暖纸面 · 不完整边缘 |
| [xxd-panel-050](https://github.com/nevertoday/xxd-panel-050) | 定制旅行场景 · 空气蓝 · 极简平涂矢量 · 编辑留白 · 一图一身份 |
| [xxd-panel-051](https://github.com/nevertoday/xxd-panel-051) | 微缩纸艺 · 横向悬浮景观带 · 真实手工材质 · 空气蓝 · 大量留白 |
| [xxd-panel-052](https://github.com/nevertoday/xxd-panel-052) | 纸艺微缩 · 横向浮岛 · 真实手作 · 空气感冷蓝 · 大量留白 |
| [xxd-panel-053](https://github.com/nevertoday/xxd-panel-053) | 观察线稿 · 透明淡彩 · 音乐性节奏 · 近白纸面 · 大胆留白 |
| [xxd-panel-054](https://github.com/nevertoday/xxd-panel-054) | 选择性记忆 · 主视觉 · 六枚贴纸 · 哑光印刷 · 空气感蓝 |
| [xxd-panel-055](https://github.com/nevertoday/xxd-panel-055) | 主体叙事 · 治愈粉彩 · 浅油画笔触 · 空气感蓝 · 编辑留白 |
| [xxd-panel-056](https://github.com/nevertoday/xxd-panel-056) | 核心意象 · 巨大留白 · 暖冷跳色 · 稚拙手绘 · 视觉隐喻 |
| [xxd-panel-057](https://github.com/nevertoday/xxd-panel-057) | 几何构成 · 智能马赛克 · 建筑图解 · 艺术地图 · 暖冷色块 |
| [xxd-panel-058](https://github.com/nevertoday/xxd-panel-058) | 潜台词解读 · 几何极简 · 观念景观 · 柔和手工质感 · 淡色留白 |
| [xxd-panel-059](https://github.com/nevertoday/xxd-panel-059) | 手绘叙事 · 童真隐喻 · 温暖纸感 · 轻微诙谐 · 诗性旁白 |
| [xxd-panel-060](https://github.com/nevertoday/xxd-panel-060) | 黑色主形 · 极大留白 · 网点消散 · 禅意思考 · 哲思碎片 |
<!-- xxd-panel-catalog:end -->

## 关于 XXD

XXD 是小小东的品牌名称缩写。项目由 [@xiaoxiaodong01](https://x.com/xiaoxiaodong01) 创建并维护。

## 服务与会员

### 小小东总控 · 将军总指挥 Skill · 100 元

一次支付 100 元获得本套将军总指挥 Skill（`xxd-panel-all`），用于主控、推荐、点将和批量调度全部士兵 Skills。扫码后请备注“将军总指挥 Skill”。

<!-- xxd-panel-command-system:start -->
**购买后可使用：主控全队的将军 Skill**

| 层级 | Skill | 负责什么 |
|---|---|---|
| **将军级** | [`xxd-panel-all`](https://github.com/nevertoday/xxd-panel-all) | 识别当前可用的编号 Skills；按图片、主题和用途推荐；按编号点将；组织同图多风格试稿；为图片文件夹批量分配并逐项派发。 |
| **士兵级** | `xxd-panel-NNN`（当前 001–060） | 每个编号只执行自己独立的原始提示词与审美，把将军派发的单个任务完成为成品。 |

将军 Skill 是整个编号 Skills 队伍的总控入口。购买后即可使用，并获得安装、版本更新、队伍配置和调度方式的答疑。将军只负责组织与派发，不会改写、混合或覆盖士兵的原始美学；每张成品仍由被选中的士兵 Skill 独立完成。
<!-- xxd-panel-command-system:end -->

### 知识星球＋成员提示词库＋Skills 所有将军会员 · 699 元/年

[知识星球](https://wx.zsxq.com/group/15554814142882)、[小小东成员提示词库](https://vip.xiaoxiaodong.ai/)与 Skills 所有将军会员是同一份会员权益：**一次年费同时开通三项权益，无需重复付费。**

1. 在[知识星球](https://wx.zsxq.com/group/15554814142882)开通后，微信联系小小东领取成员提示词库兑换码。
2. 在[成员提示词库](https://vip.xiaoxiaodong.ai/)自助开通后，微信联系小小东邀请进入知识星球。

<p align="center">
  <a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="小小东付费服务微信二维码" width="320"></a>
</p>

<div align="center">

**不是把照片塞进玩具城，而是把它最独特的体量、颜色与孤独安放在纸上。**

</div>

---

<div align="center">
  <h2>☕ 为开源项目赞助算力</h2>
  <p>如果项目对你有帮助，愿意的话，可以用小小东本人的微信或支付宝赞赏码支持算力。</p>
  <table>
    <tr>
      <td align="center" width="240">
        <a href="https://colors.xiaoxiaodong.ai/docs/images/wechat-reward-qr.png"><img src="https://colors.xiaoxiaodong.ai/docs/images/wechat-reward-qr.png" alt="小小东微信算力赞助二维码" width="180"></a><br>
        <strong>微信算力赞助</strong>
      </td>
      <td align="center" width="240">
        <a href="https://colors.xiaoxiaodong.ai/docs/images/alipay-reward-qr.png"><img src="https://colors.xiaoxiaodong.ai/docs/images/alipay-reward-qr.png" alt="小小东支付宝算力赞助二维码" width="180"></a><br>
        <strong>支付宝算力赞助</strong>
      </td>
    </tr>
  </table>
</div>
