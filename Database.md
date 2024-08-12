# 京セラNVF-01のデータベース

中に入っているSQLite3データベースについての説明を想像で書きます。

## 一覧

`/var/cachedb`と`/mnt/khems/equip`にあるSQLite3データベースのファイル名はほとんど同じです。
共通の名前を列挙します:

- `bt_10min_average.db`
- `bt_10min_remain.db`
- `bt_average.db`
- `bt_remain.db`
- `bt_total.db`
- `gas_total.db`
- `hw_10min_remain.db`
- `hw_remain.db`
- `ope_hist.db`
- `output_control.db`
- `pcs_control.db`
- `pv_10min_average.db`
- `pv_10min_controler_2.db`
- `pv_10min_controler_3.db`
- `pv_10min_controler_4.db`
- `pv_10min_controler_5.db`
- `pv_10min_controler_6.db`
- `pv_average.db`
- `pv_peak.db`
- `pv_total.db`
- `sensor_10min_average201.db`
- `sensor_10min_average202.db`
- `sensor_10min_average203.db`
- `sensor_10min_average204.db`
- `sensor_10min_average205.db`
- `sensor_10min_average206.db`
- `sensor_10min_average207.db`
- `sensor_10min_average208.db`
- `sensor_10min_average209.db`
- `sensor_10min_average210.db`
- `sensor_10min_average211.db`
- `sensor_10min_average212.db`
- `sensor_10min_average213.db`
- `sensor_10min_average214.db`
- `sensor_10min_average215.db`
- `sensor_10min_average216.db`
- `sensor_10min_average217.db`
- `sensor_10min_average218.db`
- `sensor_10min_average219.db`
- `sensor_10min_average220.db`
- `sensor_10min_average221.db`
- `sensor_10min_average222.db`
- `sensor_10min_average223.db`
- `sensor_10min_average224.db`
- `sensor_10min_average225.db`
- `sensor_10min_average226.db`
- `sensor_10min_average227.db`
- `sensor_10min_average228.db`
- `sensor_10min_average229.db`
- `sensor_10min_average230.db`
- `sensor_10min_average231.db`
- `sensor_10min_average232.db`
- `sensor_10min_average233.db`
- `sensor_10min_average234.db`
- `sensor_10min_average235.db`
- `sensor_10min_average236.db`
- `sensor_10min_average300.db`
- `sensor_10min_average301.db`
- `sensor_10min_average302.db`
- `sensor_average201.db`
- `sensor_average202.db`
- `sensor_average203.db`
- `sensor_average204.db`
- `sensor_average205.db`
- `sensor_average206.db`
- `sensor_average207.db`
- `sensor_average208.db`
- `sensor_average209.db`
- `sensor_average210.db`
- `sensor_average211.db`
- `sensor_average212.db`
- `sensor_average213.db`
- `sensor_average214.db`
- `sensor_average215.db`
- `sensor_average216.db`
- `sensor_average217.db`
- `sensor_average218.db`
- `sensor_average219.db`
- `sensor_average220.db`
- `sensor_average221.db`
- `sensor_average222.db`
- `sensor_average223.db`
- `sensor_average224.db`
- `sensor_average225.db`
- `sensor_average226.db`
- `sensor_average227.db`
- `sensor_average228.db`
- `sensor_average229.db`
- `sensor_average230.db`
- `sensor_average231.db`
- `sensor_average232.db`
- `sensor_average233.db`
- `sensor_average234.db`
- `sensor_average235.db`
- `sensor_average236.db`
- `sensor_average300.db`
- `sensor_average301.db`
- `sensor_average302.db`
- `sensor_total201.db`
- `sensor_total202.db`
- `sensor_total203.db`
- `sensor_total204.db`
- `sensor_total205.db`
- `sensor_total206.db`
- `sensor_total207.db`
- `sensor_total208.db`
- `sensor_total209.db`
- `sensor_total210.db`
- `sensor_total211.db`
- `sensor_total212.db`
- `sensor_total213.db`
- `sensor_total214.db`
- `sensor_total215.db`
- `sensor_total216.db`
- `sensor_total217.db`
- `sensor_total218.db`
- `sensor_total219.db`
- `sensor_total220.db`
- `sensor_total221.db`
- `sensor_total222.db`
- `sensor_total223.db`
- `sensor_total224.db`
- `sensor_total225.db`
- `sensor_total226.db`
- `sensor_total227.db`
- `sensor_total228.db`
- `sensor_total229.db`
- `sensor_total230.db`
- `sensor_total231.db`
- `sensor_total232.db`
- `sensor_total233.db`
- `sensor_total234.db`
- `sensor_total235.db`
- `sensor_total236.db`
- `sensor_total300.db`
- `sensor_total301.db`
- `sensor_total302.db`
- `v2h_10min_average.db`
- `v2h_10min_remain.db`
- `v2h_average.db`
- `v2h_remain.db`
- `v2h_total.db`
- `water_total.db`

共通でない名前を列挙します:

- `/mnt/khems/equip`にしかないもの:
  - `output_control.db`
- `/mnt/khems`の下の異なるパスにあるもの:
  - `error.db`: `/mnt/khems/error`
  - `state_for_http.db`: `/mnt/khems/error`
  - `setting.db`: `/mnt/khems/config`
- `/var/cachedb`にしかないもの:
  - `electric_price.db`
  - `holiday.db`
  - `hw_10min_electric_energy.db`
  - `hw_10min_power.db`
  - `hw_operation_plan.db`
  - `money.db`
  - `prediction_10min.db`
  - `surplus_power.db`
  - `tempinfo.db`
  - `weatherforecast.db`

## 注目ファイル

なんかたくさんあってよくわからないので、明らかに重要そうなものをピックアップしました:

- `sensor_total300.db`: 売電電力と売電価格、積算値
- `sensor_total301.db`: 買電電力と買電価格、積算値
- `pv_peak.db`: 発電ピーク値
- `sensor_average300.db`: 売電電力、分単位の平均値
- `sensor_average301.db`: 買電電力、分単位の平均値
- `error.db`: エラー情報?
- `sensor_10min_average300.db`: 売電電力、10分単位の平均値
- `sensor_10min_average301.db`: 買電電力、10分単位の平均値
- `pv_10min_average.db`: 発電電力、10分単位の平均値
- `pv_total.db`: 発電電力、積算値
- `pv_average.db`: 発電電力、分単位の平均値

内容は推定なのですがたぶんこんな感じかと思います。
エラーを除いて分類すると、まず取得データは以下の3種類:

- pv: 発電電力
- sensor 300: 売電電力
- sensor 301: 買電電力

それぞれについて以下のデータ:

- total: 積算値
- average: 分単位の平均値
- 10min average: 10分単位の平均値

発電電力のみ以下のデータも:

- peak: ピーク値

## テーブル

さらに詳しく見ると、以下のテーブルがあります:

- total: hour, day, month, year, total
- average: minute
- 10min average: minute
- peak: day\_peak, month\_peak, year\_peak

これらすべてのテーブルに共通して、`date`というカラムがあります。
このカラムは整数値で、各テーブルについて以下の値を持ちます:

- total: 0
- year, year\_peak: YY
- month, month\_peak: YYMM
- day, day\_peak: YYMMDD
- hour: YYMMDDhh
- minute: YYMMDDhhmm

YYMMDDhhmmというのは、おわかりかとは思いますが、例えば2024-02-14 22:11を2402142211と表すものです。
それ以外のカラムについては以下のようになっています:

- `value`: 値(W) (共通)
- `yen`: 価格(円) (sensor totalおよびsensor 10min average)
- `value2`: 不明 (pv total, pv average)

## アクセス

TELNETでログインすれば、`sqlite3`コマンドが使えますので、とても簡単にアクセスできます。

```
root@freescale ~$ sqlite3 /var/cachedb/pv_peak.db 'select * from day_peak limit 1'
240720|2622
```

古いデータは消されていきますので、手元に残したい場合は各データベースのダンプをとっておくといいのではないでしょうか。
