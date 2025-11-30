## BuyTicket - 線上演唱會模擬購票系統 🎫

這是一個基於 HTML5, Tailwind CSS 與 Google Firebase 構建的 Client-Server 架構 購票系統。
本專案模擬了完整的購票流程，包含座位視覺化選擇、即時庫存更新、交易處理與票券管理，並採用正規化的資料庫結構設計。

### 專案符合規格說明

#### 本系統針對課程要求進行設計：

**Client-Server 架構：**

Client (前端)：使用者透過瀏覽器操作網頁。

Server (後端/資料庫)：使用 Google Cloud Firestore 託管資料與邏輯，透過 API 進行遠端通訊。

**遠端資料庫連接：**

資料庫部署於雲端，非本機 localhost 環境，確保任何網路環境皆可存取。

**SQL 關聯式邏輯設計：**

雖然底層採用高效能 NoSQL，但資料結構嚴格遵循 SQL Schema 設計（包含 User, Ticket, Event 等實體關聯）。

### 核心功能

**視覺化選位 (Visual Seat Map)：**

動態生成座位表，即時顯示 Sold (已售出) 與 Available (可選) 狀態。

透過網路即時與雲端資料庫同步。

**即時資料庫 (Real-time Database)：**

使用 Google Cloud Firestore 存儲所有資料。

支援 ACID 概念的交易處理（同時寫入訂單與更新座位狀態）。

**會員系統：**

支援自動註冊與登入驗證（密碼驗證機制）。

「我的票券」功能可查詢歷史訂單與付款方式（信用卡/轉帳）。

**動態售罄偵測：**

系統後端會自動計算各場次銷售狀況，若座位全數售出，首頁自動標示 SOLD OUT。

### 技術架構

Frontend (Client): Native HTML5, JavaScript (ES6 Modules)

Styling: Tailwind CSS (CDN)

Backend / Database (Server): Firebase Firestore (NoSQL based on SQL logic)

Hosting: GitHub Pages
