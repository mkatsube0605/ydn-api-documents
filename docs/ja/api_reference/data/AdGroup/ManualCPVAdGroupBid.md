

# ManualCPVAdGroupBid

ManualCPVAdGroupBidオブジェクトは、広告グループの入札価格（CPV）を保持します。
※広告掲載方式がVIDEO_AD(動画広告)のキャンペーンIDを指定した時のみ利用可能です。

### Service

+ [AdGroupService](../../services/AdGroupService.md)

### Namespace

[AdGroupService#Namespace](../../services/AdGroupService.md#namespace)

| Field | Type | Description | response | get | add | set | remove |
| ----- | ---- | ----------- | -------- | --------- | --------- | --------- | --------- |
| type | enum <a href="./BiddingStrategyType.md">BiddingStrategyType</a> | 入札方法です。 | yes | - | Requirement | Requirement<br/>NotUpdatable | Ignore<br/>NotUpdatable | |
| maxCpv | xsd:long | 入札価格です。 | yes | - | Requirement | Requirement<br/>Updatable | Ignore<br/>NotUpdatable | |

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
