# 2027統一地方選 対象議会の「議会での行動」データ調査（2026-11-21）

目的：統一地方選ページで、現職候補の議会での行動（増税議案への賛否、一般質問など）を載せられるか確認する。
調べ方：各議会の公式サイトをWeb検索で確認。○＝確認済み、△＝一部・形式未確認、×＝見つからない、？＝未確認。

| 選挙 | 議員別の賛否 | 会議録のWeb公開 | ほかの資料 |
|---|---|---|---|
| 高知県議会（4/11） | ○ 定例会ごとの議決結果一覧PDF（R8.2・R8.6まで掲載） | ○ 会議録検索（本会議・委員会） | 会派別議員名簿 |
| 高知市議会 | × 議員別の一覧なし。議案審議結果は可否のみ。会派の態度は議会だよりの討論から | ○ 会議録検索システム（本会議H6.12〜R8.6、委員会H19.4〜） | ○ 本会議の中継・録画（約1年、質問議員名・語句で検索可） |
| 宿毛市議会 | △ 会議録PDFの目次に議案ごとの議員名と賛否の記載例あり（R7第1回） | ○ 会議録PDF | 議会だより |
| 奈半利町議会 | × | × 議会事務局で閲覧のみ（閲覧申請書あり） | 議会だよりは「広報なはり」内 |
| 田野町議会 | ？ | × 見つからず | 議会だより（207号まで）、会期予定表、一般質問の記録 |
| 安田町議会 | ？ | × 見つからず | 議会だより（186号まで、PDF） |
| 北川村議会 | ？ | △ 定例会ごとの会期日程・審議結果ページのみ | 議会だよりは見つからず |
| 大川村議会 | × | × | 議会ページに会議録・議会だよりなし |
| 土佐町議会 | ？ | ？ 見つからず | 議会の概要ページのみ |
| 梼原町議会 | ？ | △ 年度ごとの「定例会議事録」ページあり（町議会のものか要確認） | 町議会だより |
| 三原村議会 | △ 広報みはらに「議案の賛否一覧」掲載（議員別か要確認） | × | 議会だより |
| 黒潮町議会 | △ 議会だよりに議案と採決結果の一覧（議員別か要確認） | ○ 会議録PDF（2018年12月〜） | 議会だより（PDF） |

首長選（東洋町長・北川村長・土佐町長）は、首長が提出した議案（予算・税条例・使用料改定）を各議会の審議結果から拾う。

## 設計への含意
- 議員別の賛否を公式資料で載せられるのは、確実なのは県議会、ほぼ確実なのは宿毛市。三原村・黒潮町は資料の形式を確認する。
- 高知市議会は起立採決が多く、会議録にも議員名が残らない可能性が高い。会派の討論と一般質問を中心にする。
- 小さな町村は会議録がWebにないため、一般質問のテーマ（議会だより）が主な材料。賛否まで載せるには議会事務局での閲覧や情報公開請求が要る。

## 出典
- 高知県議会「議員別賛否の状況」 https://gikai.pref.kochi.lg.jp/activity/decision.html
- 高知市議会 会議録検索システム https://www.city.kochi.kochi.jp/soshiki/97/kaigirokukenn.html ／ 議会中継 https://www.city.kochi.kochi.jp/soshiki/97/rokugatyukei.html
- 宿毛市議会 https://www.city.sukumo.kochi.jp/01/04/02/
- 奈半利町 議会情報 https://www.town.nahari.kochi.jp/life/dtl.php?hdnKey=1110
- 田野町議会 https://www.tanocho.jp/gikai/
- 安田町議会 https://www.town.yasuda.kochi.jp/gikai/
- 北川村 議会事務局 https://www.kitagawamura.jp/life/list.php?hdnSKBN=C&hdnZoku=1005
- 大川村 村議会 https://www.vill.okawa.kochi.jp/life/dtl.php?hdnKey=1186
- 土佐町 議会の概要 https://www.town.tosa.kochi.jp/life/detail.php?hdnKey=116
- 梼原町議会 https://www.town.yusuhara.lg.jp/gikai/
- 三原村議会 https://www.vill.mihara.kochi.jp/gikai/ ／ 広報みはら2025年6月号 https://www.kochi-ebooks.jp/bookinfo/koho-mihara-202506/
- 黒潮町 議会だより https://www.town.kuroshio.lg.jp/pb/cont/310 ／ 会議録 https://www.town.kuroshio.lg.jp/pb/cont/machi-gikai-giji
