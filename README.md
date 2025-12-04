# SoulTalk Tool v2.0

模組化字幕生成工具，支援 MV 和語音兩種模式。

---

## 🚀 部署到 Zeabur

### 1. 設定 Volume（重要！）

| 設定項目 | 值 |
|---------|-----|
| Volume ID | `data` |
| Mount Path | `/app/data` |
| Port | `8080` |

### 2. 環境變數

```bash
PORT=8080
```

---

## 📁 專案結構

```
soultalk-v2/
├── server/                 # 後端
│   ├── index.js           # 主程式
│   ├── services/          # 服務模組
│   ├── integrations/      # 外部整合
│   ├── notifications/     # 通知系統
│   └── prompts/           # AI 提示詞
├── public/                 # 前端頁面
├── data/config/            # 設定檔
├── package.json
└── zeabur.json
```

---

## 🌐 頁面

| 路徑 | 功能 |
|------|------|
| `/` | 主頁 |
| `/mv.html` | MV 操作 |
| `/audio.html` | 語音操作 |
| `/settings.html` | 設定 |
| `/subtitle-styles.html` | 字幕樣式 |
| `/logs.html` | 系統日誌 |

---

## 🔌 API

### MV 模式
```
GET  /api/mv/fetch/:code
POST /api/mv/transcribe
POST /api/mv/match
POST /api/mv/upload
```

### 語音模式
```
GET  /api/audio/fetch/:code
POST /api/audio/transcribe
POST /api/audio/match
POST /api/audio/upload
```

### 設定
```
GET  /api/config
GET  /api/config/:name
POST /api/config/:name
```

### 匯出/匯入
```
GET  /api/export/json
GET  /api/export/html
POST /api/import/json
```

---

## 📦 版本

- **v2.0.0** - 模組化架構
