# Analog Clock + Date (Matter.js)

## 概要
SVGベースのアナログ時計に Matter.js を組み合わせた試作です。針のみ物理ボディ化しています。

## 表示内容
- アナログ時計（時針／分針／秒針）
- ミニ日付（YYYY / MM / DD / 曜日）

## 振る舞い
- 1秒ごとに更新
- 秒の境界に合わせて更新
- 針は Matter.js のボディとして扱う

## 動作環境
- モダンブラウザ（Chrome / Edge / Safari / Firefox）
- 外部ライブラリ: SVG.js / Matter.js（CDN）

## 使い方
- `src/clock-analog-matter.html` を直接ブラウザで開く

## 変更の目安
- 針の揺れ: ボディの `frictionAir` や角速度設定を調整
- 物理挙動: トルクや制約の追加
