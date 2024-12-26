# Phone Number Validation and Ownership Check with AWS Lambda

## 簡介
這是一個使用 Node.js 編寫的 AWS Lambda 函數，用於驗證台灣手機號碼並檢查該號碼是否已經獲得相應的優惠。此專案涵蓋了基本的錯誤處理及與 AWS S3 的互動，以讀取優惠擁有者資料。

## 功能
- 驗證用戶輸入的手機號碼格式。
- 檢查該號碼是否已經領取過優惠。
- 從 AWS S3 中讀取已經儲存的優惠擁有者資料。
- 確保適當的 CORS 頭部分配，以支持跨域請求。

## 安裝與使用方式

### 先決條件
請確保你已經安裝了 Node.js 和 npm。

### 步驟
1. 將專案代碼下載到本地環境。
2. 在 AWS 俱樂部創建一個 IAM 用戶，為其配置適當的S3訪問權限，並取得 `Access Key ID` 和 `Secret Access Key`。
3. 在程式碼中填入該 IAM 用戶的 `Access Key ID`, `Secret Access Key`, 以及 S3 資源的 `Bucket` 與 `Key`。
4. 部署程式碼至 AWS Lambda。
5. 配置 API Gateway 以觸發此 Lambda 函數。
6. 使用 Postman 或其他 API 測試工具來發送 POST 請求測試功能。

### 示例請求
```json
{
    "value": "0912345678"
}
```

## 必要的依賴模組清單
- aws-sdk

請確保在你的 `package.json` 中有對 `aws-sdk` 的依賴。

## 授權條款
本專案採用 MIT 授權條款。詳情請參閱 [LICENSE](LICENSE) 文件。 

如有任何問題或建議，歡迎發起討論或提出問題！