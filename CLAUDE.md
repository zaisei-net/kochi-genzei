# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## サイト概要

**高知減税会** の GitHub Pages 静的サイト。
- 公開URL: `https://zaisei-net.github.io/kochi-genzei/`
- リポジトリ: `zaisei-net/kochi-genzei`（branch: `main`）
- ビルドツール・パッケージマネージャーなし。純粋なHTMLファイルのみ。

## デプロイ

```bash
git add <files>
git commit -m "メッセージ"
git push origin main
```

push するだけで GitHub Pages が自動デプロイされる。

## ディレクトリ構造

```
/                   トップページ（高知減税会 概要・マニフェスト）
/kami/              香美市 行政ウォッチ（最重点ページ）
/kami/analyze/      香美市 財政分析
/kami/genzei/       香美市 減税計画（香美市の子ページ）
/pref/              高知県庁ウォッチ
/kochi/             高知県34市町村データ一覧
/senkyo/            選挙日程ポータル（JS で動的生成）
/aki/               安芸市 選挙ウォッチ
/geisei/            芸西村 選挙ウォッチ
/ochi/              越知町 選挙ウォッチ
/muroto/            室戸市 選挙ウォッチ
/susaki/            須崎市 選挙ウォッチ
/tosashimizu/       土佐清水市 選挙ウォッチ
/pubcom/            パブリックコメント情報（県内全自治体）
/chinjo/            陳情・請願 ガイド
/jiyuu/             自由民権 歴史ページ
/map/               地図（kochi_muni.geojson 使用）
```

## ページの設計パターン

### すべてのページ共通

- CSS変数でテーマ管理（`:root` → `data-theme="dark"` / `data-theme="light"`）
- ナビゲーションは `<header class="topbar">` 内の `.topbar-nav`
- Google Analytics: `G-F1PBSFFVQ5`
- フォント: `"Hiragino Kaku Gothic ProN","Yu Gothic UI",Meiryo,"BIZ UDGothic",sans-serif`

### 子ページパターン（kami/genzei/ など）

- 親ページへのナビリンクに `class="parent"` を追加して青字・太字表示
- ヒーロー直下にパンくずリスト `.breadcrumb` を置く
  ```html
  <p class="breadcrumb"><a href="/kochi-genzei/">高知減税会</a> › <a href="/kochi-genzei/kami/">香美市</a> › ページ名</p>
  ```

### 市町村選挙ウォッチページ（aki, geisei, ochi, muroto, susaki, tosashimizu）

各ページの構成：
1. 行政評価（`.eval-grid`）— `.good-box` / `.warn-box` / `.alert-box`
2. 指定管理者制度（`.shitei-grid`）
3. 選挙カウントダウン（`new Date('YYYY-MM-DD')`）
4. 要求事項テーブル
5. 高知減税会の基本方針（`.policy-list`）— 先頭に `<strong>全ての増税に反対します。</strong>`

### senkyo/index.html

JavaScript の `PAGES` オブジェクトで市町村ごとのURLとボタンラベルを管理。新しい市町村ページを追加したらここにも追記する。

## 重要な表記ルール

- 「１円の増税にも反対」— **全角数字**（「一円」「1円」は使わない）
- 「全ての増税に反対します。」は各ページで `<strong>` タグで太字化
- 文体: です・ます体で統一

## テキスト一括置換の方法（PowerShell 5.1）

`Set-Content -Encoding UTF8 -NoNewline` はBOMを付けるため使用不可。代わりに：

```powershell
$files = Get-ChildItem -Path . -Filter "*.html" -Recurse
foreach ($f in $files) {
    $content = [System.IO.File]::ReadAllText($f.FullName, [System.Text.Encoding]::UTF8)
    $newContent = $content -replace '旧テキスト', '新テキスト'
    [System.IO.File]::WriteAllText($f.FullName, $newContent, [System.Text.Encoding]::UTF8)
}
```

## パブコメページの更新方針（pubcom/index.html）

- 最終確認日を毎回更新する（`最終確認: YYYY年M月D日`）
- 「パブリックコメント」「意見公募」「意見募集」「住民意見等の募集」すべての用語を対象に調査
- 高知県内で意見公募手続制度を条例制定しているのは**四万十町のみ**（H29総務省調査）。多くの自治体は専用ページを持たない
- 締切3日以内の案件は `.pc-card` に赤ボーダーと「緊急・締切近」バッジを付ける
