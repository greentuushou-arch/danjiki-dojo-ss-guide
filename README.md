# 断食道場SHOP｜楽天スーパーSALE クーポンカレンダー

楽天スーパーSALE（2026年9月）の断食道場SHOP（優光泉）向け **クーポンまとめ / カレンダー型イベントページ**。
カレンダー画像＋日付ストリップ（9日分）＋日付順のクーポン一覧＋日付を大きく見せたクーポンカードで構成。

- 1ファイル完結：`index.html` に CSS・JS をすべて内包（相対パス）
- 中央1カラム `max-width:750px`
- 公開URL：https://greentuushou-arch.github.io/danjiki-dojo-ss-guide/
- 配色：ピンク＋イエローのイベント配色（全面ベタ塗り・無地）。ピンク `#E64C86` / 深ローズ `#C43A70` / ビビッドイエロー `#FFD400` / 生成り `#FFFBF4` / インク `#2A0E1E`
- フォント：**すべて Zen Kaku Gothic New**（Google Fonts、見出し900／本文700／説明500）。`:root` の `--font-display` / `--font-jp` / `--font-num` すべて同じスタック
- デザイン：全体センター寄せ／文字の影なし（枠・カードのオフセット影のみ）／極太ピルボタン／小見出しラベルはフラットなテキスト（傾き・ピル・影なし）／大タイトルに「、。」を入れない／日付を大きく
- 写真：ユーザー支給のバナー画像は加工なしで掲載（枠・影なし）
- 表記ルール：楽天SALE規定で "SUPER" 単独の英字は禁止 → 「RAKUTENスーパーSALE」「楽天スーパーSALE」と表記

## ページ構成

1. サイトヘッダー（`.topbar`）… 「断食道場SHOP ↗」→ 店舗トップ（rakuten.co.jp/danjiki-dojo/）
2. FV（`.fv`）… `images/fv-banner.jpg` 全画像（日付・キャッチを焼き込み済）
3. あいさつ（`.greet`）… クリーム地。ショップからのあいさつ文
4. カレンダー（`.calsec`）… `images/sale-calendar.jpg` ＋日付ストリップ（`.daycal` 9セル、5/10は黄ハイライト）＋日付大の一覧（`.callist`）。すべて該当クーポンへアンカージャンプ
5. イベント（`.sec.pink` / `.coupon`）… 福袋・15%OFF・敬老の日ポイント10倍・10%OFF（通し）・くわタブレット30%OFF
6. 通し企画（`.sec.butter`）… 1,000円ポッキリ2品＋ポケット優光泉15包の重ねクーポン（20%→45%→無料）
7. ラインナップ（`.sec.cream` / `.lineup`）… SALE対象商品バナー13点。各画像は楽天の商品ページへリンク
8. 結び（`.closing`）… ショップトップリンク＋注意書き

## 日付ストリップ（`.daycal`）のジャンプ先

| 日付 | ジャンプ先カード |
|---|---|
| 9/3木 | `#c-off15`（全品15%OFF・先着200名） |
| 9/4金 | `#c-off10`（全品10%OFF・通し） |
| 9/5土 | `#c-keirou`（敬老の日ギフト ポイント10倍） |
| 9/6日〜9/9水 | `#c-off10` |
| 9/10木 | `#c-kuwa`（くわタブレット 3袋以上で30%OFF） |
| 9/11金 | `#c-off10` |

## クーポン・リンク一覧

| セクション | 日付 | 内容 | リンク |
|---|---|---|---|
| サブローの日 限定福袋 | 9/3–9/6 | 数量限定 | `gold/danjiki-dojo/event/201712/20250203.html` |
| 全品15%OFF | 9/3–9/5 | 先着200名 | getkey `NVpKQy1VTEdULU1UTUctSjVYUA--` |
| 敬老の日ギフト ポイント10倍 | 9/5のみ | 優光泉200ml×4本 | `item.rakuten.co.jp/danjiki-dojo/3004/` |
| 全品10%OFF | 通し（9/4 20:00–9/11 1:59） | 先着15%OFFのフォロー枠 | getkey `U0NUQS00SVFXLTBRUjItVUtLSA--`・バナー `images/coupon10off.png` |
| くわタブレット 30%OFF | 9/10のみ | 3袋以上購入で | getkey `UzdEUC1LRk9HLU9ZUVgtUkhVQg--` |
| ポケット優光泉6包 1,000円ポッキリ | 通し | — | `item.rakuten.co.jp/danjiki-dojo/1000/` |
| 酵素ゼリー ミカン味6包 1,000円ポッキリ | 通し | — | `item.rakuten.co.jp/danjiki-dojo/4001/` |
| ポケット優光泉15包 1箱目 20%OFF | 通し | ゼリー対象外 | getkey `WVE3Sy1JUEcwLUczOFctTEo1Nw--` |
| ポケット優光泉15包 2箱目 45%OFF | 通し | ゼリー対象外 | getkey `NkpVSy1ZRllHLVM2QzItSUVQRw--` |
| ポケット優光泉15包 3箱目 無料 | 通し | ゼリー対象外 | getkey `UFFMVi1PSllNLVNGOE0tVU44UA--` |

## ラインナップ13点（`images/lineup/NN.jpg` → 商品ページ）

| # | 商品 | リンク |
|---|---|---|
| 01 | ポケット優光泉 ミカン 15包 | `item/danjiki-dojo/7003/` |
| 02 | 優光泉 スタンダード ボトル 600ml | `item/danjiki-dojo/0090/` |
| 03 | 優光泉 ミカン ボトル 600ml | `item/danjiki-dojo/7001/` |
| 04 | 優光泉 濃縮発酵和漢ドリンク 600ml | `item/danjiki-dojo/0037_1/` |
| 05 | バスクレンチーム26 薬用酵素入浴剤 | `item/danjiki-dojo/0040/` |
| 06 | くわタブレット | `item/danjiki-dojo/5557/` |
| 07 | 優光泉 スタンダード・梅 600ml×2本 | `item/danjiki-dojo/0090/` |
| 08 | 優光泉 ミカン 600ml×2本 | `item/danjiki-dojo/7002/` |
| 09 | 優光泉 ザクローズ 600ml×2本 | `item/danjiki-dojo/0064/` |
| 10 | 優光泉 濃縮発酵和漢ドリンク 600ml×2本 | `item/danjiki-dojo/0037_2/` |
| 11 | ポケット優光泉 16時間ダイエットセット 20ml×15包 | `item/danjiki-dojo/0002/` |
| 12 | ポケット優光泉 ザクローズ 20ml×15包 | `item/danjiki-dojo/0058/` |
| 13 | ポケット優光泉 濃縮発酵和漢ドリンク 20ml×15包 | `item/danjiki-dojo/0046/` |

## 画像

| ファイル | 用途 |
|---|---|
| `images/fv-banner.jpg` | FVヒーロー（1400×1284） |
| `images/sale-calendar.jpg` | SALEカレンダーポスター（1084×1591） |
| `images/coupon10off.png` / `coupon15off.png` | 10%/15%OFFクーポンのバナー |
| `images/items/*.jpg` | クーポンカード内の商品サムネイル |
| `images/lineup/01〜13.jpg` | ラインナップ節のバナー（幅900px） |

## 納品

`index.html` ＋ `images/` を配置すれば動作。開発用の `scripts/` は含まず。
