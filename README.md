# Browser Clock Collection

ブラウザで動く時計（アナログ／フリップ）の作例集です。見た目の良さと動きの軽快さにこだわり、シンプルな構成で作り込んでいます。
現在の作業の核は `src/clock-analog-svg.html` です。長針・短針・秒針の更新に絞り、日付やレイアウトは変化時のみ再計算することで、CPU負荷を最小限に抑える設計にしています。
プロジェクトはGitHub上で作業しています: https://github.com/igapyon/browser-clock-collection

## 収録時計
- アナログ＋フリップ日付: アナログにミニ日付を合成。時計の余白に年月日が出るのが魅力で、長針と短針の外角に配置する発想はデジタルならでは `src/clock-analog-svg.html` (いちおし)
- アナログ時計: クラシックな文字盤と3針の基本形 `src/parts/clock-analog-parts-main.html`
- フリップデジタル時計: HH:MM:SS をフリップで切り替え `src/clock-digital-flip-main.html`
- フリップ日付: 年・月・日・曜日を大きく表示 `src/parts/clock-analog-parts-flip-date.html`
- アナログ＋フリップ日付（物理）: 秒針のみ物理挙動を試すバリエーション `src/clock-analog-matter-phys.html`

## フォルダ構成
- `src/` ソースコードであり実行形式 (HTML)
- `docs/` 各時計の説明
- `assets/preview/` 画像などの補助素材

## 仕様メモ
各時計の仕様説明は `docs/` 配下の Markdown を参照してください。設計意図や調整ポイントをまとめています。
プレビュー画像は `assets/preview/` にあります。見た目の比較に使ってください。
このプロジェクトでは svg.js（MIT License）、Matter.js（MIT License）、Phaser 3（MIT License）を利用しています。

## ローカルで開く
`src/` 以下の HTML をブラウザで直接開けば動作します。ビルドは不要です。
