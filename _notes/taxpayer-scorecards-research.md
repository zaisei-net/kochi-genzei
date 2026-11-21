# 納税者団体の議員評価・誓約の研究（2026-11-21）

統一地方選ページの「候補者誓約」と「議員評価」の設計のため、米国の先行例と日本の対応例を調べた。

## 1. ATR（Americans for Tax Reform）Taxpayer Protection Pledge
- 候補者・現職が「増税に反対し、反対票を投じる」と書面で約束する誓約。連邦版と州版で文言が別。
- 誓約は ATR ではなく選挙区の有権者に対する約束という位置づけ。署名した職にある間は有効。
- ATR は違反を監視し、議案が誓約違反に当たるかを議員に指摘する（ロビー活動に使う）。全50州の納税者団体と組んで署名を集める。
- 署名者は州議員から知事・連邦議員まで約1,400人（ATRの説明）。批判：解釈が広くなりうる。

## 2. NTU（National Taxpayers Union）Rates Congress
- 税・歳出・主要な規制の採決を「選り好みせず全部」対象にする。
- 各採決に財政への影響の大きさで重み（1〜100、平均的な採決は10前後）をつける。
- 点数＝納税者側（歳出減・減税・規制減）の票の重み合計 ÷ その議員が投票した採決の重み合計。
- 欠席・棄権は計算から除く。投票した重みが全体の50%以下の議員は採点しない。
- A＝90%以上で「Taxpayers' Friend Award」。満点の議員はこれまでいない。

## 3. Club for Growth Foundation Scorecard
- 減税・規制緩和など成長政策の目標リストに照らし、重要な採決だけを選ぶ（2024年は856採決から下院14・上院13）。
- 事前に「キーボート（重要採決）」として通告することが多いが、事後に加えることもある。
- 重要度で配点し、0〜100点。年間と通算（lifetime）の点数。90点以上で表彰。欠席が多い年は採点しない。
- 州議会版もある（例：フロリダ州2024年、下院16・上院13採決）。

## 4. 日本：JTR（日本税制改革協議会）納税者保護誓約書
- 「私は、いかなる増税にも反対をします。」と書かれた誓約書に、立会人をつけて署名し、JTR会長と取り交わす。
- 国会議員・地方議員・首長・候補者が対象。署名者を速報ページで公表（2026年も市議の署名あり）。
- ATRの手法を日本に導入したものという説明があるが、JTR公式サイトでの提携の明記は確認できていない（第三者ブログの記述）。
- 高知県内の署名者は今回の検索では見つからなかった。

## 高知への当てはめ
- 県議会の現任期の採決は会派単位で完全にそろい、税・手数料の議案はほぼ全会一致（`data_raw/kengikai/votes_R5-R8.json`）。NTU型（全採決）だと差がほとんど出ず、出る差は会派の差。
- Club for Growth型（重要採決を選び、事前に通告する）が向いている。選挙直前のR9.2定例会（当初予算・税条例）で、事前に「この議案を評価対象にする」と公表できる。
- 歳出を評価に入れるなら、予算の修正案の中身の確認が要る。
- 誓約は、JTRの納税者保護誓約書を使うか、高知減税会独自の誓約にするかを決める。

## 出典
- ATR: https://en.wikipedia.org/wiki/Americans_for_Tax_Reform ／ https://www.legistorm.com/organization/summary/45895/Americans_for_Tax_Reform.html ／ https://ballotpedia.org/Americans_for_Tax_Reform
- NTU: https://www.ntu.org/ratecongress/page/computation ／ https://www.ntu.org/ratecongress
- Club for Growth: https://www.clubforgrowth.org/scorecards/2023-scorecard-methodology-copy/ ／ https://clubforgrowthfoundation.org/wp-content/uploads/2024/11/2024-Florida-Scorecard-FINAL.pdf
- JTR: https://jtr.gr.jp/sign ／ https://jtr.gr.jp/cms/wp-content/uploads/2021/10/HP%E7%94%A8%E7%BD%B2%E5%90%8D%E7%94%A8%E7%B4%99.pdf ／ https://note.com/quirky_wasp5981/n/n3c837d0cadb6
