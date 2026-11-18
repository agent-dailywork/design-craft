# design-craft

供不同 AI Agent 使用的視覺設計方法與參考文件，涵蓋平面、網站介面、圖解、設計系統與交付驗收。內容使用 Markdown、標準 HTML/CSS 與 SVG，不需要指定模型、專屬畫布語法或供應商品牌資產。

## 使用方式

- **支援檔案式 Skills 的 Agent**：將整個 `design-craft` 資料夾放入該 Agent 文件指定的技能目錄，保留 `SKILL.md` 與 `references/` 的相對位置。安裝目錄、啟用與自動觸發方式依各 Agent 而異。
- **可讀取檔案但沒有 Skills 的 Agent**：在專案指令或對話中指定先讀 `design-craft/SKILL.md`，再按任務讀取其中列出的參考頁。
- **只能對話的 Agent**：提供 `SKILL.md` 與任務所需參考頁的內容，要求產出設計規格或原始碼。此模式不代表已建立檔案或完成渲染。

可使用下列指令：

> 請先讀取 `design-craft/SKILL.md`，依本次任務選讀 references，再使用目前可用的工具製作與驗收。請說明無法執行的檢查或交付項目。

## 能力與交付

| 環境能力 | 可採用的工作方式 |
|---|---|
| 讀寫檔案 | 製作 HTML/CSS、SVG 或環境支援的原始檔 |
| 原生設計畫布 | 依該工具的實際 API 建立文字、圖形、畫板與元件 |
| 瀏覽器或渲染器 | 以目標尺寸檢查字型、溢出、互動與手機版 |
| PDF／圖片匯出 | 匯出並檢查目標檔；印刷規格依印刷廠要求 |
| 無上述工具 | 提供規格或原始碼，明確標記未執行項目 |

這是一套通用指令與設計方法；不提供各平台的自動安裝器，也不保證所有 Agent 有相同工具或自動載入能力。

## 結構

`SKILL.md` 是唯一技能入口；`references/` 是按需載入的通用參考。參考頁不是另一組獨立技能，不需要全部常駐上下文。

| 參考頁 | 用途 |
|---|---|
| [craft.md](references/craft.md) | 視覺方向、構圖、文案與介面精修 |
| [format.md](references/format.md) | 標準 HTML/CSS、響應式與資產管理 |
| [canvas-workflow.md](references/canvas-workflow.md) | 多畫板、增量修改與共同編輯 |
| [diagrams.md](references/diagrams.md) | 節點、箭頭與可編輯圖解 |
| [print.md](references/print.md) | 實體尺寸、出血、PDF 與分頁 |
| [questions.md](references/questions.md) | 適量提問與合理預設 |
| [view-state.md](references/view-state.md) | 辨認目前視圖與選取目標 |
| [design-system-components.md](references/design-system-components.md) | Token、元件與資產依賴 |
| [color-system.md](references/color-system.md) | 品牌中立的色彩角色與對比 |
| [typography.md](references/typography.md) | 字體選擇、CJK 與字型載入 |
| [derived-deliverables.md](references/derived-deliverables.md) | 衍生版本、來源關聯與交付 |
