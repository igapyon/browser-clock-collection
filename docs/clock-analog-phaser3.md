# Analog Clock + Date (Phaser 3)

## 概要
Phaser 3 で描画するアナログ時計です。SVG版と同じ構成を Canvas/WebGL 上で再現しています。

## 表示内容
- アナログ時計（時針／分針／秒針）
- ミニ日付（YYYY / MM / DD / 曜日）

## 振る舞い
- 1秒ごとに更新
- 秒の境界に合わせて更新
- 日付は日付変更時のみ更新

## 動作環境
- モダンブラウザ（Chrome / Edge / Safari / Firefox）
- 外部ライブラリ: Phaser 3（CDN）

## 使い方
- `src/clock-analog-phaser3.html` を直接ブラウザで開く

## 変更の目安
- サイズ: ページ内の `#mount` のサイズ調整
- 表示のシャープさ: `resolution` や文字スナップの調整
