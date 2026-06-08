# Final
# 智慧長照服藥紀錄 LINE Bot 系統

這是一個專為長照長輩設計的智慧服藥回報系統。長輩只需在 LINE 官方帳號點擊或輸入「已吃藥」，系統便會自動將時間、使用者的 LINE UID 以及服藥狀態即時寫入雲端 Google 試算表後台，方便家屬或照護人員遠端監控與追蹤。

## 🚀 功能特點
- **零學習成本**：長輩操作熟悉的 LINE 介面即可完成回報。
- **即時雲端紀錄**：整合 Google Sheets API，資料同步不延遲。
- **防呆偵錯機制**：自動過濾非目標訊息，給予長輩溫馨引導。

## 📦 檔案結構
- `app.py`          # Flask 後端主程式（負責接收 LINE Webhook 與處理邏輯）
- `app.json`        # 存放 LINE Channel Secret 與 Access Token 的金鑰檔
- `creds.json`      # Google Cloud 服務帳戶憑證（請勿外流）
- `requirements.txt` # 本專案所需之 Python 套件清單

## 🔧 本機執行步驟

### 1. 環境準備
請確保您的電腦已安裝 Python 3.10+，並在終端機執行以下指令安裝所需套件：
```bash
pip install flask line-bot-sdk gspread oauth2client
