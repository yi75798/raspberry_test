# Gemini 啟動說明

本文件說明了幾種常見的 Gemini 啟動方式。請根據您的安裝和使用情境選擇合適的方法。

## 1. 從可執行檔啟動

如果 Gemini 已經編譯成一個獨立的可執行檔，您可以直接運行它。

```bash
./gemini  # 如果可執行檔在當前目錄
/path/to/gemini/executable/gemini # 如果可執行檔在特定路徑
```

## 2. 使用套件管理器啟動 (如果適用)

如果 Gemini 是透過套件管理器 (例如 `npm`, `pip`, `apt`, `brew` 等) 安裝的，通常會有一個命令可以直接啟動。

### 範例：Node.js 應用

```bash
npm start
```

### 範例：Python 應用

```bash
python -m gemini_app # 假設模組名稱為 gemini_app
```

## 3. 從原始碼啟動

如果從原始碼運行 Gemini，您需要先安裝所有依賴項，然後執行主程式。

### 範例：Python 專案

1.  安裝依賴 (通常在 `requirements.txt` 中定義):
    ```bash
    pip install -r requirements.txt
    ```
2.  運行主程式:
    ```bash
    python main.py # 假設主程式為 main.py
    ```

### 範例：Node.js 專案

1.  安裝依賴 (通常在 `package.json` 中定義):
    ```bash
    npm install
    ```
2.  運行主程式:
    ```bash
    node index.js # 假設主程式為 index.js
    ```

## 4. 使用 Docker 啟動 (如果適用)

如果 Gemini 提供了 Docker 映像檔，您可以使用 Docker 容器來啟動它。

1.  拉取 Docker 映像檔:
    ```bash
    docker pull your-gemini-image:latest
    ```
2.  運行 Docker 容器:
    ```bash
    docker run -p 8080:8080 your-gemini-image:latest # 假設應用程式在 8080 埠
    ```

## 5. 其他啟動方式

*   **系統服務:** 如果 Gemini 被設定為系統服務 (例如 `systemd` 服務)，您可以使用以下命令啟動:
    ```bash
    sudo systemctl start gemini
    ```
*   **Web 伺服器:** 如果是 Web 應用程式，可能需要透過特定的 Web 伺服器 (如 Nginx, Apache) 或應用程式伺服器 (如 Gunicorn, PM2) 來啟動。

請根據您的具體情況選擇最合適的啟動方法。如果遇到問題，請查閱 Gemini 的官方文件或尋求協助。
