# 模具：视觉笔记（-v）

## 灵魂

把一个概念铸成一份编辑式的图文档案。

读者翻它，像翻一本期刊专题——从一个真问题（专题刊头）→ 失败的尝试（便签批注、档案标签）→ 一句"等等——"的转折（跨栏大标题）→ 看见那个东西（Hero 对开页）→ 名字（Closing 名牌）。

不是博物馆陈列，是杂志栏目。不是教科书定义，是探案档案。视觉与叙事一起负责——让读者自己经历"卡住—走不通—翻过去—看见了"的弧线，**文字克制，不点题**。

## 五条公理（不可削）

每张图都必须满足。削掉任何一条，灵魂就崩。

### 公理 1 · 有真问题在前

每张图必须以一个**具体的、可触摸的、卡住的问题**开始。

不是「什么是 X」（教科书式），是「当时的人们用 A、B、C 都不够，因为……」。

问题必须有裂缝，裂缝必须可感——读者自己能感到"嗯，这确实卡住了"。

**削掉它**：失去叙事的发动机。退化为时间线。

### 公理 2 · 必须有失败

路径中必须包含**至少一次失败**（或走偏、半对了）。线性推导（"由此可得"）会杀掉张力。

失败让读者明白：不是只有这一条路，是别的路都走不通。

**削掉它**：变成定理证明。读者点头但没占有。

### 公理 3 · 顿悟在前、命名在后

读者必须先「看到那个东西」（顿悟时刻），再被告诉"这个东西叫……"。

先抛出概念名再解释，等于剧透。**命名必须是路径的终点，不是起点。**

→ 标题不能出现概念名（「打不开的盒子」可以，「黑箱理论」不可以）。

**削掉它**：剧透杀死惊讶感。读者获得标签而非视力。

### 公理 4 · 「现在」视角，非「上帝」视角

每一站，时间锚点是「他/她在那一刻能看到什么」，**不是「我们站在 100 年后回望」**。

后世评价、连锁影响、与其他概念的对比——都是路径外的事，不进画面。

**削掉它**：读者重新成为博物馆游客。在场感破碎。

### 公理 5 · 文字克制，不点题

让叙事张力自己产生发明感，不靠元自指话术。

**禁止句式**：
- ✗「你以为你刚才学到了一个概念。其实你刚才不得不发明了它。」
- ✗「你重新分娩了它」「你亲身发明了它」「你见证了它的诞生」之类自指
- ✗ 任何「你 + 发明 / 创造 / 重新 X + 它」结构

**允许的余韵**（如果一定要 closing 加一句）：
- ✓ 诗意而非元论："于是，你看见了山。" / "门一旦开过一次，就不会再合上。"
- ✓ 完全不要 wink，让 closing 在 mega-name + byline + closing-body 后干净结束

读者的发明感来自**叙事张力**（失败可见 / 转折顿挫 / 视觉惊讶），不来自被告知"你正在发明"。**告诉就破。**

每一层叙事可以留缝隙（未完成句、开放设问、暗示性图示），但**不能用元话语点题**。

**削掉它**：自我陶醉的话术覆盖了真正的发明感。

---

## 步骤 1：读取模板

Read `assets/sketchnote_template.html`

模板提供（仅"基础设施"）：
- 字体加载：`Noto Sans SC` / `Noto Serif SC` / `Caveat` / `JetBrains Mono`
- CSS 变量基底：基底色 / 字族
- `.colophon` 署名 + 来源
- `{{CUSTOM_CSS}}` `{{CONTENT_HTML}}` `{{LOGO}}` `{{SOURCE_LINE}}` 插槽

具体的杂志骨架 layout 由本模式现场设计——模板只给颜料盒和画框。

注：旧版的 `.station--start/--failed/--pivot/--insight/--name` 已**废弃**——本模式用六种 layout 模具：`.feature/.note/.archive/.cross/.hero/.closing`。橙色弯曲箭头流程也已废弃。

---

## 步骤 2：寻找叙事弧线

读完原始内容后，先**沉默 30 秒**问自己一个问题：

> 这个概念是从哪个**真问题**里长出来的？如果回到它被发明前的那一刻，世界缺了什么、谁卡在哪里？

如果回答不了，**回去重读**直到能答。否则后面的图都是浮的。

### 2.1 找问题（站点 1：起点 / Feature）

不是抽象的「问题领域」，是**一个具体的、可触摸的卡住的瞬间**。

举例（黑箱理论）：
- ✗「20 世纪复杂系统研究遇到的认识论困境」（教科书腔）
- ✓「缴获的电子设备里可能有炸药——开了就炸。活体的大脑——开了就死。雷达系统几千个反馈元件——开了你也理不清。」

裂缝感来自具体的物理约束。

输出：
- **head**：卡住的描述（Serif 大标题 56-60px）
- **lead**：italic 引言段（一句简洁的领题，红色左边线）
- **body**：2-4 个具体例子（drop cap 第一字下沉）
- **ask**：开放设问（手写体 Caveat，红色）

### 2.2 找失败（站点 2、3：Note 和 Archive）

至少一次，理想 1-2 次。每次失败要呈现：
- **当时的工具**（已有的方法、本能反应）
- **为什么这个工具不够**（具体的失败原因，不是泛泛"不行"）

**两个失败站点必须形态不同**——一个 note（便签批注），一个 archive（档案标签），节奏才出来。

举例（黑箱理论）：
- 站点 2 note（拆）：还原论本能 → 活体不能拆 / 元件多到画图无意义
- 站点 3 archive（跳过）：行为主义跳过内部 → "不管"不等于"回答"

输出：
- **kicker**：编号 + "第 N 次尝试"
- **head**：尝试的简短动作名（"那就拆开看" / "那就别看里面了"）
- **body**：思路 + 失败原因（紧凑 2-3 段）
- **失败标记**：站点 2 用 `.strike` 红笔删除线（划在关键词如「解析解」上）+ scribble 红笔批注；站点 3 用黑色 `.stamp` 印章（含 ✕ 大字）+ verdict 红色 italic 结案语

### 2.3 找转折（站点 4：Cross-page Mega）

转折不是"换一个角度"，是**反向使用约束**。

举例：
- 不是"我打不开它"（被动）
- 而是"我**故意**不开它"（主动）

转折点必须有"等等——"的停顿感。

输出：
- **mega**：表达停顿的大字（"等等——"，Serif 200px）+ amber 高亮 highlight 段（仅"等等"二字）
- **body**：反向陈述（左栏）
- **visual**：反向姿态的小图（右栏，球滚山谷之类的简单类比）+ caption

### 2.4 找顿悟（站点 5：Hero Spread）

顿悟站点呈现**转折姿态实施后意外发现的核心洞察**。

举例：
- 故意不开 → 只看输入输出 → 竟然能完全刻画系统！

⚠ 站点 5 **不能**出现概念名！

输出：
- **head**：顿悟的姿态名（"在状态空间画一座山" / "只看输入输出"），Serif 50px
- **pull-quote**：核心句子大引号（蓝色 Serif italic 38px，浮动 `\201C` 大引号）
- **body**：洞察的具体表述（drop cap）
- **visual**：可视化那个洞察（大幅 hero 图，左 7 分占满）+ caption

### 2.5 找命名（站点 6：Closing Page）

读者已经看到了那个东西。现在告诉他名字。

输出：
- **approach**：「这种 X 的研究对象，叫——」（italic 26px Serif）
- **mega-name**：大字呈现（中文 Serif 144px + 英文 Sans 38px）
- **byline**：Mono uppercase 14px，上下细黑线，间用 `·` 分隔
  - 格式：`<人名> · <年份> · <机构> · <文献>`
- **closing-body**：它打开了什么（2-3 段 Serif 22px）
- **epilogue**（可选）：诗意余韵，**不元自指**
  - ✓「于是，你看见了山。」
  - ✗「你以为你刚才学到了一个概念……」

---

## 步骤 3：设计画面（杂志 × 探案档案风）

### 3.1 六种 layout 模具

每个站点必须用不同的 layout，让节奏出现：

| 站点 | layout 模具 | class | 视觉特征 |
|------|------------|-------|---------|
| 1 起点 | feature spread | `.feature` | 米色底 + grid 6fr/6fr，左大图 / 右文字，kicker + Serif 大标题 + italic lead + drop cap body |
| 2 失败 | margin note | `.note` | 浅米色底 + 窄栏 540px，便签纸感（顶部虚线穿孔），红笔删除线 + scribble + footnote ¹，微旋 0.5deg |
| 3 失败 | archive label | `.archive` | 全宽 + 黑色印章 stamp（左 168px，含 ✕ 大字）+ 右栏 body + 网格图 + verdict 红色 italic |
| 4 转折 | cross-page mega | `.cross` | 全宽 + Serif 200px「等等——」+ amber 高亮 + 二栏（文字 / 图） |
| 5 顿悟 | hero spread | `.hero` | 蓝色顶边 4px + grid 7fr/5fr，大图（左）+ 右栏 pull quote + drop cap body |
| 6 命名 | closing page | `.closing` | 米色底 + 双线顶边 + 中心对称 + 巨大 Serif 名 + byline 上下细线 + epilogue |

**节奏（极重要）**：开阔（feature） → 紧（note 错位） → 紧（archive 横长） → 爆（cross 200px） → 开阔（hero） → 静（closing 中心对称）

不是均匀展开。是有呼吸的——开阔与紧凑交替，转折时大爆炸，最后回到中心对称。

### 3.2 字族对比（必须四种同时使用）

- **Serif**（Noto Serif SC）：杂志主标题、命名 mega-name、引言 lead、引文 pull-quote
- **Sans**（Noto Sans SC）：正文 body-sans、failed station head、kicker 后文字
- **Mono**（JetBrains Mono / SF Mono）：编号 num、kicker label、byline、footnote 编号、stamp
- **Hand**（Caveat / 楷体）：手写批注 scribble、ask 设问、caption

字族对比是杂志感的核心。任一缺席，视觉就回到 AI 单一字族的均质感。

### 3.3 装饰元素清单（按需取用）

| 元素 | 用法 | 实现 |
|------|------|------|
| **kicker** | 站点序号 + 类型小字 | Mono uppercase 13px + 黑底白字 num 方块 + 36px 短横线 rule |
| **drop cap** | body 第一段第一字 | `::first-letter` float left, 96px Serif |
| **lead** | feature 引言 | italic 23px Serif + 红色左边线 2px |
| **pull quote** | hero 关键句 | italic 38px Serif + 蓝色边线 4px + 浮动 `\201C` 大引号 100px |
| **strike** | failed body 删除关键词 | `text-decoration: line-through` 红色 2.5px |
| **scribble** | note 红笔批注 | Caveat 24px + 6deg 旋转 + 红色 + 虚线红边框 |
| **stamp** | archive 失败印章 | 黑底白字 12px Mono + ✕ Serif 64px |
| **verdict** | archive 结案语 | italic 19px Serif 红色 + 上虚线分隔 |
| **footnote** | note 脚注 | Mono 13px + ¹ 上标 + 上虚线分隔 |
| **byline** | closing 出处 | Mono 14px uppercase + letter-spacing 0.18em + 上下细黑线 |
| **mega** | cross 大字 | Serif 200px + amber 渐变高亮 highlight 段 |
| **epilogue** | closing 余韵 | italic 26px Serif + `—` 红色破折号前缀 |

不要全用。但 **kicker、drop cap、byline、stamp** 是结构必须项。

### 3.4 颜色系统（精简而克制）

| 角色 | 变量 | hex | 用法 |
|------|------|-----|------|
| 暖米白底 | `--bg` | `#FAF7EF` | 主背景 |
| 米色卡 | `--paper` | `#F5F1E5` | feature/closing 底 |
| 墨黑标题 | `--ink-strong` | `#0F0F0F` | 重要文字（避免 #000 纯黑） |
| 正文黑 | `--ink` | `#1F1F1F` | body |
| 灰文 | `--ink-light` | `#6B6B6B` | kicker、caption |
| 红 | `--red` | `#B23A2C` | 错误、批注、强调 |
| 蓝深 | `--blue-deep` | `#3D5A80` | 顿悟视觉 |
| amber | `--amber` | `#BB8A2B` | 转折提示 |
| amber-soft | `--amber-soft` | `#D7A85A` | 高亮底色 |

**≤ 4 主色**（红 + 蓝 + amber + 中性）。不堆色。**禁止 #000 纯黑**。

### 3.5 边距与节奏

- 杂志主体每节左右内边距：64px
- 节与节之间用 border-top + 不同 margin-top 自然分隔（不是 gap: 88px）
- note 站点错位浮右（`margin: 56px 64px 0 auto`）
- archive 站点全宽贴边（`margin: 64px 64px 0`）
- cross 上下大空白（`padding: 96px 64px 84px`）+ margin-top: 64px
- hero `padding: 72px 64px 64px` + margin-top: 56px
- closing `padding: 80px 64px 84px` + margin-top: 64px + text-align: center

---

## 步骤 4：写 CSS + HTML

把全部 CSS 写入 `{{CUSTOM_CSS}}`，全部 HTML 写入 `{{CONTENT_HTML}}`。

### 4.1 CSS 骨架（完整复用版）

```css
:root {
  --bg: #FAF7EF;
  --paper: #F5F1E5;
  --ink: #1F1F1F;
  --ink-strong: #0F0F0F;
  --ink-light: #6B6B6B;
  --ink-fade: #9A958C;
  --rule: rgba(15,15,15,0.16);
  --red: #B23A2C;
  --blue-deep: #3D5A80;
  --amber: #BB8A2B;
  --amber-soft: #D7A85A;
  --sans: 'Noto Sans SC', 'PingFang SC', system-ui, sans-serif;
  --serif: 'Noto Serif SC', 'Songti SC', serif;
  --hand: 'Caveat', '楷体', 'STKaiti', cursive;
  --mono: 'JetBrains Mono', 'SF Mono', monospace;
}

/* magazine head */
.magazine-head {
  padding: 60px 64px 44px;
  border-bottom: 2px solid var(--ink-strong);
  position: relative;
}
.magazine-head::after {
  content: ''; position: absolute;
  left: 64px; right: 64px; bottom: -8px;
  height: 1px; background: var(--ink-strong);
}
.top-bar {
  display: flex; justify-content: space-between; align-items: center;
  font: 600 12px/1 var(--mono);
  color: var(--ink-light);
  letter-spacing: 0.22em;
  text-transform: uppercase;
  margin-bottom: 36px; padding-bottom: 14px;
  border-bottom: 1px solid var(--rule);
}
.top-bar .left { display: flex; align-items: center; gap: 18px; }
.top-bar .badge { background: var(--ink-strong); color: var(--bg); padding: 5px 11px; letter-spacing: 0.18em; }
.magazine-head h1 {
  font: 900 110px/0.92 var(--serif);
  color: var(--ink-strong);
  letter-spacing: -0.03em;
  margin-bottom: 24px;
}
.magazine-head .deck {
  font: italic 400 26px/1.45 var(--serif);
  color: var(--ink-light);
  max-width: 820px;
  border-left: 3px solid var(--ink-strong);
  padding-left: 20px;
}

/* shared */
.kicker {
  font: 600 13px/1 var(--mono);
  color: var(--ink-light);
  text-transform: uppercase;
  letter-spacing: 0.22em;
  display: inline-flex; align-items: center; gap: 12px;
}
.kicker .num {
  background: var(--ink-strong); color: var(--bg);
  padding: 5px 10px 4px; font-weight: 700; letter-spacing: 0.12em;
}
.kicker .rule { width: 36px; height: 1px; background: var(--ink-strong); }
.head-serif { font: 700 60px/1.05 var(--serif); margin: 18px 0 22px; letter-spacing: -0.018em; color: var(--ink-strong); }
.head-sans { font: 900 42px/1.12 var(--sans); margin: 14px 0; letter-spacing: -0.012em; color: var(--ink-strong); }
.body-serif p { font: 400 22px/1.65 var(--serif); }
.body-serif p + p { margin-top: 12px; }
.body-sans p { font: 400 21px/1.6 var(--sans); }
.body-sans p + p { margin-top: 10px; }
.body em { font-style: normal; font-weight: 700; color: var(--ink-strong); }
.ask { font: 600 32px/1.3 var(--hand); color: var(--red); margin-top: 22px; display: block; }
.drop-cap > p:first-child::first-letter {
  float: left;
  font: 700 96px/0.84 var(--serif);
  color: var(--ink-strong);
  margin: 4px 14px -6px 0;
}

/* feature */
.feature {
  padding: 56px 64px 60px;
  background: var(--paper);
  border-bottom: 1px solid var(--rule);
  display: grid;
  grid-template-columns: 6fr 6fr;
  gap: 44px;
  align-items: start;
}
.feature .lead {
  font: italic 400 23px/1.45 var(--serif);
  margin-bottom: 22px;
  padding: 0 0 0 18px;
  border-left: 2px solid var(--red);
}

/* note */
.note {
  margin: 56px 64px 0 auto;
  max-width: 540px;
  padding: 28px 30px 28px 32px;
  background: #FFFBF1;
  border: 1px solid rgba(120,110,80,0.32);
  border-left: 4px solid var(--red);
  box-shadow: 5px 9px 22px -12px rgba(0,0,0,0.22);
  position: relative;
  transform: rotate(0.5deg);
  transform-origin: top right;
}
.note::before {
  content: ''; position: absolute;
  top: -1px; left: -1px; right: -1px; height: 4px;
  background: repeating-linear-gradient(90deg, transparent 0 6px, rgba(120,110,80,0.18) 6px 8px);
}
.note .strike {
  text-decoration: line-through;
  text-decoration-color: var(--red);
  text-decoration-thickness: 2.5px;
  color: var(--ink-fade);
}
.note .scribble {
  position: absolute; right: -8px; top: 28px;
  font: 600 24px/1.15 var(--hand); color: var(--red);
  transform: rotate(6deg);
  background: #FFFBF1;
  padding: 6px 12px 4px;
  border: 1px dashed var(--red);
  white-space: nowrap;
}
.note .footnote {
  margin-top: 14px; padding-top: 12px;
  border-top: 1px dashed rgba(120,110,80,0.4);
  font: 500 13px/1.4 var(--mono);
  color: var(--ink-light);
  display: flex; gap: 8px;
}
.note .footnote .mark { color: var(--red); font-weight: 700; }

/* archive */
.archive {
  margin: 64px 64px 0;
  background: var(--bg);
  border-top: 2px solid var(--ink-strong);
  border-bottom: 1px solid var(--rule);
  display: grid;
  grid-template-columns: 168px 1fr;
  align-items: stretch;
}
.archive .stamp {
  background: var(--ink-strong); color: var(--bg);
  padding: 28px 18px;
  font: 700 12px/1.4 var(--mono);
  letter-spacing: 0.16em;
  text-transform: uppercase;
  text-align: center;
  display: flex; flex-direction: column; justify-content: center; gap: 10px;
}
.archive .stamp .label { border: 1px solid rgba(255,255,255,0.45); padding: 4px 6px; }
.archive .stamp .x { font: 700 64px/1 var(--serif); color: #C85042; }
.archive .body-area { padding: 26px 34px 30px; }
.archive .verdict {
  margin-top: 16px; padding-top: 12px;
  border-top: 1px dashed var(--rule);
  font: italic 600 19px/1.4 var(--serif);
  color: var(--red);
}

/* cross */
.cross {
  padding: 96px 64px 84px;
  border-top: 1px solid var(--rule);
  border-bottom: 1px solid var(--rule);
  margin-top: 64px;
}
.cross .mega {
  font: 900 200px/0.88 var(--serif);
  color: var(--ink-strong);
  letter-spacing: -0.045em;
}
.cross .mega .em {
  background: linear-gradient(180deg, transparent 60%, var(--amber-soft) 60%, var(--amber-soft) 90%, transparent 90%);
  padding: 0 6px;
}
.cross .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 56px; align-items: end; margin-top: 28px; }
.cross .left, .cross .right { border-top: 2px solid var(--ink-strong); padding-top: 20px; }
.cross .right .caption { font: italic 400 16px/1.45 var(--serif); color: var(--ink-light); margin-top: 12px; padding-left: 10px; border-left: 2px solid var(--amber); }

/* hero */
.hero {
  padding: 72px 64px 64px;
  border-top: 4px solid var(--blue-deep);
  margin-top: 56px;
  position: relative;
}
.hero .layout { display: grid; grid-template-columns: 7fr 5fr; gap: 44px; align-items: start; }
.hero .visual .caption { font: italic 400 16px/1.45 var(--serif); color: var(--ink-light); margin-top: 14px; padding-left: 12px; border-left: 2px solid var(--blue-deep); }
.hero .pull-quote {
  font: italic 700 38px/1.22 var(--serif);
  color: var(--blue-deep);
  margin: 18px 0 24px;
  padding: 8px 0 8px 22px;
  border-left: 4px solid var(--blue-deep);
  position: relative;
}
.hero .pull-quote::before {
  content: '\201C'; position: absolute;
  left: 4px; top: -42px;
  font: 700 100px/1 var(--serif);
  color: var(--blue-deep); opacity: 0.35;
}

/* closing */
.closing {
  padding: 80px 64px 84px;
  background: var(--paper);
  border-top: 6px double var(--ink-strong);
  margin-top: 64px;
  text-align: center;
}
.closing .approach {
  font: italic 400 26px/1.45 var(--serif);
  color: var(--ink-light);
  margin-bottom: 36px;
}
.closing .mega-name {
  font: 900 144px/0.95 var(--serif);
  color: var(--ink-strong);
  letter-spacing: -0.028em;
  margin-bottom: 18px;
}
.closing .en-name {
  font: 500 38px/1 var(--sans);
  color: var(--ink-light);
  letter-spacing: 0.04em;
  margin-bottom: 38px;
}
.closing .byline {
  display: flex; justify-content: center; align-items: baseline; gap: 28px;
  font: 600 14px/1.2 var(--mono);
  color: var(--ink-light);
  letter-spacing: 0.18em;
  text-transform: uppercase;
  padding: 22px 0;
  margin: 0 auto 32px;
  max-width: 760px;
  border-top: 1px solid var(--ink-strong);
  border-bottom: 1px solid var(--ink-strong);
}
.closing .byline strong { color: var(--ink-strong); font-weight: 700; letter-spacing: 0.12em; }
.closing .byline .sep { color: var(--ink-fade); font-weight: 400; }
.closing .closing-body {
  font: 400 22px/1.7 var(--serif);
  max-width: 760px;
  margin: 0 auto 30px;
  text-align: left;
}
.closing .epilogue {
  font: italic 500 26px/1.45 var(--serif);
  color: var(--ink-strong);
  margin-top: 24px;
}
.closing .epilogue::before { content: '— '; color: var(--red); font-weight: 700; }
```

### 4.2 HTML 骨架

```html
<div class="magazine-head">
  <div class="top-bar">
    <div class="left">
      <span class="badge">№ 01</span>
      <span>[领域 · 年份]</span>
    </div>
    <div class="right">[ENGLISH CATEGORY / SUBCATEGORY]</div>
  </div>
  <h1>[不剧透标题]<br>[第二行可选]</h1>
  <p class="deck">[italic 引言：暗示问题但不揭示答案]</p>
</div>

<section class="feature">
  <div class="visual">[SVG 大图，max-width 540px]</div>
  <div class="meta">
    <div class="kicker"><span class="num">01</span><span class="rule"></span>起点 · [时空锚点]</div>
    <h2 class="head-serif">[卡住的问题]</h2>
    <p class="lead">[一句简洁领题]</p>
    <div class="body-sans drop-cap">
      <p>[具体例子，drop cap 第一段第一字]</p>
      <p>[关键转折用 <em> 强调]</p>
      <span class="ask">[开放设问？]</span>
    </div>
  </div>
</section>

<aside class="note">
  <div class="kicker"><span class="num">02</span>第一次尝试</div>
  <h3 class="head-sans">[尝试的动作名]</h3>
  <div class="body-serif">
    <p>[思路 1]</p>
    <p>失败的关键词用 <span class="strike">删除线</span></p>
  </div>
  <div class="footnote"><span class="mark">¹</span><span>[失败的根本原因]</span></div>
  <div class="scribble">[一句红笔批注]</div>
</aside>

<section class="archive">
  <div class="stamp">
    <div class="label">EX-02</div>
    <div class="x">✕</div>
    <div class="case">Failed</div>
  </div>
  <div class="body-area">
    <div class="kicker"><span>第二次尝试</span></div>
    <h3 class="head-sans">[尝试的动作名]</h3>
    <div class="visual">[SVG 失败示意，max-width 720px]</div>
    <div class="body-serif"><p>[思路 + 失败]</p></div>
    <div class="verdict">[结案语]</div>
  </div>
</section>

<section class="cross">
  <h2 class="mega"><span class="em">等等</span>——</h2>
  <div class="grid">
    <div class="left">
      <div class="kicker" style="color: var(--amber);"><span class="num" style="background: var(--amber);">04</span>转折</div>
      <div class="body-serif">
        <p>[反向陈述]</p>
      </div>
      <span class="ask" style="color: var(--amber);">[转折设问？]</span>
    </div>
    <div class="right">
      <div class="visual">[SVG 反向姿态示意，max-width 460px]</div>
      <p class="caption">[caption]</p>
    </div>
  </div>
</section>

<section class="hero">
  <div class="layout">
    <div class="visual">
      [SVG 大幅 hero 图，宽度自适应]
      <p class="caption">[caption]</p>
    </div>
    <div class="text">
      <div class="kicker" style="color: var(--blue-deep);"><span class="num" style="background: var(--blue-deep);">05</span>顿悟</div>
      <h2 class="head-serif" style="color: var(--blue-deep); font-size: 50px;">[姿态名，不出现概念名]</h2>
      <div class="pull-quote">[核心句子]</div>
      <div class="body-serif drop-cap">
        <p>[洞察的具体表述]</p>
      </div>
    </div>
  </div>
</section>

<section class="closing">
  <p class="approach">[这种 X 的研究对象，叫——]</p>
  <h1 class="mega-name">[中文概念名]</h1>
  <div class="en-name">[English Name]</div>
  <div class="byline">
    <span><strong>[人名]</strong></span>
    <span class="sep">·</span>
    <span>[年份]</span>
    <span class="sep">·</span>
    <span>[机构]</span>
    <span class="sep">·</span>
    <span>[文献]</span>
  </div>
  <div class="closing-body">
    <p>[它打开了什么]</p>
    <p>[它换了什么眼睛]</p>
  </div>
  <p class="epilogue">[诗意余韵，不元自指]</p>
</section>
```

写入：`/tmp/ljg_cast_sketchnote_{name}.html`

---

## 步骤 5：截图（单阶段）

新风格不再使用橙色弯曲箭头。叙事流通过 page rules + 编号传达，**单阶段渲染**：

```bash
node assets/capture.js /tmp/ljg_cast_sketchnote_{name}.html ~/Downloads/{name}.png 1080 1500 fullpage
```

`fullpage` 让 Playwright 自动适应内容总高度。

旧版的 measure.js 两阶段流程（先空跑测高再写 SVG 箭头）已**废弃**——本模式不需要。

---

## 步骤 6：自检（逐项）

### 公理项（任何一条不过 → 重做）
- [ ] 公理 1：具体物理约束（不是"领域困境"等抽象腔）
- [ ] 公理 2：至少一次失败，且 station 2 与 3 形态不同（note + archive）
- [ ] 公理 3：标题不剧透 + 命名站点最后
- [ ] 公理 4：现在视角，无"100 年后"等上帝视角
- [ ] 公理 5：文字克制，无元自指（不出现"你刚才发明了它"等点题语）

### 视觉项（杂志骨架）
- [ ] 6 个站点，每个用不同 layout 模具：feature / note / archive / cross / hero / closing
- [ ] 4 字族同时使用：Serif + Sans + Mono + Hand
- [ ] 必备装饰：kicker（含 mono num 方块）+ drop cap + byline + stamp
- [ ] Station 2 (note)：红笔删除线 + scribble + footnote
- [ ] Station 3 (archive)：黑色印章 ✕ + verdict 红色 italic
- [ ] Station 4 (cross)：「等等——」200px Serif + amber 高亮
- [ ] Station 5 (hero)：pull-quote 蓝色 + 浮动大引号
- [ ] Station 6 (closing)：mega-name ≥ 130px + byline 上下细线 + epilogue
- [ ] 节奏：开阔（feature） → 紧（note） → 紧（archive） → 爆（cross） → 开阔（hero） → 静（closing）
- [ ] 颜色 ≤ 4 主色（红 + 蓝 + amber + 中性）
- [ ] 无纯黑 #000，标题用 #0F0F0F

### 技术项
- [ ] 单阶段渲染（不用 measure.js）
- [ ] PNG 高度通常 4500-6500（杂志风允许更高，节奏需要）
- [ ] 字体齐全：Noto Serif SC + Noto Sans SC + JetBrains Mono + Caveat
- [ ] 中文显示优雅（无方块字）

---

## 与其他模具的边界

- 跟 `-i`（信息图）：信息图是数据可视化，本模式是**概念叙事**
- 跟 `-w`（白板）：白板是推理过程纵向展开，本模式是**问题→失败→转折→顿悟→命名的探索路径**
- 跟 `-c`（漫画）：漫画追求黑白动态分镜，本模式追求**编辑设计 + 叙事张力**

不知道用哪个时，问：「读者读完，是带走一个**视角**，一段**推理**，还是一段**期刊专题式的体验**？」

期刊专题式 → 本模式。

---

## Known Pitfalls

- [2026-04-29] SVG.relations viewBox 必须对齐实测页面高度——凭估算会导致箭头与 HTML 标签错位（误差 30-50%）。（历史教训，新版已废弃箭头流程）
- [2026-05-01] flex 容器默认让 .station 撑满宽度——必须给所有 .station 变体显式 max-width，否则 align-self 失效。（历史教训，新版用 grid + margin auto）
- [2026-05-01] 「公理 1：真问题」最容易被偷懒——容易写成"X 领域有个问题"。检查方法：删掉一切抽象，只留具体物理约束（"开了就炸"、"开了就死"）。
- [2026-05-01] 「公理 3：命名在后」最容易被剧透——设计 layout 时，命名站点放最下面（路径终点），且标题不能出现概念名。
- [2026-05-01] 「公理 5：文字克制」最容易触雷——AI 在 closing 段会自动写成"你以为你刚才学到了一个概念。其实你刚才不得不发明了它"。这种元自指破坏体验，禁止。要余韵就写诗意句（"于是，你看见了山"），不写元论。 (from: 20260501-180500_cast-potential-function-sketchnote)
- [2026-05-01] 旧版"重新发明 / 重新分娩 / 不得不发明它"等元自指 framing 已彻底淘汰——文档和输出文字都不再用此类自指话术。 (from: 20260501-180500_cast-potential-function-sketchnote)
- [2026-05-01] 杂志风排版需要四字族同时在场（Serif/Sans/Mono/Hand）。如果输出全是 Sans，回到 AI 单一字族的均质感。Mono 用于 kicker / num / byline / stamp，Hand 用于 ask / scribble / caption，缺一不可。 (from: 20260501-180500_cast-potential-function-sketchnote)
- [2026-05-01] 两个失败站点必须形态不同——station 2 用 note（便签批注），station 3 用 archive（档案标签）。两个都用 note 或都用 archive，节奏不出来。 (from: 20260501-180500_cast-potential-function-sketchnote)
- [2026-05-01] Drop cap 用 `::first-letter` 选第一段第一字。如果 pull quote 在 body 之前，drop cap 不会作用于 pull quote——只作用于其后第一段。这是预期行为。 (from: 20260501-180500_cast-potential-function-sketchnote)
