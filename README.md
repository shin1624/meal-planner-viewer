# meal-planner-viewer

吉川家の週次夕飯献立 (3日分) を表示する公開 viewer。

- 本体（生成ロジック・機密同居）は private monorepo `life-repo` の `projects/meal-planner/`。
- この repo は **生成された静的 HTML (`index.html`) だけ** を受け取り GitHub Pages で配信する。
- 週次バッチ (火曜朝) が `meal_planner.web.render` で HTML を生成 → この repo に push → Pages 反映。

機密分離のため life-repo 本体を Pages 化せず、配信物だけをここに切り出している (PER-139)。
