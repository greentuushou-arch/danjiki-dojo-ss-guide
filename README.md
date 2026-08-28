# 断食道場SHOP｜スーパーSALEの歩き方

楽天スーパーSALE（2026年9月）向けの「SALEの楽しみ方／歩き方」ページ。
うなぎ屋かわすいの「スーパーSALEの愉しみ方」ページの **“接客するように順番に案内する”構成** を下敷きに、
色・世界観は断食道場SHOP（優光泉）向けに作り直したもの。

- 1ファイル完結：`index.html` に CSS・JS をすべて内包
- 中央1カラム `max-width:750px`、両脇は深緑の余白
- 配色：深い緑 × 生成り × 酵素ドリンクの琥珀色（アクセント）／ 赤は「先着・締切」だけに限定
- フォント：Zen Kaku Gothic New（本文）／ Kaisei Opti（見出し）／ Josefin Sans（数字・欧文）
- スクロールで静かに現れる演出付き。JSが無効／失敗しても内容は必ず表示される作り

## ローカルプレビュー

```
powershell -ExecutionPolicy Bypass -File scripts/serve.ps1
# → http://localhost:8736/
```

## 差し替え・確認が必要な箇所

| 箇所 | いまの状態 | やること |
|---|---|---|
| SALEカレンダー画像 | `images/calendar-poster-placeholder.svg`（仮） | 正式画像を `images/` に置き、`index.html` の `<!-- ▼▼ 差し替え -->` の `src` を変更 |
| 開催期間 | FV：`9/4 20:00 → 9/11 01:59`（かわすいの同SALEページから推定） | 2026年9月の楽天スーパーSALE公式日程で要確認 |
| 「9/6以降 10%OFF」の終了 | `9/11 1:59 まで` と記載 | 実際の終了日時を確認（施策指示に明記なし） |
| 商品写真 | 優光泉シリーズの楽天キャビネット画像を `images/` に取得して同梱 | 最新の商品画像に差し替える場合は `images/yukosen-*.jpg` / `pocket-yukosen.jpg` を置換。楽天GOLDへ載せる際は自店キャビネットのURL参照でも可（コメントに元ファイル名を記載） |
| 対象商品リンク | クーポン取得ボタンのみ | 必要なら各セクションに「対象商品を見る」リンクを追加 |

## クーポン（施策指示どおり）

| セクション | 内容 | getkey |
|---|---|---|
| 前半 15%OFF（先着200名） | 9/3–9/5 | `NVpKQy1VTEdULU1UTUctSjVYUA--` |
| 後半 10%OFF | 9/6– | `U0NUQS00SVFXLTBRUjItVUtLSA--` |
| ポケット優光泉15包 1箱目 20%OFF | ゼリー対象外 | `WVE3Sy1JUEcwLUczOFctTEo1Nw--` |
| ポケット優光泉15包 2箱目 45%OFF | ゼリー対象外 | `NkpVSy1ZRllHLVM2QzItSUVQRw--` |
| ポケット優光泉15包 3箱目 無料 | ゼリー対象外 | `UFFMVi1PSllNLVNGOE0tVU44UA--` |

## 納品

`index.html` + `images/` を配置すれば動く（相対パス）。`scripts/` は開発用なので納品物からは除外可。
