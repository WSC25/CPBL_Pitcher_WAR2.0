# WAR2.0
# 日本原文(1.02)
RA＝｛（0.297×uBB＋0.327×HBP-0.108×奪三振＋1.401×被HR＋0.036×滾地球-0.124×内野飛球＋0.132×外野飛球＋0.289×平飛球）÷（奪三振＋0.745×滾地球＋0.304×平飛球＋0.994×内野飛球＋0.675×外野飛球）×27｝+定数

*定数=全體[聯盟 ERA｛（0.297×uBB＋0.327×HBP-0.108×奪三振＋1.401×被HR＋0.036×滾地球-0.124×内野飛球＋0.132×外野飛球＋0.289×平飛球）÷（奪三振＋0.745×滾地球＋0.304×平飛球＋0.994×内野飛球＋0.675×外野飛球）×27｝]

PF補正値（tRA から減算）＝（本拠地球場での対戦打席数÷総対戦打席数）×（本拠地試合での両軍合わせた tRA －それ以外の試合での両軍合わせた tRA）

SPRAR＝（1.39×聯盟平均tRA－PF補正後tRA）÷9×（獲得出局數÷3）
RPRAR＝（1.34×聯盟平均tRA－PF補正後tRA）÷9×（獲得出局數÷3）
WAR（投手）＝（SPRAR＋RPRAR）÷RPW

## 1.CPBL 2023版本
分子係數:該狀態下RE24平均
分母係數:該狀態下的出局比例


| 狀態 | RE24 | 出局比例 |
| ------------- | ------------- | ------------- |
| uBB | 0.354188 |
| HBP | 0.372947 |
| SO | -0.304666 |
| HR | 1.711948 |
| 滾地球 | -0.077254 | 0.709957 |
| 內野飛球 | 0.300934 | 0.987002 |
| 外野飛球 | -0.048510 | 0.711651 |
| 平飛球 | 0.307350 | 0.290352 |

1-1.定数=全體 [ 聯盟ERA-｛（ 0.354188×uBB＋0.372947×HBP -0.304666×奪三振＋1.711948×被HR -0.077254×滾地球+0.300934×内野飛球-0.048510×外野飛球＋0.307350×平飛球）÷（奪三振+0.709957×滾地球+0.290352×平飛球+0.987002×内野飛球+0.711651×外野飛球）×27｝]

1-2.RA=｛（0.354188×uBB＋0.372947×HBP -0.304666×奪三振＋1.711948×被HR -0.077254×滾地球+0.300934×内野飛球-0.048510×外野飛球＋0.307350×平飛球）÷（奪三振+0.709957×滾地球+0.290352×平飛球+0.987002×内野飛球+0.711651×外野飛球）×27｝+定数

## 2.CPBL 2022版本
分子係數:該狀態下RE24平均
分母係數:該狀態下的出局比例
| 狀態 | RE24 | 出局比例 |
| ------------- | ------------- | ------------- |
| uBB | 0.311522 |
| HBP | 0.328145 |
| SO | -0.27208 |
| HR | 1.657671 |
| 滾地球 | -0.0554 | 0.712091 |
| 內野飛球 | 0.065453 | 0.710578 |
| 外野飛球 | -0.26825 | 0.982011 |
| 平飛球 | 0.327159 | 0.261841 |

2-1.定数=全體 [ 聯盟ERA-｛（ 0.311522×uBB＋0.328145×HBP -0.27208×奪三振＋1.657671×被HR -0.0554×滾地球+0.065453×内野飛球-0.26825×外野飛球＋0.327159×平飛球）÷（奪三振+0.712091×滾地球+0.261841×平飛球+0.710578×内野飛球+0.982011×外野飛球）×27｝]

2-2.RA=｛（ 0.311522×uBB＋0.328145×HBP -0.27208×奪三振＋1.657671×被HR -0.0554×滾地球+0.065453×内野飛球-0.26825×外野飛球＋0.327159×平飛球）÷（奪三振+0.712091×滾地球+0.261841×平飛球+0.710578×内野飛球+0.982011×外野飛球）×27｝+定数

3.球場因素修正值（从tRA中减去）--> 改為一般的Park Factor
並計算各球員的平均PF

4.RAR＝（1.356×聯盟平均tRA－PF補正後tRA）÷9×（獲得出局數÷3）
取SPRAR(1.39)和RPRAR(1.34) 平均數1.365

5.計算Run per Win
是指增加一場勝利所需的得分數量。通常來說，總得分增加10分（或總失分減少10分）會使球隊的勝場增加一場。RPW通常等於10。
原日本公式: RPW = 10 × SQRT（兩隊每局平均得分）
日本公式下 CPBL_2023_RPW  = 6.8593172473

FG公式: RPW = 9*(MLB Runs Scored / MLB Innings Pitched)*1.5 + 3
FG公式下 CPBL_2023_RPW  = 9.35166
場數校正:9.35166*120/162=6.9272

6.計算WAR
WAR = RAR/RPW





