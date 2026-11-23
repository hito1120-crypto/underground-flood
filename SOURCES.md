# 取得データと出典(首都圏外郭放水路版・2026-11-23 新規確認)

## 参照資料
- [P1] 首都圏外郭放水路(パンフレット 2026.3) / 国土交通省関東地方整備局 江戸川河川事務所 / p1(龍Q館案内) p2(全体図・メカニズム) p3(浸水の歴史) p4(治水効果) p5-6(主要施設)
  https://www.ktr.mlit.go.jp/ktr_content/content/000812781.pdf
- [W0] 首都圏外郭放水路とは / 江戸川河川事務所 / 本文
  https://www.ktr.mlit.go.jp/edogawa/edogawa00402.html
- [W1] 立坑 / 江戸川河川事務所 / 本文
  https://www.ktr.mlit.go.jp/edogawa/edogawa00404.html
- [W2] トンネル / 江戸川河川事務所 / 本文
  https://www.ktr.mlit.go.jp/edogawa/edogawa00414.html
- [W3] 調圧水槽 / 江戸川河川事務所 / 本文
  https://www.ktr.mlit.go.jp/edogawa/edogawa00611.html
- [W3b] 調圧水槽(繁體字版ミラー) / 江戸川河川事務所 / 本文
  https://www.ktr.mlit.go.jp/edogawa/gaikaku/hant/edogawa_hant00728.html
- [W4] 排水機場 / 江戸川河川事務所 / 本文
  https://www.ktr.mlit.go.jp/edogawa/edogawa00612.html
- [R1] 令和8年6月 台風第6号 出水速報(第1報) / 江戸川河川事務所 / p2,p4,p10,p12(速報値・今後修正の可能性あり)
  https://www.ktr.mlit.go.jp/ktr_content/content/000948728.pdf
- [R2] 令和8年6月 台風第6号 出水概要 / 江戸川河川事務所 / p10,p12,p14-15(速報値)
  https://www.ktr.mlit.go.jp/ktr_content/content/000951225.pdf
- [R3] 首都圏外郭放水路 記者発表資料(令和元年7月30日) / 江戸川河川事務所 / p5(事業経緯)
  https://www.ktr.mlit.go.jp/ktr_content/content/000752585.pdf
- [OSM] OpenStreetMap(立坑・施設の位置) / © OpenStreetMap contributors (ODbL) / -
  https://www.openstreetmap.org/
- [GSI] 国土地理院 淡色地図・住所検索 / 国土地理院 / -
  https://maps.gsi.go.jp/
- [S12] 道路運送車両の保安基準(自動車の大きさ: 高さ3.8m・長さ12m) / 国土交通省 / 第2条
  https://www.mlit.go.jp/jidosha/content/B092.pdf
- [S13] 中規模ビル4階建て事務所の木造化標準モデル(階高3.5〜4.5m程度) / 林野庁 / 標準モデル
  https://www.rinya.maff.go.jp/j/riyou/kidukai/attach/pdf/wckyougikai-86.pdf

## 公式値(動画・3D・詳細パネルで共通。`facility_json_b.py`)
- 調圧水槽: 長さ177m・幅78m・高さ18m・地下約22m、柱59本(1本 奥行き7m×幅2m×高さ18m・約500t・楕円に近い断面) [W3,W3b]
- 立坑5本(全体図p2の各立坑ラベル): 第1 内径31.6m/深さ71m、第2 31.6m/67m、第3 31.6m/71m、第4 25.1m/68m、第5 15m/66m [P1 p2]。掘進深度(諸元表p5)は GL-72.1/71.5/73.7/69.0/74.5m で別指標
- トンネル: 全長約6.3km、内径10.6m(第1〜3)・10.9m(第4)・6.5m(連絡)、国道16号の地下約50m [P1 p5-6, W2]
- ポンプ: 毎秒200m³(4台×50)、排水樋管 延長174.1m・幅5.4×高4.2m(6門) [W4, P1 p2]
- 台風6号(速報値): 流入開始 第2立坑8:28/第3(倉松川)9:50/第5 10:37/第3(中川)13:16、全流入終了6/4 20:35、庄和 4号ポンプのみ 6/3 16:30〜6/4 21:47、洪水調節総量3,286千m³、中川で約12cm低減(外郭+三郷の合算・想定はシミュレーション) [R1,R2]

## 推定・要確認・不採用
- 経路: OSMの第一〜第五立坑ノードを直線で結んだ推定線(長さ約5.8km。公式の線形ではない)。立坑座標もOSM(公式座標ではない)
- 調圧水槽・排水機場・樋管の位置と向き、柱の配置(5列×12本から1本を除いた模式)、流入口の取り付け位置: 公表資料に記載なし(模式)
- 庄和排水機場の累積排水量: 第1報 約262万m³ と 出水概要 5.3百万m³ が不一致 → 採用せず(要確認)
- 1〜3号ポンプの運転、トンネル内・調圧水槽内の水位の時系列、公式X 6/5の投稿: データなし/未確認
- 水の動き・音は演出。階数換算(67m÷3.8m≒18階)は林野庁資料の階高3.5〜4.5m程度の範囲内の仮定(公的な標準階高は確認できず)
- 春日部経済新聞の記事(837万m³等): 年が異なる別の出水と判断し不使用