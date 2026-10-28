# TASK.md — Just Play The Guitar 官方網站（工作指示）

> 由緣一（設計總監）寫俾 OpenCode（編寫工人）。照呢份做，唔好自由發揮。

## 任務

建立一個**單頁式品牌網站**,結合:
- 🎸 Just Play The Guitar 結他課程(主帳號 IG: justplaythe_guitar)
- 🛒 JP 結他自家手工品牌商品(IG: jp_guitarstudio_hk)

**交付**:一個完整 HTML 檔案 `index.html`(內嵌 CSS+JS,可直接開瀏覽器睇)。

## 客戶決定(鐵則)

1. **一個網站**,唔係兩個
2. **唔要標語/口號**——第一屏唔好放「讓音樂...」「Feel the music...」呢類 slogan
3. **要有質感**——黑沉木色調、暗黑系、型格、專業。唔係可愛風、唔係鮮色
4. **繁體中文**為主(英文只可做輔助小字)
5. Mobile-first(IG 客多數手機)

## 品牌資料(真實資料,唔好老作)

### 課程(主帳號 @justplaythe_guitar,10K粉)
- 定位:結他課程 ｜ 指彈 ｜ 伴奏 ｜ 樂理 ｜ 編譜
- **小組班**:$1080/8堂、3-4人班、牛頭角創業街36號華基中心1208 Studio、一至日有班(一班一星期一堂)、適合新手(學習伴奏 chord、睇譜、入門 fingerstyle)、手把手教學、氣氛好
- **個人班**:本身有底 or 想快上手進步、彈性時間
- **試堂**:DM 約、收生中
- 互動玩法:留言密語攞 PDF(「留言*5*」「留言^冬天^」)

### 商品(品牌帳號 @jp_guitarstudio_hk,289粉)
- 定位:結他零售 ｜ 結他課程 ｜ JP結他自家手工品牌
- 產品線(真實):
  1. **Randon AS-GC+** — 41吋 GA桶缺角單板,$1,399 起,歐洲雲杉單板面板+桃花芯背側,指板「靈蛇」鑲嵌,型格,音色共鳴飽滿,性價比高,只此10枝
  2. **Randon RG-19SAC** — 全單板:歐洲雲杉+印度玫瑰木單板,「螢火蟲」鑲嵌,共鳴厚實飽滿,高端玫瑰木紋理
  3. **手工結他系列** — 精選德國雲杉面板+印度玫瑰木背側+非洲桃花芯琴頸+烏木指板,650mm弦長,彩貝鑲嵌
  4. (預留「更多型號」位)

## 設計方向(Surface: Decide + Explore)

- **Color**: 深炭黑/瀝青底 + 原木深棕/琥珀 accent + 米白字
  - bg: #0E0D0B (黑)
  - surface: #17140F (深木)
  - accent: #C89B5A (琥珀/啞金)
  - text: #F0E9DD (米白)
  - muted: #8A8377
- **Typography**: 標題用有性格嘅 serif 或 display font(Playfair Display / Cormorant / Noto Serif TC),正文用清晰 sans(Noto Sans TC),mono 只做規格表小字
- **質感關鍵**:大量留白、大呎吋標題、細字距(letter-spacing)、細線分隔、hover 微動效。**唔好用**:紫藍漸層、玻璃擬態、三張等權 icon 卡、發光 glow
- **商品圖片**:用 CSS 漸層/陰影做 placeholder(實際相片後補),但設計要留到「相片位」俾客戶之後換
- **報名形式**:表單(姓名/電話/心儀時段/程度/課程選擇)→ 提交後顯示成功 message(資料可用 mailto: 或 localStorage demo)

## 頁面結構(單頁 scroll)

1. **Nav** — 極簡:課程 / 商品 / 報名(錨點scroll) + 右邊「DM」button(link去 https://www.instagram.com/justplaythe_guitar/)
2. **第一屏(Hero)** — 唔用標語。黑底大字「Just Play The Guitar」+ 細字定位「結他課程 · 指彈 · 伴奏 · 樂理」+ 狀態「收生中」badge + CTA「開始試堂」scroll去報名。背景可以用結他形狀/木紋 texture(純CSS亦得)
3. **課程區** — 小組班卡(收費/人數/地點/適合)＋ 個人班卡 + 課程內容條目(指彈/伴奏/樂理/編譜)
4. **商品區** — 結他目錄 grid:Randon AS-GC+ / RG-19SAC / 手工系列 每張卡(相位+型號+價錢+一句賣點+「查詢」button)
5. **教學/互動區**(可選)— 「留言攞譜」玩法令用戶 DM
6. **報名區** — 正式表單 + 地點資訊 + IG DM 替代
7. **Footer** — 兩個 IG link + 版權

## 質素要求(Slop 檢查)

唔可以有:
- ❌ 紫藍漸層背景
- ❌ glassmorphism blur
- ❌ 三張等權 icon+標題+一句 卡陣(課程/商品要用真層次:呎吋/粗幼/間距)
- ❌ 發光 glow 特效
- ❌ 超大字數塞空間(monument stat)
- ❌ 預設 Inter/system-ui
- ✅ 要有真留白、真字型層次、克制動效(hover fade/translate 少少)、prefers-reduced-motion 處理
- ✅ responsive(手機 44px hit target 以上)
- ✅ 所有內容用呢份 brief 嘅真實資料,唔好自己作價錢/地點/人名

## 驗證

- 完成後確認檔案存在、可開
- 自己檢查 slop 10 項,唔合格就改到合格先停
