毛根迷你聖誕雪人 DIY 免費教學網頁｜芬妮手作

2026-11-23 起沿用芬妮 GA4：`snowman_view`、`snowman_click_bNN`、`snowman_seen_bNN`。
34 個按鈕的固定識別、位置及目的地以 `tracking.json` 為準；新增或移動按鈕要同步更新，勿重新編號既有按鈕。

上線前執行 `node --test tests/tracking.test.js`。本機部署 hook 以 `git config core.hooksPath .githooks` 啟用。
QA 用 `?fenny_qa=1&qa_run=<8位以內英數>`，事件進獨立 `snowman_qa_` 前綴，不送正式 page_view。
GA4 即時報表與實際網路收據須在正式網址驗證，單元測試不能取代實機收數。

內部數據表由既有 my-skills `skills/fenny-social-commerce-analytics/snowman_report.py` 唯讀產生 HTML／CSV／JSON。
報表標示日期、來源、訪客數、各按鈕／位置的看見與點擊人數、點擊次數及明確分母的比率。
