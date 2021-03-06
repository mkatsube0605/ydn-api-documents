# RetargetingTagService

RetargetingTagServiceでは、サイトリターゲティングのタグに関する情報の取得・作成を行います。

#### WSDL

| environment |                                      url                                      |
| ----------- | ----------------------------------------------------------------------------- |
| production  | https://location.im.yahooapis.jp/services/V201911/RetargetingTagService?wsdl |
| sandbox     | https://sandbox.im.yahooapis.jp/services/V201911/RetargetingTagService?wsdl  |

#### Namespace

http://im.yahooapis.jp/V201911/RetargetingTag

#### Service Overview

サイトリターゲティングタグに関する情報の取得・作成を行います。

#### Operation

RetargetingTagServiceで提供される操作を説明します。

+ [get](#get)
+ [mutate(ADD)](#mutateadd)

## get

### リクエスト

サイトリターゲティングのタグに関する情報の取得を行います。

| パラメータ | 必須 | データ型 |
| ---------- | ---- | -------- |
| selector | Yes | [RetargetingTagSelector](../data/RetargetingTag/RetargetingTagSelector.md) |

##### ＜リクエストサンプル＞
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <RequestHeader xmlns="http://im.yahooapis.jp/V201911/RetargetingTag" xmlns:ns2="http://im.yahooapis.jp/V201911">
      <ns2:license>1111-1111-1111-1111</ns2:license>
      <ns2:apiAccountId>2222-2222-2222-2222</ns2:apiAccountId>
      <ns2:apiAccountPassword>password</ns2:apiAccountPassword>
    </RequestHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <get xmlns="http://im.yahooapis.jp/V201911/RetargetingTag">
      <selector>
        <accountId>1111</accountId>
      </selector>
    </get>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

### レスポンス

| パラメータ | データ型 |
| -------- | ------- |
| rval | [RetargetingTagPage](../data/RetargetingTag/RetargetingTagPage.md) |

##### ＜レスポンスサンプル＞
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <ResponseHeader xmlns="http://im.yahooapis.jp/V201911/RetargetingTag" xmlns:ns2="http://im.yahooapis.jp/V201911">
      <ns2:service>RetargetingTag</ns2:service>
      <ns2:requestTime>1574652131117</ns2:requestTime>
      <ns2:timeTakenSeconds>0.2671</ns2:timeTakenSeconds>
    </ResponseHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <ns2:getResponse xmlns="http://im.yahooapis.jp/V201911" xmlns:ns2="http://im.yahooapis.jp/V201911/RetargetingTag">
      <ns2:rval>
        <totalNumEntries>1</totalNumEntries>
        <ns2:values>
          <operationSucceeded>true</operationSucceeded>
          <ns2:retargetingTag>
            <ns2:retargetingTagId>AAAAAA</ns2:retargetingTagId>
            <ns2:accountId>1111</ns2:accountId>
            <ns2:approvalStatus>AVAILABLE</ns2:approvalStatus>
            <ns2:tag>&amp;lt;!-- Yahoo Code for your Target List --&amp;gt;
&amp;lt;script type="text/javascript" language="javascript"&amp;gt;
/* &amp;lt;![CDATA[ */
var yahoo_retargeting_id = 'XXXXXXXXXXXXXXXXXX';
var yahoo_retargeting_label = '';
var yahoo_retargeting_page_type = '';
var yahoo_retargeting_items = [{item_id: '', category_id: '', price: '', quantity: ''}];
/* ]]&amp;gt; */
&amp;lt;/script&amp;gt;
&amp;lt;script type="text/javascript" language="javascript" src="https://b92.yahoo.co.jp/js/s_retargeting.js"&amp;gt;&amp;lt;/script&amp;gt;</ns2:tag>
          </ns2:retargetingTag>
        </ns2:values>
      </ns2:rval>
    </ns2:getResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

## mutate(ADD)

### リクエスト

サイトリターゲティングのタグに関する情報を作成します。

| パラメータ | 必須 | データ型 |
| ---------- | ---- | -------- |
| operations | Yes | [RetargetingTagOperation](../data/RetargetingTag/RetargetingTagOperation.md) |

##### ＜リクエストサンプル＞
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <RequestHeader xmlns="http://im.yahooapis.jp/V201911/RetargetingTag" xmlns:ns2="http://im.yahooapis.jp/V201911">
      <ns2:license>1111-1111-1111-1111</ns2:license>
      <ns2:apiAccountId>2222-2222-2222-2222</ns2:apiAccountId>
      <ns2:apiAccountPassword>password</ns2:apiAccountPassword>
    </RequestHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <mutate xmlns="http://im.yahooapis.jp/V201911/RetargetingTag">
      <operations>
        <operator>ADD</operator>
        <accountId>1234</accountId>
      </operations>
    </mutate>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

### レスポンス

| パラメータ | データ型 |
| -------- | ------- |
| rval | [RetargetingTagReturnValue](../data/RetargetingTag/RetargetingTagReturnValue.md) |

##### ＜レスポンスサンプル＞
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <ResponseHeader xmlns="http://im.yahooapis.jp/V201911/RetargetingTag" xmlns:ns2="http://im.yahooapis.jp/V201911">
      <ns2:service>RetargetingTag</ns2:service>
      <ns2:requestTime>1574652131173</ns2:requestTime>
      <ns2:timeTakenSeconds>0.2671</ns2:timeTakenSeconds>
    </ResponseHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <ns2:mutateResponse xmlns="http://im.yahooapis.jp/V201911" xmlns:ns2="http://im.yahooapis.jp/V201911/RetargetingTag">
      <ns2:rval>
        <ListReturnValue.Type>RetargetingTagReturnValue</ListReturnValue.Type>
        <Operation.Type>ADD</Operation.Type>
        <ns2:values>
          <operationSucceeded>true</operationSucceeded>
          <ns2:retargetingTag>
            <ns2:retargetingTagId>AAAAAA</ns2:retargetingTagId>
            <ns2:accountId>1111</ns2:accountId>
            <ns2:approvalStatus>AVAILABLE</ns2:approvalStatus>
            <ns2:tag>&amp;lt;!-- Yahoo Code for your Target List --&amp;gt;
&amp;lt;script type="text/javascript" language="javascript"&amp;gt;
/* &amp;lt;![CDATA[ */
var yahoo_retargeting_id = 'XXXXXXXXXXXXXXXXXX';
var yahoo_retargeting_label = '';
var yahoo_retargeting_page_type = '';
var yahoo_retargeting_items = [{item_id: '', category_id: '', price: '', quantity: ''}];
/* ]]&amp;gt; */
&amp;lt;/script&amp;gt;
&amp;lt;script type="text/javascript" language="javascript" src="https://b92.yahoo.co.jp/js/s_retargeting.js"&amp;gt;&amp;lt;/script&amp;gt;</ns2:tag>
          </ns2:retargetingTag>
        </ns2:values>
      </ns2:rval>
    </ns2:mutateResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
