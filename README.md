# 断食道場SHOP｜楽天スーパーSALE クーポンカレンダー

楽天スーパーSALE（2026年9月）の断食道場SHOP（優光泉）向け **クーポンまとめ / イベントページ**。
「クーポンが一目でわかること」「楽天スーパーSALEのカレンダー型特設会場であること」を軸に、
カレンダー画像＋日付ストリップ（9日分）＋日付順のクーポン一覧＋日付を大きく見せたクーポンカードで構成。

- 1ファイル完結：`index.html` に CSS・JS をすべて内包（相対パス）
- 中央1カラム `max-width:750px`
- 配色：ピンク＋イエローのイベント配色（全面ベタ塗り・無地）。ピンク `#E64C86` / 深ローズ `#C43A70` / ビビッドイエロー `#FFD400` / 生成り `#FFFBF4` / インク `#2A0E1E`
- フォント：**すべて Zen Kaku Gothic New**（Google Fonts、見出し900／本文700／説明500）。`:root` の `--font-display` / `--font-jp` / `--font-num` すべて同じスタック。MS Pゴシック・LINE Seed JP は廃止（`fonts/` フォルダも削除）
- デザイン：全体センター寄せ／文字の影なし（枠・カードのオフセット影のみ）／極太ピルボタン／**小見出しラベルはフラットなテキスト（傾き・ピル・影なし）**／**大タイトルに「、。」を入れない**／日付を大きく（カレンダー一覧・クーポンカードの日付は Zen 900 の大サイズ）
- 写真：商品カードに大きめの Rakuten サムネイル（`images/items/<code>.jpg`、1:1・太枠）。写真つきクーポンはデスクトップで［写真260px｜内容］の2カラム、スマホは縦積み。小さい文字は全体的に拡大（説明17.5px・バッジ15.5px 目安）
- 表記ルール：楽天SALE規定で "SUPER" 単独の英字は禁止 → ラベルは「RAKUTENスーパーSALE」。英字 "SUPER SALE" を使わないこと

## ページ構成

1. FV（`.fv`）… ラベル／見出し／開催期間（9/4 20:00 → 9/11 1:59）／「福袋・一部クーポンは9/3から」注記
2. カレンダー画像（`.calendar`）… いまは `images/calendar-poster-placeholder.svg`（仮）
3. カレンダー（`.calsec`）… カレンダー画像＋日付ストリップ（`.daycal` 9セル、5/10は黄ハイライト）＋日付大の一覧（`.callist`）。すべて該当クーポンへアンカージャンプ
4. クーポン5つ（`.sec.pink` / `.coupon`）… 日付バッジ＋（商品ものはサムネイル）＋割引の巨大数字＋タイトル＋条件＋ボタン。全要素センター寄せ・文字影なし
5. 通し企画（`.sec.butter`）… 1,000円ポッキリ2品＋ポケット優光泉15包の重ねクーポン（20%→45%→無料）
6. 結び（`.closing`）… ショップ／SALE会場／楽天スーパーSALE会場リンク＋注意書き

## 差し替え・確認が必要な箇所

| 箇所 | いまの状態 | やること |
|---|---|---|
| SALEカレンダー画像 | `images/calendar-poster-placeholder.svg`（仮） | 正式画像を `images/` に置き、`.calendar` の `<img src>` を変更 |
| 開催期間 | FV：`9/4 20:00 → 9/11 01:59`（一般的な日程） | 2026年9月の楽天スーパーSALE公式日程で要確認 |
| 曜日 | 2026年9月：3木・4金・5土・6日・10木・11金 | 変更なければそのまま |

## クーポン・リンク一覧

| セクション | 日付 | 内容 | リンク |
|---|---|---|---|
| サブローの日 限定福袋 | 9/3–9/6 | 数量限定 | `gold/danjiki-dojo/event/201712/20250203.html` |
| 敬老の日ギフト ポイント10倍 | 9/5のみ | 優光泉200ml×4本 | `item.rakuten.co.jp/danjiki-dojo/3004/` |
| 全品15%OFF | 9/3–9/5 | 先着200名 | getkey `NVpKQy1VTEdULU1UTUctSjVYUA--` |
| 全品10%OFF | 9/6–9/11 1:59 | — | getkey `U0NUQS00SVFXLTBRUjItVUtLSA--` |
| くわタブレット 30%OFF | 9/10のみ | 3袋以上購入で | getkey `UzdEUC1LRk9HLU9ZUVgtUkhVQg--` |
| ポケット優光泉6包 1,000円ポッキリ | 通し(9/4 20:00–9/11 1:59) | — | `item.rakuten.co.jp/danjiki-dojo/1000/` |
| 酵素ゼリー ミカン味6包 1,000円ポッキリ | 通し | — | `item.rakuten.co.jp/danjiki-dojo/4001/` |
| ポケット優光泉15包 1箱目 20%OFF | 通し | ゼリー対象外 | getkey `WVE3Sy1JUEcwLUczOFctTEo1Nw--` |
| ポケット優光泉15包 2箱目 45%OFF | 通し | ゼリー対象外 | getkey `NkpVSy1ZRllHLVM2QzItSUVQRw--` |
| ポケット優光泉15包 3箱目 無料 | 通し | ゼリー対象外 | getkey `UFFMVi1PSllNLVNGOE0tVU44UA--` |

## ローカルプレビュー

```
powershell -ExecutionPolicy Bypass -File scripts/serve.ps1
# → http://localhost:8736/
```

## 納品

`index.html` + `images/` + `fonts/` を配置すれば動く。`scripts/` は開発用なので除外可。
