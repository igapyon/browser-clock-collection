# Analog Clock + Date (Matter.js Physics)

## 概要
Matter.js を使った秒針の物理挙動を試すアナログ時計です。秒針のみ物理ボディで駆動します。

## 表示内容
- アナログ時計（時針／分針／秒針）
- ミニ日付（YYYY / MM / DD / 曜日）
- AM / PM 表示

## 振る舞い
- 秒針のみ物理演算で揺れを表現
- 秒の境界で角度更新
- 日付は日付変更時のみ更新

## 動作環境
- モダンブラウザ（Chrome / Edge / Safari / Firefox）
- 外部ライブラリ: SVG.js / Matter.js（CDN）

## 使い方
- `src/clock-analog-matter-phys.html` を直接ブラウザで開く

## 変更の目安
- 秒針の揺れ: `secSpring` のパラメータ調整
- デバッグ表示: `debug.showSecTrace` の切り替え
