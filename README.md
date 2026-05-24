# 谁是理财王

朋友理财挑战赛静态排行榜。

## 文件说明

- `index.html`：排行榜网页，适合直接部署到 GitHub Pages。
- `app-data.js`：网页读取的比赛数据。
- `第一届谁是理财王_参赛选手填报模板.xlsx`：参赛者自填模板。
- `scripts/import_excel.py`：把 Excel 填报表转换成 `app-data.js`。

## 更新排行榜

参赛者填完 Excel 后，在项目目录运行：

```bash
python3 scripts/import_excel.py "第一届谁是理财王_参赛选手填报模板.xlsx" -o app-data.js
```

然后提交并推送到 GitHub，GitHub Pages 会展示更新后的排行榜。

## GitHub Pages

把本仓库推到 GitHub 后，在仓库设置中开启 Pages：

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/root`

开启后，别人打开 GitHub Pages 地址就能看到排行榜。
