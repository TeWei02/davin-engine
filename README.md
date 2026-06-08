# Davin Engine — 全自動 AI 作品產出引擎

> 一位特殊選才生的 30 天實驗：把所有作品產出完全交給 AI 自動化。

[![GitHub Pages](https://img.shields.io/badge/Live-Portfolio-blue)](https://tewei02.github.io/Davin-daily-briefs/)
[![HackMD](https://img.shields.io/badge/Read-HackMD-orange)](https://hackmd.io/@j327ajzSQPGOIUCOmAHPDQ)
[![Dev.to](https://img.shields.io/badge/Follow-Dev.to-black)](https://dev.to/_398176bdd5bb8ce900446)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## 系統架構

```
凌晨 2:00 (cron)
    │
    ├── CTF 解題引擎 (ctf_solver.py)
    │   └── SiliconFlow DeepSeek-V4-Flash 模擬 7 種題型
    │
    ├── Portfolio 產出引擎 (portfolio_generator.py)
    │   ├── 資訊 / 資安
    │   ├── 商管 / 創業
    │   ├── 語言 / 人文
    │   ├── 物理 / 數學
    │   ├── 藝術 / 設計
    │   └── GitHub 開源專案
    │
    ├── 個人網站重建 (portfolio_site.py)
    │
    ├── YouTube 引擎 (yt_agency.py)
    │
    └── Premium 生態閉環 (eco_closer.py)
        ├── HackMD / Dev.to 跨平台發布
        ├── SEO 優化 (sitemap + robots + Schema)
        ├── 跨平台互相連結
        └── AI 自動回覆讀者留言
```

## 技術棧

| 層級 | 技術 |
|------|------|
| LLM | SiliconFlow API (DeepSeek-V4-Flash) |
| 影片 | MoviePy + Pillow + FFmpeg |
| 分發 | HackMD API / Dev.to API / GitHub API |
| 排程 | macOS LaunchAgent + cron |
| 前端 | GitHub Pages (純 HTML/CSS/JS) |

## 快速開始

### 環境變數
```bash
export HACKMD_TOKEN="your_hackmd_token"
export DEVTO_KEY="your_devto_key"
export SILICONFLOW_KEY="your_siliconflow_key"
export GITHUB_TOKEN="your_github_token"
```

### 安裝
```bash
pip install requests moviepy Pillow imageio-ffmpeg
```

### 手動執行
```bash
python3 ctf_solver.py
python3 portfolio_generator.py
python3 portfolio_site.py
python3 yt_agency.py
python3 premium_publisher.py
python3 eco_closer.py
```

### 自動排程
```bash
# macOS LaunchAgent
cp com.portfolio.daily.plist ~/Library/LaunchAgents/
launchctl load ~/Library/LaunchAgents/com.portfolio.daily.plist
```

## 30 天產出統計

- 30 篇技術部落格
- 30 份商業分析報告
- 30 篇英文 Essay
- 30 份數理研究報告
- 30 份 CTF Writeup
- 30 支 YouTube 影片
- 9 個 GitHub 專案 README
- 1 個自動更新個人網站

**總成本：< NT$200/月**

## 授權

MIT License — 歡迎 Fork、改寫、商用。

---

*Built by [柯德瑋 Te-Wei Ko](https://tewei02.github.io/) · 清大拾穗 × 交大百川 特殊選才*
