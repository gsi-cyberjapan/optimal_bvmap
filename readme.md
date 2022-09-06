# 最適化ベクトルタイル試験公開

## 公開の位置づけ
- 「最適化ベクトルタイル」は、これまで地理院地図Vector（仮）において試験提供してきた地理院ベクトルタイルの課題を踏まえて、設計改良を施したものです。本試験公開は、ベクトルタイルの提供に必要な技術的・施策的課題を国土地理院が把握するとともに、外部からの技術的な提案を受け取り、外部との技術的な議論を通じてベクトルタイルの適切な提供方法を研究開発することを目的とするものです。
- 公開期間は、2022年9月6日から公開終了までとなります。
- 最適化ベクトルタイルは、[国土地理院コンテンツ利用規約](https://www.gsi.go.jp/kikakuchousei/kikakuchousei40182.html)に従って利用できます。データを利用する際は、「国土地理院最適化ベクトルタイル」などと、出典の明示を行ってください。
- 最適化ベクトルタイルは基本測量成果と位置付けているものではありませんが、基本測量成果としての提供を検討するにあたって、試験的に公開を行うものです。
- 最適化ベクトルタイルの利用により生じた損失及び損害等について、国土地理院はいかなる責任も負わないものとします。

## デモサイト
https://gsi-cyberjapan.github.io/optimal_bvmap/

## ベクトルタイルの仕様
本ベクトルタイルは、[地理院タイル（ラスタ）](https://maps.gsi.go.jp/development/siyou.html)と同じ方式で配信します。
`https://cyberjapandata.gsi.go.jp/xyz/{t}/{z}/{x}/{y}.{ext}`

* 本ベクトルタイルは、タイルに分割した[Vector tile specification](https://github.com/mapbox/vector-tile-spec)形式のファイル群。
* 拡張子は「pbf」。

### ズームレベルについて
本ベクトルタイルにおけるズームレベル（{z}）は、現在「地理院地図」で提供している地理院タイル（ラスタ）（ https://maps.gsi.go.jp/development/ichiran.html ）のズームレベルと同一ではありません。
画面上で同じ大きさで表示される際のズームレベルは、ベクトルタイルにおける数値が、地理院タイル（ラスタ）のズームレベルと比べて1小さい数値となります。そのため、ベクトルタイルにおけるズームレベル11のデータは、ズームレベルが12の地理院タイル（ラスタ）と同じデータを用いて作成しています。
また、ベクトルタイルにおいて画面に表示されるタイルの大きさは、地理院タイル（ラスタ）でズームレベルが1大きい（大きさが小さい）タイルの4枚分に相当します。

<table>
	<tr><th colspan="2">対応するズームレベルの範囲</th></tr>
	<tr><th>最適化ベクトルタイル</th><th>地理院タイル（ラスタ）</th></tr>
	<tr><td>4～7</td><td>5～8</td></tr>
	<tr><td>8～10</td><td>9～11</td></tr>
	<tr><td>11～13</td><td>12～14</td></tr>
	<tr><td>14～16</td><td>15～17</td></tr>
	<tr><td>17</td><td>18</td></tr>
</table>

## タイル一覧
検証中のデータであるため、URL やデータ構成、データの内容（属性の有無や名称等）が変わる可能性があります。

<table>
	<tr><th>URL</th><td>https://cyberjapandata.gsi.go.jp/xyz/experimental_bvmap-v1/{z}/{x}/{y}.pbf</tr>
	<tr><th class="titletd">データソース</td><td>数値地図（国土基本情報）- 地図情報 等</td></tr>
	<tr><th>ズームレベル</td><td>4～16<br>※ズームレベル17の情報は、ズームレベル16のタイルに含んだうえでオーバーズームして表示</td></tr>
	<tr><th>公開日</td><td>2022年9月6日</td></tr>
	<tr><th>データ更新情報</th><td>2022年7月1日時点<br>※最新の状況が反映されていない場合があります。</td></tr>
</table>

### 属性等の仕様詳細
* 地物種別コード一覧

	[PDF版](https://maps.gsi.go.jp/help/pdf/vector/optbv_featurecodes.pdf)　[Excel版](https://maps.gsi.go.jp/help/pdf/vector/optbv_featurecodes.xlsx)
  
* データ項目一覧

	[PDF版](https://maps.gsi.go.jp/help/pdf/vector/optbv_dataspec.pdf)　[Excel版](https://maps.gsi.go.jp/help/pdf/vector/optbv_dataspec.xlsx)

* 地物等の属性一覧

  [PDF版](https://maps.gsi.go.jp/help/pdf/vector/optbv_attribute.pdf)　[Word版](https://maps.gsi.go.jp/help/pdf/vector/optbv_attribute.docx)

##問い合わせ先
- gsi-inad-9@gxb.mlit.go.jp

## 履歴
- 2022-09-06 公開。
