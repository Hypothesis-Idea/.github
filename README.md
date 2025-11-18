# HypoIdea — 網站介紹與 GitHub Pages

這個 repository 用來在 GitHub 上提供一個簡短的介紹頁面，並將訪客導向主站 https://www.hypoidea.com。

主要內容：
- `index.html`：一個簡單的靜態頁面，會自動導向到主站，同時保留可閱讀的簡介。
- `CNAME`：設定 GitHub Pages 的自訂網域（預設為 `www.hypoidea.com`，若需改為 apex domain 請告知）。
- `.github/workflows/pages.yml`：GitHub Actions workflow，用來自動部署到 GitHub Pages（當 `main` branch 有 push 時）。
- `LICENSE`：採用 MIT 授權（範例）。

簡單合約（Contract）
- 輸入：將此 repo push 到 GitHub 的 `main` branch；如需使用自訂網域，請在 DNS 管理員新增 CNAME 至 GitHub Pages 指示的值。
- 輸出：GitHub Pages 會在部署後提供一個靜態首頁，並自動導向至 https://www.hypoidea.com。

注意事項與假設
- 我假設您要使用 `www.hypoidea.com` 作為自訂網域（因為您提供的網址是 https://www.hypoidea.com）。若要改為 `hypoidea.com`（apex），請告知；apex 可能需要 ALIAS/ANAME 或使用 A records。
- 若您想把內容直接放主站（非導向），可以把 `index.html` 修改為完整介紹內容。

如何上線（簡要）
1. 把本 repo push 到 GitHub（例如 `git push origin main`）。
2. 在 repository 的 Settings → Pages 中，確認 Pages 的來源是 `main` branch / root（或啟用 GitHub Actions 部署）。
3. 在 DNS 管理員中，為 `www.hypoidea.com` 新增一個 CNAME 指向 `YOUR-GITHUB-USERNAME.github.io` 或遵照 GitHub 提供的 Pages 指示（若是組織或自動化，請參考 GitHub Pages文件）。

如果您要我替您把檔案推到遠端 GitHub（建立 repo/commit/push），請提供授權方式或告訴我您願意我產生可上傳的檔案壓縮包。若您要直接自動化部署（例如透過 Personal Access Token），我也可以協助建立 workflow 或協助設定。 

---
若需更完整的介紹頁（多頁面、樣式或翻譯），我可以繼續擴充並加入簡單的 CSS 與範例內容。

作者：自動化建置器
