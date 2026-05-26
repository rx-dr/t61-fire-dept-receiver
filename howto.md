---
layout: page
title: 聴き方
---

誰にでもできる簡単な聴き方を説明します。SDR に慣れている方は、自分なりにアレンジしてみてください。

## 必要なもの

- RTL-SDR Blog V3 ドングル [Amazon](https://www.amazon.co.jp/RTL-SDR-Blog-RTL2832U-%E3%82%BD%E3%83%95%E3%83%88%E3%82%A6%E3%82%A7%E3%82%A2%E5%AE%9A%E7%BE%A9%E3%83%A9%E3%82%B8%E3%82%AA-%E3%83%B3%E3%82%B0%E3%83%AB%E3%81%AE%E3%81%BF/dp/B0BMKZCKTF)/[AliExpress](https://www.aliexpress.com/item/32939551915.html)
- 260 MHz 帯が受信可能なアンテナ
- [SDR#](https://airspy.com/download/)
- [SDR# 用 ARIB STD-T61 FDMA デコーダプラグイン](https://unset-histfile.booth.pm/items/8345951)
- [消防救急デジタル無線受信アプリ]({{site.baseurl}}assets/files/t61-fire-dept-receiver-1.0.4.zip)

## ソフトウェアのセットアップ

1. 「RTL-SDR Blog V3 ドングル」に「260 MHz 帯が受信可能なアンテナ」を接続
2. 「RTL-SDR Blog V3 ドングル」を PC に接続
3. [「SDR#」をダウンロード](https://airspy.com/download/)して適当な場所に ZIP ファイルを展開
4. [「SDR# 用 ARIB STD-T61 FDMA デコーダプラグイン」をダウンロード](https://unset-histfile.booth.pm/items/8345951)して適当な場所に ZIP ファイルを展開
5. [「消防救急デジタル無線受信アプリ」をダウンロード]({{site.baseurl}}assets/files/t61-fire-dept-receiver-1.0.4.zip)して適当な場所に ZIP ファイルを展開
6. 展開した「SDR#」の「install-rtlsdr.bat」を実行
7. 展開した「SDR#」の「zadig.exe」を使用して「RTL-SDR Blog V3 ドングル」のドライバを「WinUSB」ドライバに置き換える
8. 展開した「SDR#」の「Plugins」フォルダと、展開した「SDR# 用 ARIB STD-T61 FDMA デコーダプラグイン」の「Plugins」フォルダを統合
9. 展開した「SDR#」の「SDRSharp.dotnet9.exe」を実行して「SDR#」を起動
10. 「SDR#」の画面最左上のハンバーガーメニューを開く
11. 「Plugins」を選択し「ARIB STD-T61 FDMA Decoder (SDR# 用 ARIB STD-T61 FDMA デコーダプラグイン)」を有効化
12. 「ARIB STD-T61 FDMA Decoder」のライセンスキーを入力しアクティベート
13. 「SDR#」を再起動
14. 「ARIB STD-T61 FDMA Decoder」の「デコーダを有効化」にチェック
15. 「ポート」が「1234」になっていることを確認
16. 「ARIB STD-T61 FDMA Decoder」の「JSONL TCP」にチェック
17. 「消防救急デジタル無線受信アプリ」の「t61-fire-dept-receiver.exe」を実行して「消防救急デジタル無線受信アプリ」を起動
18. 「ホスト」が「127.0.0.1」、「ポート」が「1234」になっていることを確認
19. 「接続」ボタンを確認
20. 「SDR#」の受信周波数を聴きたい周波数に設定 (受信モードは影響しない)

## 周波数一覧

- 274.30625 MHz 都道府県・主運用波1 (青森県・栃木県・静岡県・京都府・広島県・佐賀県)
- 274.38125 MHz 都道府県・主運用波2 (宮城県・千葉県・長野県・大阪府・愛媛県・長崎県・沖縄県)
- 274.45625 MHz 都道府県・主運用波3 (山形県・埼玉県・愛知県・兵庫県・山口県・鹿児島県)
- 274.60625 MHz 都道府県・主運用波4 (北海道・福島県・東京都・岐阜県・和歌山県・鳥取県・福岡県)
- 274.68125 MHz 都道府県・主運用波5 (秋田県・茨城県・山梨県・富山県・滋賀県・徳島県・大分県)
- 274.75625 MHz 都道府県・主運用波6 (新潟県・神奈川県・福井県・奈良県・島根県・香川県・宮崎県)
- 274.83125 MHz 都道府県・主運用波7 (岩手県・群馬県・石川県・三重県・岡山県・高知県・熊本県)
- 274.90625 MHz 全都道府県・統制波1
- 274.23125 MHz 全都道府県・統制波2
- 274.53125 MHz 全都道府県・統制波3
- 274.95000 MHz 受令波1
- 274.96875 MHz 受令波2
- 274.98750 MHz 受令波3

出典: [消防・救急無線のデジタル考 \| 無線脳の視点](https://ameblo.jp/jg7ubp/entry-12942717822.html)
