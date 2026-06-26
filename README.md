# QuizWeb: 靜態單頁式多選題測驗系統

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-2.0.0-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=flat&logo=javascript&logoColor=F7DF1E)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)

本專案為一款無須後端伺服器支援的靜態網頁多選題測驗系統，涵蓋資訊網路與企業管理等多門學科。所有題目皆採用選擇題格式，支援 A-E 五選項作答，僅需瀏覽器即可運行，適用於學術考試準備與個人題庫建置。

## 更新內容 (v2.0)

* **新增資訊網路 Chapter 2 題庫** (`itch2.html`)：涵蓋網路基礎架構與通訊協定相關考題
* **新增資訊網路 Chapter 8 題庫** (`itch8.html`)：涵蓋網路安全與管理相關考題
* **新增企業管理期末考題庫** (`ba-final.html`)：涵蓋企業管理學期末範圍考題
* **新增測驗頁面模板** (`quiz-template.html`)：方便快速擴展新科目題庫

## 題庫列表

| 科目 | 頁面 | 章節 |
|------|------|------|
| 資訊網路 | [it-test.html](it-test.html) | Ch.1 期中考 |
| 資訊網路 | [it-test2.html](it-test2.html) | Ch.5 期中考 |
| 資訊網路 | [itch2.html](itch2.html) | Ch.2 |
| 資訊網路 | [itch8.html](itch8.html) | Ch.8 |
| 企業管理 | [ba-test.html](ba-test.html) | 期中考 |
| 企業管理 | [ba-final.html](ba-final.html) | 期末考 |

## 系統核心功能

* **多選題型支援**：全題庫採用 A-E 多選項格式，涵蓋資訊網路與企業管理兩大學科領域
* **深 / 淺色主題切換**：內建介面主題切換功能，並支援本地狀態記憶。
* **雙重測驗模式**：
  * **測驗模式**：隱藏答案，點擊選項後提供即時對錯反饋。
  * **讀題模式**：直接標示正確答案，提升考前複習效率。
* **進度自動儲存**：作答紀錄自動寫入瀏覽器 LocalStorage，確保跨工作階段資料不遺失。
* **錯題重練機制**：自動篩選作答錯誤之題目，提供針對性之複習測驗。
* **隨機題序出題**：支援打亂原始題目順序，提升測驗鑑別度。
* **鍵盤快捷鍵支援**：支援 A-E 鍵作答與方向鍵切換題目，提升操作效率。
* **響應式網頁設計 (RWD)**：介面自動適配桌上型電腦、平板與行動裝置。

## 快速啟動

本系統完全由靜態檔案構成，無須建置 Node.js 或資料庫環境。

1. 取得專案：透過 Git Clone 或下載 ZIP 檔取得原始碼。

2. 運行系統：直接以瀏覽器開啟 index.html 或各科測驗頁面即可開始使用。

## 自訂題庫配置

題庫資料採用 JSON 格式儲存，存放於 `question-database/` 目錄下。欲新增自訂題庫，可參考 `quiz-template.html` 模板快速建立新頁面。

資料格式範例：

    [
      {
        "N": "001",
        "Q": "請問 Tailwind CSS 的主要特色是什麼？",
        "A": "C",
        "H": "",
        "O": [
          "A) 是一個後端框架",
          "B) 需要依賴 jQuery 才能運行",
          "C) 是一個 Utility-first 的 CSS 框架",
          "D) 只能用於開發手機 App"
        ]
      }
    ]

## 技術架構

* **UI 框架**：[Tailwind CSS](https://tailwindcss.com/) (透過 CDN 載入)
* **核心邏輯**：Vanilla JavaScript (ES6+)
* **狀態管理**：Browser LocalStorage API

## 授權與作者

* **作者**: [@hongfu553](https://github.com/hongfu553)
* **授權條款**: 本專案採用 MIT 授權條款，詳細資訊請參閱 LICENSE 檔案。