# 断食道場SHOP｜スーパーSALEの歩き方

楽天スーパーSALE（2026年9月）向けの「SALEの楽しみ方／歩き方」ページ。
うなぎ屋かわすいの「スーパーSALEの愉しみ方」ページの **“接客するように順番に案内する”構成** を下敷きに、
色・世界観は断食道場SHOP（優光泉）向けに作り直したもの。

- 1ファイル完結：`index.html` に CSS・JS をすべて内包
- 中央1カラム `max-width:750px`、両脇は深緑の余白
- 配色：**イベント仕様のピンク＋イエロー（全面ベタ塗り・無地）**。ピンク `#E64C86`（上品なローズ）/ 深ローズ `#C43A70`（deep・結び背景）/ ビビッドイエロー `#FFD400` / 生成り `#FFFBF4` / インク（赤みの黒）`#2A0E1E`（本文・アウトライン・ハード影）。両脇の余白は淡ピンク `#FFE4EE`、ご案内は淡イエロー `#FFF4C2`
- セクションの地色クラス：`.sec.cream` / `.sec.pink`（ベタピンク＋白文字）/ `.sec.butter`・`.sec.feature`（ベタイエロー）/ `.sec.deep`（深ローズ＋白文字）。すべて単色（斜線・ドット・グラデは無し）
- フォント：見出し・巨大数字＝**Zen Kaku Gothic New（900）**（Google Fonts／`--font-display`）、本文＝MS Pゴシック**太字**（`body{font-weight:700}`）、小さめ数字＝LINE Seed JP。フォント指定を変える場合は `:root` の `--font-display` / `--font-jp` / `--font-num`
- デザイン：極太ピルボタン、太枠＋ベタのオフセット影（`box-shadow:Npx Npx 0`）のステッカー風カード・写真・バッジ、傾いたピル型キッカー、割引率は巨大数字（text-shadow）
- 表記ルール：楽天SALEの規定で "SUPER" 単独の英字表記は禁止。FVラベルは「RAKUTENスーパーSALE」。英字の "SUPER SALE" を使わないこと
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
| 商品写真（全セクション＋LINEUP） | カテゴリーページ `item.rakuten.co.jp/danjiki-dojo/c/0000000194/` の各商品ページ画像を `images/items/<商品コード>.jpg` として取得・同梱。文字入りのバナー画像（店舗の商品画像そのもの） | よりすっきりしたパッケージ写真がある場合は同名で差し替え |
| 各セクションの写真 | 福袋=0086（サブロー＋2本）／前半15%OFF=0090（優光泉600ml 一番人気）／後半10%OFF=0002（ポケット15包）／ポケット優光泉=0046（和漢15包） | 別カットにするなら `<figure class="photo">` の `src` を `images/items/xxxx.jpg` に変更 |
| LINEUP の価格 | 未掲載（SALE価格・通常価格の混同を避けるため各商品ページに委ねる） | 価格を出す場合は要指示（SALE適用後の表記に注意） |
| LINEUP の商品ラインナップ | カテゴリー194の掲載商品を「ボトル／ポケット／断食セット・回復食／その他」の4分類・計21点で掲載。サブローの日 福袋（0085・0086）も同カテゴリー | カテゴリーの商品が入れ替わったら追随 |

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
