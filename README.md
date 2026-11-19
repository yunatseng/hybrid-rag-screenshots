# 實際專案截圖

可直接部署到 GitHub Pages 的靜態網頁，包含兩張原始圖片。

## 本機預覽

直接用瀏覽器打開 `index.html` 即可。所有圖片均使用相對路徑，無須安裝套件或執行建置。

## 方法一：透過 GitHub 網頁上傳

1. 登入 GitHub，點選右上角「+」→「New repository」。
2. Repository name 填入 `hybrid-rag-screenshots`，選擇 **Public**，按「Create repository」。
3. 在新儲存庫首頁點選「uploading an existing file」（若已經有檔案，選「Add file」→「Upload files」）。
4. 將 `index.html`、`Hybrid_RAG_1.png`、`Hybrid_RAG_2.png` 三個檔案一起上傳，再按「Commit changes」。檔案必須直接位於儲存庫根目錄，不要只上傳 ZIP，也不要外包一層資料夾。
5. 開啟儲存庫的「Settings」→ 左側「Pages」。
6. 「Build and deployment」的「Source」選 **Deploy from a branch**。
7. 「Branch」選 **main**，資料夾選 **/(root)**，按「Save」。如果你的預設分支名稱不同，選擇剛剛上傳檔案所在的分支。
8. 等待部署完成。Pages 頁面會顯示正式網址；也可以到「Actions」確認「pages build and deployment」已成功。

網址格式：

```text
https://你的GitHub帳號.github.io/hybrid-rag-screenshots/
```

這會公開網頁原始碼及這兩張圖片，訪客不需登入 GitHub。

## 方法二：透過 Git 指令上傳

先在 GitHub 建立名為 `hybrid-rag-screenshots` 的空白 Public 儲存庫，建立時不要加入 README、.gitignore 或 License。接著在終端機進入解壓縮後的資料夾，再執行：

```sh
git init -b main
git add index.html Hybrid_RAG_1.png Hybrid_RAG_2.png README.md
git commit -m "Add project screenshots page"
git remote add origin https://github.com/YOUR_USERNAME/hybrid-rag-screenshots.git
git push -u origin main
```

將 `YOUR_USERNAME` 換成你的 GitHub 帳號。GitHub 若要求驗證，請使用你原本設定的 Git 憑證方式；HTTPS 推送不支援 GitHub 帳號密碼。

推送後仍須完成方法一的第 5–8 步，才能啟用 GitHub Pages。

## 更新內容

修改 `index.html` 可調整文字、版面或圖片名稱。日後更新同一分支的檔案後，GitHub Pages 會重新部署。

官方文件：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
