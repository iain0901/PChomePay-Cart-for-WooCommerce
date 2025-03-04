# PChomePay Gateway for WooCommerce

讓 WooCommerce 可以使用 PChomePay支付連 進行結帳！水啦！！

## 系統需求

- PHP 5.6+
- WordPress 4.3+
- WooCommerce 3.0+

## 安裝

1. 將外掛上傳至 `/wp-content/plugins/` 目錄，或直接透過 WordPress 外掛安裝介面進行安裝。
2. 在 WordPress 後台啟用外掛。
3. 前往 WooCommerce > 設定 > 付款，設定 PChomePay 付款閘道。

## PI 錢包付款方式使用說明

### 設定方法
1. 在 WordPress 管理後台，前往 **WooCommerce > 設定 > 付款**
2. 點擊 **PI 錢包** 付款方式
3. 在設定頁面中：
   - 啟用/停用 PI 錢包付款方式
   - 設定標題（顯示在結帳頁面上）
   - 設定描述（顯示在結帳頁面上）
4. 點擊 **保存設定** 按鈕

### 注意事項
- PI 錢包付款方式與 PChomePay 支付連付款方式共用 APP ID 和 SECRET 設定
- 請確保已在 PChomePay 支付連付款方式中設定了正確的 APP ID 和 SECRET
- 如果您使用了快取插件，請清除快取以確保修改生效

### 設定頁面說明
PI 錢包付款方式設定頁面包含以下欄位：

1. **啟用/停用**：啟用或停用 PI 錢包付款方式
2. **標題**：設定在結帳頁面上顯示的標題，預設為「拍錢包付款」
3. **描述**：設定在結帳頁面上顯示的描述，預設為「使用拍錢包進行付款」

設定完成後，請點擊「保存設定」按鈕。

## 版本更新說明

### 1.6.4
- 添加了 PI 錢包付款方式的標題和描述設定功能
- 移除了自定義的 PI 錢包設定頁面，改用 WooCommerce 標準設定頁面
- 修改了 PI 錢包付款方式的過濾器函數，使其從設定中獲取值

#### 1.6.4 版本修改詳情
1. **PI 錢包付款方式設定頁面**
   - 現在可以通過 WooCommerce 標準設定頁面設定 PI 錢包付款方式的標題和描述
   - 路徑：WooCommerce > 設定 > 付款 > PI 錢包

2. **修改內容**
   - 修改了 PI 錢包 Gateway 類別的 `init_form_fields` 方法，添加標題和描述欄位
   - 修改了 PI 錢包 Gateway 類別的建構函數，使其從設定中獲取標題和描述
   - 更新了設定鏈接，指向 WooCommerce 標準設定頁面
   - 修改了過濾器函數，使其從設定中獲取值

3. **使用說明**
   - 啟用 PI 錢包付款方式後，可以在設定頁面中設定標題和描述
   - 設定的標題和描述將顯示在結帳頁面上
   - 請清除快取以確保修改生效

### 1.6.3
- 原始版本

This plugin can quickly add [PChomePay](https://www.pchomepay.com.tw/) payment to your WooCommerce site!

## Features

Currently supports the following features:

* Requesting payments
* Refunds
* Order audit

This plugin supports refunds directly from the WooCommerce Order backend.\
When you processing a refund within its payment method is ATM, remember to give the refund URL to your purchaser.\
And the purchaser will be lead to a refund form via the URL to complete the refund procedure.\
You can find the refund URL in order page which meta title is "pchomepay_refund_url".

## Feedbacks?

Please raise new issues for any problems or feedbacks you may have. Fixes and enhancements are welcomed through pull requests!