# analysis/hk-stock/

港股投資分析存檔 — Ruga 為 Bjai 整理嘅市況分析。

## Naming Convention

```
yyyymmddhhmm_#_about.md

日期時間 (開始分析時) | 序號 | 時段標籤
```

### 時段標籤（about）

| 標籤 | 用途 |
|------|------|
| `intraday` | 即日分析（交易時段內） |
| `overnight` | 美股收市後 / 盤後分析 |
| `premarket` | 開市前展望 |
| `weekly` | 週度回顧/展望 |
| `special` | 特別事件分析（突發新聞、深度研究等） |

### 序號（#）

同一日同一時段如果有多份分析，用 01, 02, 03... 順序。

### 範例

```
202605180900_01_intraday.md    ← 5月18日 09:00 第一份即日分析
202605182000_02_overnight.md   ← 5月18日 20:00 美股盤後分析
202605190800_01_premarket.md   ← 5月19日 08:00 開市前展望
202605230900_01_weekly.md      ← 5月23日 週度回顧
```

## 用法

- Ruga 做完分析就寫入呢個 folder，commit & push
- 需要翻查之前嘅分析直接睇 GitHub，唔使塞 memory
- 每份分析自成一個完整文件，包含數據、分析、策略建議
