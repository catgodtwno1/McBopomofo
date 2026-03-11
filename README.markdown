# OpenVanilla McBopomofo 小麥注音輸入法

## 系統需求

小麥注音輸入法可以在 macOS 10.15 以上版本運作。如果您要自行編譯小麥注音輸入法，或參與開發，您需要：

- macOS 14.7 以上版本
- Xcode 15.3 以上版本
- Python 3.9 (可使用 Xcode 安裝後內附的，或是使用 homebrew 等方式安裝)

## 開發流程

用 Xcode 開啟 `McBopomofo.xcodeproj`，選 "McBopomofo Installer" target，build 完之後直接執行該安裝程式，就可以安裝小麥注音。

第一次安裝完，日後程式碼或詞庫有任何修改，只要重複上述流程，再次安裝小麥注音即可。

要注意的是 macOS 可能會限制同一次 login session 能 kill 同一個輸入法 process 的次數（安裝程式透過 kill input method process 來讓新版的輸入法生效）。如果安裝若干次後，發現程式修改的結果並沒有出現，或甚至輸入法已無法再選用，只要登出目前帳號再重新登入即可。

## 中英文切換鍵設定（Fork 新增功能）

本 Fork 新增了**中/英文輸入切換鍵**的可選設定功能：

- **Shift（預設）**：單擊 Shift 鍵即可快速切換中文/英文輸入模式。切換時螢幕會顯示「中」或「英」提示。
- **Caps Lock**：沿用原版小麥注音的 Caps Lock 切換行為。

### 使用方式

1. 開啟小麥注音的「偏好設定」
2. 在「基本」頁面底部找到「中/英切換鍵」選項
3. 選擇 **Shift（單擊切換）** 或 **Caps Lock**

### 注意事項

- 使用 Shift 切換模式時，需要**單獨按下並放開 Shift 鍵**（按住不超過 0.5 秒且中間不按其他鍵）才會觸發切換
- 按住 Shift 的同時按其他鍵（如 Shift+A 打大寫字母）不會觸發切換
- 切換到英文模式後，所有按鍵會直接輸出英文字元
- 切換輸入法或重新啟動輸入法時，會自動重置為中文模式

## 社群公約

歡迎小麥注音用戶回報問題與指教，也歡迎大家參與小麥注音開發。

首先，請參考我們在「[常見問題](https://github.com/openvanilla/McBopomofo/wiki/常見問題)」中所提「[我可以怎麼參與小麥注音？](https://github.com/openvanilla/McBopomofo/wiki/常見問題#我可以怎麼參與小麥注音)」一節的說明。

我們採用了 GitHub 的[通用社群公約](https://github.com/openvanilla/McBopomofo/blob/master/CODE_OF_CONDUCT.md)。公約的中文版請參考[這裡的翻譯](https://www.contributor-covenant.org/zh-tw/version/1/4/code-of-conduct/)。

## 軟體授權

本專案採用 MIT License 釋出，使用者可自由使用、散播本軟體，惟散播時必須完整保留版權聲明及軟體授權（[詳全文](https://github.com/openvanilla/McBopomofo/blob/master/LICENSE.txt)）。
