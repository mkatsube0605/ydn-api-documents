

# ReportClosedDateRecord

ReportClosedDateRecordオブジェクトは、レポート集計完了日付取得の詳細を表します。

### Service

+ [ReportDefinitionService](../../services/ReportDefinitionService.md)

### Namespace

[ReportDefinitionService#Namespace](../../services/ReportDefinitionService.md#namespace)

### Inheritance

+ [ReturnValue](../Common/ReturnValue.md)

| Field | Type | Description | response |
| ----- | ---- | ----------- | -------- |
| key | xsd:string | レポート集計完了日付取得のキーです。<br>※以下の内容が返されます。<br>- FREQ_REPORT_CLOSED_DATE：フリークエンシーレポートの最新データ取得可能日<br>- REPORT_CLOSED_DATE：パフォーマンスレポートの最新データ取得可能日<br>- REACH_REPORT_CLOSED_DATE：リーチレポートの最新データ取得可能日<br> | yes | |
| closedDate | xsd:string | レポート集計完了日です。 | yes | |

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
