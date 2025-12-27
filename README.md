# Browser Clock Collection

ブラウザで動く時計（アナログ／フリップ）を集めた小さなコレクションです。見た目と動きにこだわったシンプルな作例をまとめています。
`src` が開発・ローカル確認用、`docs` が GitHub Pages 用の公開領域です。
プロジェクトの場所: https://github.com/igapyon/browser-clock-collection

## フォルダ構成
- `src/` 開発・ローカル用
- `docs/` GitHub Pages 公開用（`src` をコピー）
- `assets/preview/` 画像などの補助素材

## 収録時計
- アナログ時計: クラシックな文字盤と3針の基本形 `src/parts/clock-analog-parts-main.html`
- フリップデジタル時計: HH:MM:SS をフリップで切り替え `src/clock-digital-flip-main.html`
- フリップ日付: 年・月・日・曜日を大きく表示 `src/parts/clock-analog-parts-flip-date.html`
- アナログ＋フリップ日付: アナログにミニ日付を合成。時計の余白に年月日が出るのが魅力で、長針と短針の外角に配置する発想はデジタルならでは `src/clock-analog-svg.html`

## 仕様メモ
各時計の仕様説明は `docs/` 配下の Markdown を参照してください。
プレビュー画像は `assets/preview/` にあります。
このプロジェクトでは svg.js（MIT License）を利用しています。

## ローカルで開く
`src/` 以下の HTML をブラウザで直接開けば動作します。
