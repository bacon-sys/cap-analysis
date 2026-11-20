# 國中教育會考 學校數據分析

上傳心測中心提供的「國中教育會考」學校報告（3 份 PDF＋6 份 Word 試題分析），直接在網頁上產生圖表化的數據分析。

網站：https://bacon-sys.github.io/cap-analysis/

## 資料不會外流

- 整個網站只有 `index.html` 一個檔案，沒有伺服器、沒有資料庫。
- 檔案的讀取、解析、計算全部在使用者自己的瀏覽器裡完成，關閉網頁即清除。
- 網頁開頭的安全規則（Content-Security-Policy：`connect-src 'none'`、`form-action 'none'`）要求瀏覽器禁止本網頁對外傳送任何資料。
- 可自行驗證：打開網頁後斷網，再上傳檔案，分析仍可完成。
- 網頁開啟時會從 jsDelivr 下載公開的程式庫、從 Google Fonts 下載字型；這些下載在選檔之前發生，不含任何學校資料。

## 使用的程式庫

Chart.js 4.4.1、JSZip 3.10.1、pdf.js 4.10.38（皆由 jsDelivr 載入）。
