# 断食道場SHOP｜スーパーSALEの歩き方

楽天スーパーSALE（2026年9月）向けの「SALEの楽しみ方／歩き方」ページ。
うなぎ屋かわすいの「スーパーSALEの愉しみ方」ページの **“接客するように順番に案内する”構成** を下敷きに、
色・世界観は断食道場SHOP（優光泉）向けに作り直したもの。

- 1ファイル完結：`index.html` に CSS・JS をすべて内包
- 中央1カラム `max-width:750px`、両脇は深緑の余白
- 配色：深い緑 × 生成り × 酵素ドリンクの琥珀色（アクセント）／ 赤は「先着・締切」だけに限定／ ページ両脇の余白は薄いグリーン（`--gutter`）
- フォント：`:root` の `--font-jp` / `--font-accent` / `--font-num` の3変数で一括管理
  - 本文・見出し（タイトル含む）＝ **MS Pゴシック**（`--font-jp` / `--font-accent`）。MS Pゴシックは Windows 専用のローカルフォントなので、スマホ（iOS/Android）など無い端末では Hiragino/Noto などのゴシック体にフォールバックします
  - 数字・欧文ラベル＝ **LINE Seed JP**（`--font-num`）。`fonts/line-seed-jp-num-{Rg,Bd}.woff2` に Latin・数字・記号だけをサブセットして同梱（各約15KB、OFL）。曜日などの日本語は自動で MS Pゴシックに落ちます
- 本文・キャプション類は大きめに設定（本文17.5px、キャプション15.5px 目安）
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
| 商品写真（各セクション） | 優光泉シリーズの楽天キャビネット画像を `images/` に取得して同梱 | 差し替える場合は `images/yukosen-*.jpg` / `pocket-yukosen.jpg` を置換。楽天GOLDへ載せる際は自店キャビネットのURL参照でも可（コメントに元ファイル名を記載） |
| LINEUP セクションの商品画像 | SALE会場ページの各商品ページ（og:image）を `images/items/<商品コード>.jpg` として取得・同梱。文字入りのバナー画像 | よりすっきりしたパッケージ写真がある場合は同名で差し替え |
| LINEUP の価格 | 未掲載（SALE価格・通常価格の混同を避けるため各商品ページに委ねる） | 価格を出す場合は要指示（SALE適用後の表記に注意） |
| LINEUP の商品ラインナップ | SALE会場ページ（20260904_sale15off.html）の掲載商品15点をボトル／スティック／その他に分類 | 会場ページの商品が入れ替わったら追随 |

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
