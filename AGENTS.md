# AGENTS.md

このリポジトリは、ブラウザで動く時計（アナログ／フリップ）の作例集です。HTML を直接開いて動作します。

## 目的と方針
- 見た目の良さと軽快な動作を重視する
- 不要な再描画を避け、更新は秒境界に合わせる
- 静的要素は初期描画とリサイズ時のみ再描画する
- 日付などの情報は変化時のみ更新する

## 中心ファイル
- 主要な作業対象: `src/clock-analog-svg.html`
  - 長針・短針・秒針のみ毎秒更新
  - 日付やレイアウトは変化時のみ再計算

## 収録時計（代表）
- アナログ＋ミニフリップ日付: `src/clock-analog-svg.html`
- アナログ時計: `src/parts/clock-analog-parts-main.html`
- フリップデジタル時計: `src/clock-digital-flip-main.html`
- フリップ日付: `src/parts/clock-analog-parts-flip-date.html`
- 物理挙動（Matter.js）: `src/clock-analog-matter-phys.html`
- Phaser 3 版: `src/clock-analog-phaser3.html`

## 実行方法
- `src/` 以下の HTML をブラウザで直接開く（ビルド不要）

## 外部ライブラリ
- SVG.js / Matter.js / Phaser 3（いずれも CDN 利用）

## 仕様参照
- 各時計の詳細は `docs/` 配下の Markdown を参照
- プレビュー画像は `assets/preview/`

## 変更の目安（共通）
- サイズ調整: `#mount` のサイズや幅
- 配色調整: テーマ色の変更
- 日付の配置・サイズ: 位置やスケール調整
- 物理挙動: Matter.js のパラメータ調整
