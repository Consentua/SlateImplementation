---
title: Consentua Service API
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - ruby: Ruby
  - python: Python
  - java: Java
  - go: Go
toc_footers:
  - <a href='https://consentua.com'>Get Consentua</a>
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="Consentua-Service-API">Consentua Service API v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="https://test.consentua.com/">https://test.consentua.com/</a>

<h1 id="Consentua-Service-API-ConsentTemplate">ConsentTemplate</h1>

## Get

<a id="opIdGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://test.consentua.com//template/Get?clientId=0&serviceId=0&accessToken=string&language=string \
  -H 'Accept: application/json'

```

```http
GET https://test.consentua.com//template/Get?clientId=0&serviceId=0&accessToken=string&language=string HTTP/1.1
Host: test.consentua.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//template/Get',
  method: 'get',
  data: '?clientId=0&serviceId=0&accessToken=string&language=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://test.consentua.com//template/Get?clientId=0&serviceId=0&accessToken=string&language=string',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://test.consentua.com//template/Get',
  params: {
  'clientId' => 'integer(int32)',
'serviceId' => 'integer(int32)',
'accessToken' => 'string',
'language' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://test.consentua.com//template/Get', params={
  'clientId': '0',  'serviceId': '0',  'accessToken': 'string',  'language': 'string'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//template/Get?clientId=0&serviceId=0&accessToken=string&language=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://test.consentua.com//template/Get", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /template/Get`

*Gets the consent templates for a given service*

<h3 id="get-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|clientId|query|integer(int32)|true|none|
|serviceId|query|integer(int32)|true|none|
|accessToken|query|string|true|none|
|language|query|string|true|none|

> Example responses

> 200 Response

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "Token": "string",
  "Success": true,
  "Message": "string",
  "Templates": [
    {
      "Id": 0,
      "OwnerId": 0,
      "Public": true,
      "Name": "string",
      "Language": "string",
      "Question": "string",
      "Explanation": "string",
      "DataUseText": "string",
      "DataPurposeText": "string",
      "ConsentType": "string",
      "DisplayType": "string",
      "InteractionUrl": "string",
      "Version": 0,
      "Notifiable": true,
      "NotifyMethod": "string",
      "PurposeGroups": [
        {
          "Id": 0,
          "Language": "string",
          "Description": "string",
          "Explanation": "string",
          "ConsentType": "string",
          "DisplayType": "string",
          "ConsentTemplateId": 0,
          "Deleted": true,
          "Purposes": [
            {
              "Id": 0,
              "Language": "string",
              "DataUse": "string",
              "DataUseText": "string",
              "DataPurpose": "string",
              "DataPurposeText": "string",
              "URI": "string",
              "Category": "string",
              "ThirdPartyDisclosure": true,
              "ThirdPartyName": "string",
              "IsSensitive": true,
              "SensitiveCategory": "string",
              "TerminationURI": "string",
              "Position": 0,
              "PurposeGroupId": 0,
              "ConsentTemplateId": 0,
              "InteractionUrl": "string",
              "Version": 0,
              "DataTypeId": 0,
              "Deleted": true,
              "ServiceId": 0
            }
          ]
        }
      ]
    }
  ]
}
```

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "Token": "string",
  "Success": true,
  "Message": "string",
  "Templates": [
    {
      "Id": 0,
      "OwnerId": 0,
      "Public": true,
      "Name": "string",
      "Language": "string",
      "Question": "string",
      "Explanation": "string",
      "DataUseText": "string",
      "DataPurposeText": "string",
      "ConsentType": "string",
      "DisplayType": "string",
      "InteractionUrl": "string",
      "Version": 0,
      "Notifiable": true,
      "NotifyMethod": "string",
      "PurposeGroups": [
        {
          "Id": 0,
          "Language": "string",
          "Description": "string",
          "Explanation": "string",
          "ConsentType": "string",
          "DisplayType": "string",
          "ConsentTemplateId": 0,
          "Deleted": true,
          "Purposes": [
            {
              "Id": 0,
              "Language": "string",
              "DataUse": "string",
              "DataUseText": "string",
              "DataPurpose": "string",
              "DataPurposeText": "string",
              "URI": "string",
              "Category": "string",
              "ThirdPartyDisclosure": true,
              "ThirdPartyName": "string",
              "IsSensitive": true,
              "SensitiveCategory": "string",
              "TerminationURI": "string",
              "Position": 0,
              "PurposeGroupId": 0,
              "ConsentTemplateId": 0,
              "InteractionUrl": "string",
              "Version": 0,
              "DataTypeId": 0,
              "Deleted": true,
              "ServiceId": 0
            }
          ]
        }
      ]
    }
  ]
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ConsentTemplateResponseModel>
  <ClientId>0</ClientId>
  <ServiceId>0</ServiceId>
  <Token>string</Token>
  <Success>true</Success>
  <Message>string</Message>
  <Templates>
    <Id>0</Id>
    <OwnerId>0</OwnerId>
    <Public>true</Public>
    <Name>string</Name>
    <Language>string</Language>
    <Question>string</Question>
    <Explanation>string</Explanation>
    <DataUseText>string</DataUseText>
    <DataPurposeText>string</DataPurposeText>
    <ConsentType>string</ConsentType>
    <DisplayType>string</DisplayType>
    <InteractionUrl>string</InteractionUrl>
    <Version>0</Version>
    <Notifiable>true</Notifiable>
    <NotifyMethod>string</NotifyMethod>
    <PurposeGroups>
      <Id>0</Id>
      <Language>string</Language>
      <Description>string</Description>
      <Explanation>string</Explanation>
      <ConsentType>string</ConsentType>
      <DisplayType>string</DisplayType>
      <ConsentTemplateId>0</ConsentTemplateId>
      <Deleted>true</Deleted>
      <Purposes>
        <Id>0</Id>
        <Language>string</Language>
        <DataUse>string</DataUse>
        <DataUseText>string</DataUseText>
        <DataPurpose>string</DataPurpose>
        <DataPurposeText>string</DataPurposeText>
        <URI>string</URI>
        <Category>string</Category>
        <ThirdPartyDisclosure>true</ThirdPartyDisclosure>
        <ThirdPartyName>string</ThirdPartyName>
        <IsSensitive>true</IsSensitive>
        <SensitiveCategory>string</SensitiveCategory>
        <TerminationURI>string</TerminationURI>
        <Position>0</Position>
        <PurposeGroupId>0</PurposeGroupId>
        <ConsentTemplateId>0</ConsentTemplateId>
        <InteractionUrl>string</InteractionUrl>
        <Version>0</Version>
        <DataTypeId>0</DataTypeId>
        <Deleted>true</Deleted>
        <ServiceId>0</ServiceId>
      </Purposes>
    </PurposeGroups>
  </Templates>
</ConsentTemplateResponseModel>
```

> 401 Response

```json
"string"
```

```json
"string"
```

> 404 Response

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "Token": "string",
  "Success": true,
  "Message": "string",
  "Templates": [
    {
      "Id": 0,
      "OwnerId": 0,
      "Public": true,
      "Name": "string",
      "Language": "string",
      "Question": "string",
      "Explanation": "string",
      "DataUseText": "string",
      "DataPurposeText": "string",
      "ConsentType": "string",
      "DisplayType": "string",
      "InteractionUrl": "string",
      "Version": 0,
      "Notifiable": true,
      "NotifyMethod": "string",
      "PurposeGroups": [
        {
          "Id": 0,
          "Language": "string",
          "Description": "string",
          "Explanation": "string",
          "ConsentType": "string",
          "DisplayType": "string",
          "ConsentTemplateId": 0,
          "Deleted": true,
          "Purposes": [
            {
              "Id": 0,
              "Language": "string",
              "DataUse": "string",
              "DataUseText": "string",
              "DataPurpose": "string",
              "DataPurposeText": "string",
              "URI": "string",
              "Category": "string",
              "ThirdPartyDisclosure": true,
              "ThirdPartyName": "string",
              "IsSensitive": true,
              "SensitiveCategory": "string",
              "TerminationURI": "string",
              "Position": 0,
              "PurposeGroupId": 0,
              "ConsentTemplateId": 0,
              "InteractionUrl": "string",
              "Version": 0,
              "DataTypeId": 0,
              "Deleted": true,
              "ServiceId": 0
            }
          ]
        }
      ]
    }
  ]
}
```

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "Token": "string",
  "Success": true,
  "Message": "string",
  "Templates": [
    {
      "Id": 0,
      "OwnerId": 0,
      "Public": true,
      "Name": "string",
      "Language": "string",
      "Question": "string",
      "Explanation": "string",
      "DataUseText": "string",
      "DataPurposeText": "string",
      "ConsentType": "string",
      "DisplayType": "string",
      "InteractionUrl": "string",
      "Version": 0,
      "Notifiable": true,
      "NotifyMethod": "string",
      "PurposeGroups": [
        {
          "Id": 0,
          "Language": "string",
          "Description": "string",
          "Explanation": "string",
          "ConsentType": "string",
          "DisplayType": "string",
          "ConsentTemplateId": 0,
          "Deleted": true,
          "Purposes": [
            {
              "Id": 0,
              "Language": "string",
              "DataUse": "string",
              "DataUseText": "string",
              "DataPurpose": "string",
              "DataPurposeText": "string",
              "URI": "string",
              "Category": "string",
              "ThirdPartyDisclosure": true,
              "ThirdPartyName": "string",
              "IsSensitive": true,
              "SensitiveCategory": "string",
              "TerminationURI": "string",
              "Position": 0,
              "PurposeGroupId": 0,
              "ConsentTemplateId": 0,
              "InteractionUrl": "string",
              "Version": 0,
              "DataTypeId": 0,
              "Deleted": true,
              "ServiceId": 0
            }
          ]
        }
      ]
    }
  ]
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ConsentTemplateResponseModel>
  <ClientId>0</ClientId>
  <ServiceId>0</ServiceId>
  <Token>string</Token>
  <Success>true</Success>
  <Message>string</Message>
  <Templates>
    <Id>0</Id>
    <OwnerId>0</OwnerId>
    <Public>true</Public>
    <Name>string</Name>
    <Language>string</Language>
    <Question>string</Question>
    <Explanation>string</Explanation>
    <DataUseText>string</DataUseText>
    <DataPurposeText>string</DataPurposeText>
    <ConsentType>string</ConsentType>
    <DisplayType>string</DisplayType>
    <InteractionUrl>string</InteractionUrl>
    <Version>0</Version>
    <Notifiable>true</Notifiable>
    <NotifyMethod>string</NotifyMethod>
    <PurposeGroups>
      <Id>0</Id>
      <Language>string</Language>
      <Description>string</Description>
      <Explanation>string</Explanation>
      <ConsentType>string</ConsentType>
      <DisplayType>string</DisplayType>
      <ConsentTemplateId>0</ConsentTemplateId>
      <Deleted>true</Deleted>
      <Purposes>
        <Id>0</Id>
        <Language>string</Language>
        <DataUse>string</DataUse>
        <DataUseText>string</DataUseText>
        <DataPurpose>string</DataPurpose>
        <DataPurposeText>string</DataPurposeText>
        <URI>string</URI>
        <Category>string</Category>
        <ThirdPartyDisclosure>true</ThirdPartyDisclosure>
        <ThirdPartyName>string</ThirdPartyName>
        <IsSensitive>true</IsSensitive>
        <SensitiveCategory>string</SensitiveCategory>
        <TerminationURI>string</TerminationURI>
        <Position>0</Position>
        <PurposeGroupId>0</PurposeGroupId>
        <ConsentTemplateId>0</ConsentTemplateId>
        <InteractionUrl>string</InteractionUrl>
        <Version>0</Version>
        <DataTypeId>0</DataTypeId>
        <Deleted>true</Deleted>
        <ServiceId>0</ServiceId>
      </Purposes>
    </PurposeGroups>
  </Templates>
</ConsentTemplateResponseModel>
```

> 500 Response

```json
"string"
```

```json
"string"
```

<h3 id="get-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns the template details for the requested service|[ConsentTemplateResponseModel](#schemaconsenttemplateresponsemodel)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|You do Not have the appropriate access credentials!|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Templates cannot be found details in the message field of the response.|[ConsentTemplateResponseModel](#schemaconsenttemplateresponsemodel)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An error occured during processing please contact support with the returned message.|string|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="Consentua-Service-API-ConsentuaInformation">ConsentuaInformation</h1>

## GetSystemInformation

<a id="opIdGetSystemInformation"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://test.consentua.com//consentua/GetSystemInformation \
  -H 'Accept: application/json'

```

```http
GET https://test.consentua.com//consentua/GetSystemInformation HTTP/1.1
Host: test.consentua.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//consentua/GetSystemInformation',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://test.consentua.com//consentua/GetSystemInformation',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://test.consentua.com//consentua/GetSystemInformation',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://test.consentua.com//consentua/GetSystemInformation', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//consentua/GetSystemInformation");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://test.consentua.com//consentua/GetSystemInformation", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /consentua/GetSystemInformation`

> Example responses

> 200 Response

```json
{
  "InstanceName": "string",
  "Version": "string"
}
```

```json
{
  "InstanceName": "string",
  "Version": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<SystemInformation>
  <InstanceName>string</InstanceName>
  <Version>string</Version>
</SystemInformation>
```

<h3 id="getsysteminformation-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns Consentua System Information|[SystemInformation](#schemasysteminformation)|

<aside class="success">
This operation does not require authentication
</aside>

## Key

<a id="opIdKey"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://test.consentua.com//consentua/Key?key=string

```

```http
GET https://test.consentua.com//consentua/Key?key=string HTTP/1.1
Host: test.consentua.com

```

```javascript

$.ajax({
  url: 'https://test.consentua.com//consentua/Key',
  method: 'get',
  data: '?key=string',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

fetch('https://test.consentua.com//consentua/Key?key=string',
{
  method: 'GET'

})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://test.consentua.com//consentua/Key',
  params: {
  'key' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('https://test.consentua.com//consentua/Key', params={
  'key': 'string'
)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//consentua/Key?key=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://test.consentua.com//consentua/Key", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /consentua/Key`

<h3 id="key-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|key|query|string|true|none|
|serverFormat|query|boolean|false|none|

<h3 id="key-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="Consentua-Service-API-Login">Login</h1>

## Service

<a id="opIdService"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://test.consentua.com//login/Service \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test.consentua.com//login/Service HTTP/1.1
Host: test.consentua.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//login/Service',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "ClientId": 0,
  "ServiceId": 0,
  "LoginToken": "string",
  "DeviceId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://test.consentua.com//login/Service',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://test.consentua.com//login/Service',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://test.consentua.com//login/Service', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//login/Service");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test.consentua.com//login/Service", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /login/Service`

*Logs in a service*

> Body parameter

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "LoginToken": "string",
  "DeviceId": "string"
}
```

```yaml
ClientId: 0
ServiceId: 0
LoginToken: string
DeviceId: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ServiceLoginModel>
  <ClientId>0</ClientId>
  <ServiceId>0</ServiceId>
  <LoginToken>string</LoginToken>
  <DeviceId>string</DeviceId>
</ServiceLoginModel>
```

<h3 id="service-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ServiceLoginModel](#schemaserviceloginmodel)|true|The service login credentials|

> Example responses

> 200 Response

```json
{
  "Id": 0,
  "ClientId": 0,
  "Type": 0,
  "Token": "00000000-0000-0000-0000-000000000000",
  "Success": true,
  "Role": "string",
  "Message": "string"
}
```

```json
{
  "Id": 0,
  "ClientId": 0,
  "Type": 0,
  "Token": "00000000-0000-0000-0000-000000000000",
  "Success": true,
  "Role": "string",
  "Message": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<AccessTokenModel>
  <Id>0</Id>
  <ClientId>0</ClientId>
  <Type>0</Type>
  <Token>00000000-0000-0000-0000-000000000000</Token>
  <Success>true</Success>
  <Role>string</Role>
  <Message>string</Message>
</AccessTokenModel>
```

> 401 Response

```json
{
  "Id": 0,
  "ClientId": 0,
  "Type": 0,
  "Token": "00000000-0000-0000-0000-000000000000",
  "Success": true,
  "Role": "string",
  "Message": "string"
}
```

```json
{
  "Id": 0,
  "ClientId": 0,
  "Type": 0,
  "Token": "00000000-0000-0000-0000-000000000000",
  "Success": true,
  "Role": "string",
  "Message": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<AccessTokenModel>
  <Id>0</Id>
  <ClientId>0</ClientId>
  <Type>0</Type>
  <Token>00000000-0000-0000-0000-000000000000</Token>
  <Success>true</Success>
  <Role>string</Role>
  <Message>string</Message>
</AccessTokenModel>
```

<h3 id="service-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Service Logged in please use the provided token to access the API|[AccessTokenModel](#schemaaccesstokenmodel)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Invalid Login Credentials|[AccessTokenModel](#schemaaccesstokenmodel)|

<aside class="success">
This operation does not require authentication
</aside>

## IsLoggedIn

<a id="opIdIsLoggedIn"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://test.consentua.com//login/IsLoggedIn?token=string

```

```http
GET https://test.consentua.com//login/IsLoggedIn?token=string HTTP/1.1
Host: test.consentua.com

```

```javascript

$.ajax({
  url: 'https://test.consentua.com//login/IsLoggedIn',
  method: 'get',
  data: '?token=string',

  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

fetch('https://test.consentua.com//login/IsLoggedIn?token=string',
{
  method: 'GET'

})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://test.consentua.com//login/IsLoggedIn',
  params: {
  'token' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('https://test.consentua.com//login/IsLoggedIn', params={
  'token': 'string'
)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//login/IsLoggedIn?token=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://test.consentua.com//login/IsLoggedIn", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /login/IsLoggedIn`

*Checks to see if the supplied token is logged in or not.*

<h3 id="isloggedin-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|token|query|string|true|the token to check|

<h3 id="isloggedin-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The supplied token is currently logged in to consentua|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|The supplied token is not logged in to consentua|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="Consentua-Service-API-Search">Search</h1>

## QueryUser

<a id="opIdQueryUser"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://test.consentua.com//search/QueryUser \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test.consentua.com//search/QueryUser HTTP/1.1
Host: test.consentua.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//search/QueryUser',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "UserId": 0,
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "Token": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://test.consentua.com//search/QueryUser',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://test.consentua.com//search/QueryUser',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://test.consentua.com//search/QueryUser', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//search/QueryUser");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test.consentua.com//search/QueryUser", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /search/QueryUser`

> Body parameter

```json
{
  "UserId": 0,
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "Token": "string"
}
```

```yaml
UserId: 0
ClientId: 0
ServiceId: 0
PurposeId: 0
Token: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<UserConsentQueryModel>
  <UserId>0</UserId>
  <ClientId>0</ClientId>
  <ServiceId>0</ServiceId>
  <PurposeId>0</PurposeId>
  <Token>string</Token>
</UserConsentQueryModel>
```

<h3 id="queryuser-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserConsentQueryModel](#schemauserconsentquerymodel)|true|none|

> Example responses

> 200 Response

```json
{
  "UserId": 0,
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "SearchId": "00000000-0000-0000-0000-000000000000",
  "Response": "string",
  "ResultsReturned": 0
}
```

```json
{
  "UserId": 0,
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "SearchId": "00000000-0000-0000-0000-000000000000",
  "Response": "string",
  "ResultsReturned": 0
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<UserConsentResponseModel>
  <UserId>0</UserId>
  <ClientId>0</ClientId>
  <ServiceId>0</ServiceId>
  <PurposeId>0</PurposeId>
  <SearchId>00000000-0000-0000-0000-000000000000</SearchId>
  <Response>string</Response>
  <ResultsReturned>0</ResultsReturned>
</UserConsentResponseModel>
```

> 404 Response

```json
"string"
```

```json
"string"
```

> 500 Response

```json
"string"
```

```json
"string"
```

<h3 id="queryuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Query Successful|[UserConsentResponseModel](#schemauserconsentresponsemodel)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|You do Not have the appropriate access credentials!|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|User or service not found please refer to the response for details|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An error occured during processing please contact support with the returned message.|string|

<aside class="success">
This operation does not require authentication
</aside>

## QueryPurpose

<a id="opIdQueryPurpose"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://test.consentua.com//search/QueryPurpose \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test.consentua.com//search/QueryPurpose HTTP/1.1
Host: test.consentua.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//search/QueryPurpose',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "Token": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://test.consentua.com//search/QueryPurpose',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://test.consentua.com//search/QueryPurpose',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://test.consentua.com//search/QueryPurpose', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//search/QueryPurpose");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test.consentua.com//search/QueryPurpose", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /search/QueryPurpose`

> Body parameter

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "Token": "string"
}
```

```yaml
ClientId: 0
ServiceId: 0
PurposeId: 0
Token: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<InverseConsentQueryModel>
  <ClientId>0</ClientId>
  <ServiceId>0</ServiceId>
  <PurposeId>0</PurposeId>
  <Token>string</Token>
</InverseConsentQueryModel>
```

<h3 id="querypurpose-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[InverseConsentQueryModel](#schemainverseconsentquerymodel)|true|none|

> Example responses

> 200 Response

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "SearchId": "00000000-0000-0000-0000-000000000000",
  "Message": "string",
  "Response": [
    "string"
  ],
  "ResultsReturned": 0
}
```

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "SearchId": "00000000-0000-0000-0000-000000000000",
  "Message": "string",
  "Response": [
    "string"
  ],
  "ResultsReturned": 0
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<InverseConsentResponseModel>
  <ClientId>0</ClientId>
  <ServiceId>0</ServiceId>
  <PurposeId>0</PurposeId>
  <SearchId>00000000-0000-0000-0000-000000000000</SearchId>
  <Message>string</Message>
  <Response>string</Response>
  <ResultsReturned>0</ResultsReturned>
</InverseConsentResponseModel>
```

> 404 Response

```json
"string"
```

```json
"string"
```

> 500 Response

```json
"string"
```

```json
"string"
```

<h3 id="querypurpose-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Query Successful|[InverseConsentResponseModel](#schemainverseconsentresponsemodel)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|You do Not have the appropriate access credentials!|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|User or service not found please refer to the response for details|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An error occured during processing please contact support with the returned message.|string|

<aside class="success">
This operation does not require authentication
</aside>

## GetServiceSearches

<a id="opIdGetServiceSearches"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://test.consentua.com//search/GetServiceSearches \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test.consentua.com//search/GetServiceSearches HTTP/1.1
Host: test.consentua.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//search/GetServiceSearches',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "ClientId": 0,
  "ServiceId": 0,
  "Token": "string",
  "Start": "2018-06-11T14:02:37Z",
  "End": "2018-06-11T14:02:37Z"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://test.consentua.com//search/GetServiceSearches',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://test.consentua.com//search/GetServiceSearches',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://test.consentua.com//search/GetServiceSearches', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//search/GetServiceSearches");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test.consentua.com//search/GetServiceSearches", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /search/GetServiceSearches`

> Body parameter

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "Token": "string",
  "Start": "2018-06-11T14:02:37Z",
  "End": "2018-06-11T14:02:37Z"
}
```

```yaml
ClientId: 0
ServiceId: 0
Token: string
Start: '2018-06-11T14:02:37Z'
End: '2018-06-11T14:02:37Z'

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ServiceSearchModel>
  <ClientId>0</ClientId>
  <ServiceId>0</ServiceId>
  <Token>string</Token>
  <Start>2018-06-11T14:02:37Z</Start>
  <End>2018-06-11T14:02:37Z</End>
</ServiceSearchModel>
```

<h3 id="getservicesearches-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ServiceSearchModel](#schemaservicesearchmodel)|true|none|

> Example responses

> 200 Response

```json
[
  {
    "ServiceOwner": "string",
    "Service": "string",
    "UserId": 0,
    "SearchTime": "2018-06-11T14:02:37Z",
    "SearchId": "string",
    "Result": "string"
  }
]
```

```json
[
  {
    "ServiceOwner": "string",
    "Service": "string",
    "UserId": 0,
    "SearchTime": "2018-06-11T14:02:37Z",
    "SearchId": "string",
    "Result": "string"
  }
]
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ServiceOwner>string</ServiceOwner>
<Service>string</Service>
<UserId>0</UserId>
<SearchTime>2018-06-11T14:02:37Z</SearchTime>
<SearchId>string</SearchId>
<Result>string</Result>
```

> 404 Response

```json
"string"
```

```json
"string"
```

> 500 Response

```json
"string"
```

```json
"string"
```

<h3 id="getservicesearches-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Query Successful|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|You do Not have the appropriate access credentials!|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|User or service not found please refer to the response for details|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An error occured during processing please contact support with the returned message.|string|

<h3 id="getservicesearches-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ConsentSearchModel](#schemaconsentsearchmodel)]|false|none|none|
|» ServiceOwner|string|false|none|none|
|» Service|string|false|none|none|
|» UserId|integer(int32)|false|none|none|
|» SearchTime|string(date-time)|false|none|none|
|» SearchId|string|false|none|none|
|» Result|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## GetUserSearches

<a id="opIdGetUserSearches"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://test.consentua.com//search/GetUserSearches \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test.consentua.com//search/GetUserSearches HTTP/1.1
Host: test.consentua.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//search/GetUserSearches',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "ServiceId": 0,
  "UserId": 0,
  "Token": "string",
  "Start": "2018-06-11T14:02:37Z",
  "End": "2018-06-11T14:02:37Z"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://test.consentua.com//search/GetUserSearches',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://test.consentua.com//search/GetUserSearches',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://test.consentua.com//search/GetUserSearches', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//search/GetUserSearches");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test.consentua.com//search/GetUserSearches", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /search/GetUserSearches`

> Body parameter

```json
{
  "ServiceId": 0,
  "UserId": 0,
  "Token": "string",
  "Start": "2018-06-11T14:02:37Z",
  "End": "2018-06-11T14:02:37Z"
}
```

```yaml
ServiceId: 0
UserId: 0
Token: string
Start: '2018-06-11T14:02:37Z'
End: '2018-06-11T14:02:37Z'

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<UserSearchModel>
  <ServiceId>0</ServiceId>
  <UserId>0</UserId>
  <Token>string</Token>
  <Start>2018-06-11T14:02:37Z</Start>
  <End>2018-06-11T14:02:37Z</End>
</UserSearchModel>
```

<h3 id="getusersearches-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserSearchModel](#schemausersearchmodel)|true|none|

> Example responses

> 200 Response

```json
[
  {
    "ServiceOwner": "string",
    "Service": "string",
    "UserId": 0,
    "SearchTime": "2018-06-11T14:02:37Z",
    "SearchId": "string",
    "Result": "string"
  }
]
```

```json
[
  {
    "ServiceOwner": "string",
    "Service": "string",
    "UserId": 0,
    "SearchTime": "2018-06-11T14:02:37Z",
    "SearchId": "string",
    "Result": "string"
  }
]
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ServiceOwner>string</ServiceOwner>
<Service>string</Service>
<UserId>0</UserId>
<SearchTime>2018-06-11T14:02:37Z</SearchTime>
<SearchId>string</SearchId>
<Result>string</Result>
```

> 404 Response

```json
"string"
```

```json
"string"
```

> 500 Response

```json
"string"
```

```json
"string"
```

<h3 id="getusersearches-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Query Successful|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|You do Not have the appropriate access credentials!|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|User or service not found please refer to the response for details|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An error occured during processing please contact support with the returned message.|string|

<h3 id="getusersearches-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ConsentSearchModel](#schemaconsentsearchmodel)]|false|none|none|
|» ServiceOwner|string|false|none|none|
|» Service|string|false|none|none|
|» UserId|integer(int32)|false|none|none|
|» SearchTime|string(date-time)|false|none|none|
|» SearchId|string|false|none|none|
|» Result|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="Consentua-Service-API-User">User</h1>

## GetServiceUser

<a id="opIdGetServiceUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://test.consentua.com//serviceuser/GetServiceUser?identifier=string&serviceId=0&token=string \
  -H 'Accept: application/json'

```

```http
GET https://test.consentua.com//serviceuser/GetServiceUser?identifier=string&serviceId=0&token=string HTTP/1.1
Host: test.consentua.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//serviceuser/GetServiceUser',
  method: 'get',
  data: '?identifier=string&serviceId=0&token=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://test.consentua.com//serviceuser/GetServiceUser?identifier=string&serviceId=0&token=string',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://test.consentua.com//serviceuser/GetServiceUser',
  params: {
  'identifier' => 'string',
'serviceId' => 'integer(int32)',
'token' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://test.consentua.com//serviceuser/GetServiceUser', params={
  'identifier': 'string',  'serviceId': '0',  'token': 'string'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//serviceuser/GetServiceUser?identifier=string&serviceId=0&token=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://test.consentua.com//serviceuser/GetServiceUser", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /serviceuser/GetServiceUser`

*Retrieves a user for a service*

<h3 id="getserviceuser-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|identifier|query|string|true|the identifier of the user for the service|
|serviceId|query|integer(int32)|true|The id of the service requesting the user information|
|token|query|string|true|The API access token|

> Example responses

> 200 Response

```json
{
  "UserId": 0,
  "Identifier": "string",
  "ServiceId": 0
}
```

```json
{
  "UserId": 0,
  "Identifier": "string",
  "ServiceId": 0
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ServiceUserModel>
  <UserId>0</UserId>
  <Identifier>string</Identifier>
  <ServiceId>0</ServiceId>
</ServiceUserModel>
```

> 401 Response

```json
"string"
```

```json
"string"
```

> 404 Response

```json
"string"
```

```json
"string"
```

> 500 Response

```json
"string"
```

```json
"string"
```

<h3 id="getserviceuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns the user details for the requested user|[ServiceUserModel](#schemaserviceusermodel)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|You do Not have the appropriate access credentials!|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Cannot find the requested user for this service|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An error occured during processing please contact support with the returned message.|string|

<aside class="success">
This operation does not require authentication
</aside>

## AddUserToService

<a id="opIdAddUserToService"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://test.consentua.com//serviceuser/AddUserToService?identifier=string&serviceId=0&token=string \
  -H 'Accept: application/json'

```

```http
POST https://test.consentua.com//serviceuser/AddUserToService?identifier=string&serviceId=0&token=string HTTP/1.1
Host: test.consentua.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//serviceuser/AddUserToService',
  method: 'post',
  data: '?identifier=string&serviceId=0&token=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://test.consentua.com//serviceuser/AddUserToService?identifier=string&serviceId=0&token=string',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.post 'https://test.consentua.com//serviceuser/AddUserToService',
  params: {
  'identifier' => 'string',
'serviceId' => 'integer(int32)',
'token' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.post('https://test.consentua.com//serviceuser/AddUserToService', params={
  'identifier': 'string',  'serviceId': '0',  'token': 'string'
}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//serviceuser/AddUserToService?identifier=string&serviceId=0&token=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test.consentua.com//serviceuser/AddUserToService", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /serviceuser/AddUserToService`

*Adds a user to a service*

<h3 id="addusertoservice-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|identifier|query|string|true|The user identifier in the service|
|serviceId|query|integer(int32)|true|The id of the service adding the user|
|token|query|string|true|The API access token|

> Example responses

> 200 Response

```json
{
  "UserId": 0,
  "Identifier": "string",
  "ServiceId": 0
}
```

```json
{
  "UserId": 0,
  "Identifier": "string",
  "ServiceId": 0
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<ServiceUserModel>
  <UserId>0</UserId>
  <Identifier>string</Identifier>
  <ServiceId>0</ServiceId>
</ServiceUserModel>
```

> 401 Response

```json
"string"
```

```json
"string"
```

> 404 Response

```json
"string"
```

```json
"string"
```

> 500 Response

```json
"string"
```

```json
"string"
```

<h3 id="addusertoservice-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Adds a user to the service|[ServiceUserModel](#schemaserviceusermodel)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|You do Not have the appropriate access credentials!|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Cannot find the requested user or service|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An error occured during processing please contact support with the returned message.|string|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="Consentua-Service-API-UserConsent">UserConsent</h1>

## SetConsents

<a id="opIdSetConsents"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://test.consentua.com//userconsent/SetConsents \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test.consentua.com//userconsent/SetConsents HTTP/1.1
Host: test.consentua.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//userconsent/SetConsents',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "Token": "string",
  "Consent": {
    "ClientId": 0,
    "ServiceId": 0,
    "UserId": 0,
    "Purposes": [
      {
        "ConsentTemplateId": 0,
        "PurposeId": 0,
        "Consent": true
      }
    ]
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://test.consentua.com//userconsent/SetConsents',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://test.consentua.com//userconsent/SetConsents',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://test.consentua.com//userconsent/SetConsents', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//userconsent/SetConsents");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test.consentua.com//userconsent/SetConsents", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /userconsent/SetConsents`

*Sets the consents for a service user*

> Body parameter

```json
{
  "Token": "string",
  "Consent": {
    "ClientId": 0,
    "ServiceId": 0,
    "UserId": 0,
    "Purposes": [
      {
        "ConsentTemplateId": 0,
        "PurposeId": 0,
        "Consent": true
      }
    ]
  }
}
```

```yaml
Token: string
Consent:
  ClientId: 0
  ServiceId: 0
  UserId: 0
  Purposes:
    - ConsentTemplateId: 0
      PurposeId: 0
      Consent: true

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<UserConsentAddRequestModel>
  <Token>string</Token>
  <Consent>
    <ClientId>0</ClientId>
    <ServiceId>0</ServiceId>
    <UserId>0</UserId>
    <Purposes>
      <ConsentTemplateId>0</ConsentTemplateId>
      <PurposeId>0</PurposeId>
      <Consent>true</Consent>
    </Purposes>
  </Consent>
</UserConsentAddRequestModel>
```

<h3 id="setconsents-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserConsentAddRequestModel](#schemauserconsentaddrequestmodel)|true|An array of the consents to be set|

> Example responses

> 200 Response

```json
{
  "Success": true,
  "Message": "string"
}
```

```json
{
  "Success": true,
  "Message": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<UserConsentAddResponseModel>
  <Success>true</Success>
  <Message>string</Message>
</UserConsentAddResponseModel>
```

> 401 Response

```json
"string"
```

```json
"string"
```

> 404 Response

```json
"string"
```

```json
"string"
```

> 500 Response

```json
"string"
```

```json
"string"
```

<h3 id="setconsents-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Consents have been Set|[UserConsentAddResponseModel](#schemauserconsentaddresponsemodel)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|You do Not have the appropriate access credentials!|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Cannot find user or service please check the response message|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An error occured during processing please contact support with the returned message.|string|

<aside class="success">
This operation does not require authentication
</aside>

## SetConsentsEx

<a id="opIdSetConsentsEx"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://test.consentua.com//userconsent/SetConsentsEx \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test.consentua.com//userconsent/SetConsentsEx HTTP/1.1
Host: test.consentua.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//userconsent/SetConsentsEx',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "Token": "string",
  "AuthenticationData": "string",
  "Consent": {
    "ClientId": 0,
    "ServiceId": 0,
    "UserId": 0,
    "Purposes": [
      {
        "ConsentTemplateId": 0,
        "PurposeId": 0,
        "Consent": true
      }
    ]
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://test.consentua.com//userconsent/SetConsentsEx',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://test.consentua.com//userconsent/SetConsentsEx',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://test.consentua.com//userconsent/SetConsentsEx', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//userconsent/SetConsentsEx");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test.consentua.com//userconsent/SetConsentsEx", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /userconsent/SetConsentsEx`

*Sets the consents for a service user*

> Body parameter

```json
{
  "Token": "string",
  "AuthenticationData": "string",
  "Consent": {
    "ClientId": 0,
    "ServiceId": 0,
    "UserId": 0,
    "Purposes": [
      {
        "ConsentTemplateId": 0,
        "PurposeId": 0,
        "Consent": true
      }
    ]
  }
}
```

```yaml
Token: string
AuthenticationData: string
Consent:
  ClientId: 0
  ServiceId: 0
  UserId: 0
  Purposes:
    - ConsentTemplateId: 0
      PurposeId: 0
      Consent: true

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<UserConsentAddRequestModelEx>
  <Token>string</Token>
  <AuthenticationData>string</AuthenticationData>
  <Consent>
    <ClientId>0</ClientId>
    <ServiceId>0</ServiceId>
    <UserId>0</UserId>
    <Purposes>
      <ConsentTemplateId>0</ConsentTemplateId>
      <PurposeId>0</PurposeId>
      <Consent>true</Consent>
    </Purposes>
  </Consent>
</UserConsentAddRequestModelEx>
```

<h3 id="setconsentsex-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserConsentAddRequestModelEx](#schemauserconsentaddrequestmodelex)|true|An array of the consents to be set|

> Example responses

> 200 Response

```json
{
  "Success": true,
  "Message": "string"
}
```

```json
{
  "Success": true,
  "Message": "string"
}
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<UserConsentAddResponseModel>
  <Success>true</Success>
  <Message>string</Message>
</UserConsentAddResponseModel>
```

> 401 Response

```json
"string"
```

```json
"string"
```

> 404 Response

```json
"string"
```

```json
"string"
```

> 500 Response

```json
"string"
```

```json
"string"
```

<h3 id="setconsentsex-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Consents have been Set|[UserConsentAddResponseModel](#schemauserconsentaddresponsemodel)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|You do Not have the appropriate access credentials!|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Cannot find user or service please check the response message|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An error occured during processing please contact support with the returned message.|string|

<aside class="success">
This operation does not require authentication
</aside>

## GetConsents

<a id="opIdGetConsents"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://test.consentua.com//userconsent/GetConsents \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test.consentua.com//userconsent/GetConsents HTTP/1.1
Host: test.consentua.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://test.consentua.com//userconsent/GetConsents',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "ClientId": 0,
  "ServiceId": 0,
  "UserId": 0,
  "Token": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://test.consentua.com//userconsent/GetConsents',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://test.consentua.com//userconsent/GetConsents',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://test.consentua.com//userconsent/GetConsents', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://test.consentua.com//userconsent/GetConsents");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test.consentua.com//userconsent/GetConsents", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /userconsent/GetConsents`

*Retrieves the consents for a system user*

> Body parameter

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "UserId": 0,
  "Token": "string"
}
```

```yaml
ClientId: 0
ServiceId: 0
UserId: 0
Token: string

```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<UserConsentGetRequestModel>
  <ClientId>0</ClientId>
  <ServiceId>0</ServiceId>
  <UserId>0</UserId>
  <Token>string</Token>
</UserConsentGetRequestModel>
```

<h3 id="getconsents-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserConsentGetRequestModel](#schemauserconsentgetrequestmodel)|true|The request for the consents|

> Example responses

> 200 Response

```json
[
  {
    "Success": true,
    "Message": "string",
    "Consent": {
      "ClientId": 0,
      "ServiceId": 0,
      "UserId": 0,
      "Purposes": [
        {
          "ConsentTemplateId": 0,
          "PurposeId": 0,
          "Consent": true
        }
      ]
    }
  }
]
```

```json
[
  {
    "Success": true,
    "Message": "string",
    "Consent": {
      "ClientId": 0,
      "ServiceId": 0,
      "UserId": 0,
      "Purposes": [
        {
          "ConsentTemplateId": 0,
          "PurposeId": 0,
          "Consent": true
        }
      ]
    }
  }
]
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<Success>true</Success>
<Message>string</Message>
<Consent>
  <ClientId>0</ClientId>
  <ServiceId>0</ServiceId>
  <UserId>0</UserId>
  <Purposes>
    <ConsentTemplateId>0</ConsentTemplateId>
    <PurposeId>0</PurposeId>
    <Consent>true</Consent>
  </Purposes>
</Consent>
```

> 401 Response

```json
"string"
```

```json
"string"
```

> 404 Response

```json
"string"
```

```json
"string"
```

> 500 Response

```json
"string"
```

```json
"string"
```

<h3 id="getconsents-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Consents have been Retrieved|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|You do Not have the appropriate access credentials!|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Cannot find user or service please check the response message|string|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|An error occured during processing please contact support with the returned message.|string|

<h3 id="getconsents-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[UserConsentGetResponseModel](#schemauserconsentgetresponsemodel)]|false|none|none|
|» Success|boolean|false|none|Flag to show the success/failure of the request|
|» Message|string|false|none|Message associated with the request|
|» Consent|[UserConsentModel](#schemauserconsentmodel)|false|none|none|
|»» ClientId|integer(int32)|false|none|Service Id of the service requesting the consents|
|»» ServiceId|integer(int32)|false|none|Service Id of the service requesting the consents|
|»» UserId|integer(int32)|false|none|User Id of the conset holder in the service|
|»» Purposes|[[UserPurposeConsentModel](#schemauserpurposeconsentmodel)]|false|none|An array of purposes and the user consent to those purposes|
|»»» ConsentTemplateId|integer(int32)|false|none|The id of the consent template which owns the purpose|
|»»» PurposeId|integer(int32)|false|none|The Id of the purpose of the consent|
|»»» Consent|boolean|false|none|The state of consent for the specified purpose|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocSconsenttemplateresponsemodel">ConsentTemplateResponseModel</h2>

<a id="schemaconsenttemplateresponsemodel"></a>

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "Token": "string",
  "Success": true,
  "Message": "string",
  "Templates": [
    {
      "Id": 0,
      "OwnerId": 0,
      "Public": true,
      "Name": "string",
      "Language": "string",
      "Question": "string",
      "Explanation": "string",
      "DataUseText": "string",
      "DataPurposeText": "string",
      "ConsentType": "string",
      "DisplayType": "string",
      "InteractionUrl": "string",
      "Version": 0,
      "Notifiable": true,
      "NotifyMethod": "string",
      "PurposeGroups": [
        {
          "Id": 0,
          "Language": "string",
          "Description": "string",
          "Explanation": "string",
          "ConsentType": "string",
          "DisplayType": "string",
          "ConsentTemplateId": 0,
          "Deleted": true,
          "Purposes": [
            {
              "Id": 0,
              "Language": "string",
              "DataUse": "string",
              "DataUseText": "string",
              "DataPurpose": "string",
              "DataPurposeText": "string",
              "URI": "string",
              "Category": "string",
              "ThirdPartyDisclosure": true,
              "ThirdPartyName": "string",
              "IsSensitive": true,
              "SensitiveCategory": "string",
              "TerminationURI": "string",
              "Position": 0,
              "PurposeGroupId": 0,
              "ConsentTemplateId": 0,
              "InteractionUrl": "string",
              "Version": 0,
              "DataTypeId": 0,
              "Deleted": true,
              "ServiceId": 0
            }
          ]
        }
      ]
    }
  ]
}

```

*Response model for consent template requests*

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ClientId|integer(int32)|false|none|Client Id of the Template Owner|
|ServiceId|integer(int32)|false|none|Service Id of the service the template belongs to.|
|Token|string|false|none|API access token|
|Success|boolean|false|none|A Flag denoting success|
|Message|string|false|none|The message associated with the response. for a 501 response this will be an error or exception message.|
|Templates|[[DisplayConsentTemplateModel](#schemadisplayconsenttemplatemodel)]|false|none|The list of templates associated with the service if the Success flag is true. {Consentua.API.Models.ConsentTemplateModel}|

<h2 id="tocSdisplayconsenttemplatemodel">DisplayConsentTemplateModel</h2>

<a id="schemadisplayconsenttemplatemodel"></a>

```json
{
  "Id": 0,
  "OwnerId": 0,
  "Public": true,
  "Name": "string",
  "Language": "string",
  "Question": "string",
  "Explanation": "string",
  "DataUseText": "string",
  "DataPurposeText": "string",
  "ConsentType": "string",
  "DisplayType": "string",
  "InteractionUrl": "string",
  "Version": 0,
  "Notifiable": true,
  "NotifyMethod": "string",
  "PurposeGroups": [
    {
      "Id": 0,
      "Language": "string",
      "Description": "string",
      "Explanation": "string",
      "ConsentType": "string",
      "DisplayType": "string",
      "ConsentTemplateId": 0,
      "Deleted": true,
      "Purposes": [
        {
          "Id": 0,
          "Language": "string",
          "DataUse": "string",
          "DataUseText": "string",
          "DataPurpose": "string",
          "DataPurposeText": "string",
          "URI": "string",
          "Category": "string",
          "ThirdPartyDisclosure": true,
          "ThirdPartyName": "string",
          "IsSensitive": true,
          "SensitiveCategory": "string",
          "TerminationURI": "string",
          "Position": 0,
          "PurposeGroupId": 0,
          "ConsentTemplateId": 0,
          "InteractionUrl": "string",
          "Version": 0,
          "DataTypeId": 0,
          "Deleted": true,
          "ServiceId": 0
        }
      ]
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|Id|integer(int32)|false|none|none|
|OwnerId|integer(int32)|false|none|none|
|Public|boolean|false|none|none|
|Name|string|false|none|none|
|Language|string|false|none|none|
|Question|string|false|none|none|
|Explanation|string|false|none|none|
|DataUseText|string|false|none|none|
|DataPurposeText|string|false|none|none|
|ConsentType|string|false|none|none|
|DisplayType|string|false|none|none|
|InteractionUrl|string|false|none|none|
|Version|integer(int32)|false|none|none|
|Notifiable|boolean|false|none|none|
|NotifyMethod|string|false|none|none|
|PurposeGroups|[[DisplayPurposeGroupModel](#schemadisplaypurposegroupmodel)]|false|none|none|

<h2 id="tocSdisplaypurposegroupmodel">DisplayPurposeGroupModel</h2>

<a id="schemadisplaypurposegroupmodel"></a>

```json
{
  "Id": 0,
  "Language": "string",
  "Description": "string",
  "Explanation": "string",
  "ConsentType": "string",
  "DisplayType": "string",
  "ConsentTemplateId": 0,
  "Deleted": true,
  "Purposes": [
    {
      "Id": 0,
      "Language": "string",
      "DataUse": "string",
      "DataUseText": "string",
      "DataPurpose": "string",
      "DataPurposeText": "string",
      "URI": "string",
      "Category": "string",
      "ThirdPartyDisclosure": true,
      "ThirdPartyName": "string",
      "IsSensitive": true,
      "SensitiveCategory": "string",
      "TerminationURI": "string",
      "Position": 0,
      "PurposeGroupId": 0,
      "ConsentTemplateId": 0,
      "InteractionUrl": "string",
      "Version": 0,
      "DataTypeId": 0,
      "Deleted": true,
      "ServiceId": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|Id|integer(int32)|false|none|none|
|Language|string|false|none|none|
|Description|string|false|none|none|
|Explanation|string|false|none|none|
|ConsentType|string|false|none|none|
|DisplayType|string|false|none|none|
|ConsentTemplateId|integer(int32)|false|none|none|
|Deleted|boolean|false|none|none|
|Purposes|[[PurposeModel](#schemapurposemodel)]|false|none|none|

<h2 id="tocSpurposemodel">PurposeModel</h2>

<a id="schemapurposemodel"></a>

```json
{
  "Id": 0,
  "Language": "string",
  "DataUse": "string",
  "DataUseText": "string",
  "DataPurpose": "string",
  "DataPurposeText": "string",
  "URI": "string",
  "Category": "string",
  "ThirdPartyDisclosure": true,
  "ThirdPartyName": "string",
  "IsSensitive": true,
  "SensitiveCategory": "string",
  "TerminationURI": "string",
  "Position": 0,
  "PurposeGroupId": 0,
  "ConsentTemplateId": 0,
  "InteractionUrl": "string",
  "Version": 0,
  "DataTypeId": 0,
  "Deleted": true,
  "ServiceId": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|Id|integer(int32)|false|none|The id of the purpose in consentua|
|Language|string|false|none|The default language of the purpose|
|DataUse|string|false|none|The description of the data use for this purpose|
|DataUseText|string|false|none|none|
|DataPurpose|string|false|none|The purpose for which the data will be used|
|DataPurposeText|string|false|none|none|
|URI|string|false|none|The URI describing this purpose|
|Category|string|false|none|The Category of the purpose. These can be found in appendix B of the current consent reciept specification.|
|ThirdPartyDisclosure|boolean|false|none|Is this purpose for third party disclosure|
|ThirdPartyName|string|false|none|The name or names of the third parties to be disclosed to|
|IsSensitive|boolean|false|none|none|
|SensitiveCategory|string|false|none|none|
|TerminationURI|string|false|none|Conditions for the termination of consent.|
|Position|integer(int32)|false|none|The position of the purpose within the template|
|PurposeGroupId|integer(int32)|false|none|The id of the purpose group this purpose belongs to|
|ConsentTemplateId|integer(int32)|false|none|The id of the consent template containing this purpose|
|InteractionUrl|string|false|none|The url for the purpose interaction endpoint for the web sdk|
|Version|integer(int32)|false|none|The current version of the purpose|
|DataTypeId|integer(int32)|false|none|The data type associated with the purpose|
|Deleted|boolean|false|none|Flag to show if the purpose is deleted|
|ServiceId|integer(int32)|false|none|none|

<h2 id="tocSsysteminformation">SystemInformation</h2>

<a id="schemasysteminformation"></a>

```json
{
  "InstanceName": "string",
  "Version": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|InstanceName|string|false|none|The name of this instance of consentua. Usually Test, Live or Development.|
|Version|string|false|none|The version of consentua running.|

<h2 id="tocSserviceloginmodel">ServiceLoginModel</h2>

<a id="schemaserviceloginmodel"></a>

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "LoginToken": "string",
  "DeviceId": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ClientId|integer(int32)|false|none|none|
|ServiceId|integer(int32)|false|none|none|
|LoginToken|string|false|none|none|
|DeviceId|string|false|none|none|

<h2 id="tocSaccesstokenmodel">AccessTokenModel</h2>

<a id="schemaaccesstokenmodel"></a>

```json
{
  "Id": 0,
  "ClientId": 0,
  "Type": 0,
  "Token": "00000000-0000-0000-0000-000000000000",
  "Success": true,
  "Role": "string",
  "Message": "string"
}

```

*The Token model returned from login*

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|Id|integer(int32)|false|none|The user id or service id of the login|
|ClientId|integer(int32)|false|none|The client Id of the login|
|Type|integer(int32)|false|none|The type of login 1 = user login 2 = service login|
|Token|string(uuid)|false|none|The token needed to access the consentua API|
|Success|boolean|false|none|Success flag|
|Role|string|false|none|The role of the user either SA,ADMIN, USER or SERVICE|
|Message|string|false|none|Message associated with the login attempt|

<h2 id="tocSuserconsentquerymodel">UserConsentQueryModel</h2>

<a id="schemauserconsentquerymodel"></a>

```json
{
  "UserId": 0,
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "Token": "string"
}

```

*Model for querying the consent for a user of a service for a specific purpose*

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|UserId|integer(int32)|false|none|The id of the user to be queried|
|ClientId|integer(int32)|false|none|The client id of the service owner|
|ServiceId|integer(int32)|false|none|The id of the service making the query|
|PurposeId|integer(int32)|false|none|The purpose being queried|
|Token|string|false|none|The access token for the API|

<h2 id="tocSuserconsentresponsemodel">UserConsentResponseModel</h2>

<a id="schemauserconsentresponsemodel"></a>

```json
{
  "UserId": 0,
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "SearchId": "00000000-0000-0000-0000-000000000000",
  "Response": "string",
  "ResultsReturned": 0
}

```

*The response to a user consent query*

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|UserId|integer(int32)|false|none|The id of the queried user|
|ClientId|integer(int32)|false|none|The client id of the service owner|
|ServiceId|integer(int32)|false|none|The id of the querying service.|
|PurposeId|integer(int32)|false|none|The purpose being queried|
|SearchId|string(uuid)|false|none|The id of the search|
|Response|string|false|none|The search response.|
|ResultsReturned|integer(int32)|false|none|The number of results returned by the query|

<h2 id="tocSinverseconsentquerymodel">InverseConsentQueryModel</h2>

<a id="schemainverseconsentquerymodel"></a>

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "Token": "string"
}

```

*Model for obtaining a list of consenting users for a given purpose in a service*

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ClientId|integer(int32)|false|none|The client id of the service owner|
|ServiceId|integer(int32)|false|none|The id of the service being queried|
|PurposeId|integer(int32)|false|none|The purpose being queried|
|Token|string|false|none|The access token for the API|

<h2 id="tocSinverseconsentresponsemodel">InverseConsentResponseModel</h2>

<a id="schemainverseconsentresponsemodel"></a>

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "PurposeId": 0,
  "SearchId": "00000000-0000-0000-0000-000000000000",
  "Message": "string",
  "Response": [
    "string"
  ],
  "ResultsReturned": 0
}

```

*The response to an inverse consent query*

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ClientId|integer(int32)|false|none|The client id of the service owner|
|ServiceId|integer(int32)|false|none|The id of the querying service.|
|PurposeId|integer(int32)|false|none|The purpose being queried|
|SearchId|string(uuid)|false|none|The id of the search|
|Message|string|false|none|The response message|
|Response|[string]|false|none|The search response.|
|ResultsReturned|integer(int32)|false|none|The number of results returned by the query|

<h2 id="tocSservicesearchmodel">ServiceSearchModel</h2>

<a id="schemaservicesearchmodel"></a>

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "Token": "string",
  "Start": "2018-06-11T14:02:37Z",
  "End": "2018-06-11T14:02:37Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ClientId|integer(int32)|false|none|none|
|ServiceId|integer(int32)|false|none|none|
|Token|string|false|none|none|
|Start|string(date-time)|false|none|none|
|End|string(date-time)|false|none|none|

<h2 id="tocSconsentsearchmodel">ConsentSearchModel</h2>

<a id="schemaconsentsearchmodel"></a>

```json
{
  "ServiceOwner": "string",
  "Service": "string",
  "UserId": 0,
  "SearchTime": "2018-06-11T14:02:37Z",
  "SearchId": "string",
  "Result": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ServiceOwner|string|false|none|none|
|Service|string|false|none|none|
|UserId|integer(int32)|false|none|none|
|SearchTime|string(date-time)|false|none|none|
|SearchId|string|false|none|none|
|Result|string|false|none|none|

<h2 id="tocSusersearchmodel">UserSearchModel</h2>

<a id="schemausersearchmodel"></a>

```json
{
  "ServiceId": 0,
  "UserId": 0,
  "Token": "string",
  "Start": "2018-06-11T14:02:37Z",
  "End": "2018-06-11T14:02:37Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ServiceId|integer(int32)|false|none|none|
|UserId|integer(int32)|false|none|none|
|Token|string|false|none|none|
|Start|string(date-time)|false|none|none|
|End|string(date-time)|false|none|none|

<h2 id="tocSserviceusermodel">ServiceUserModel</h2>

<a id="schemaserviceusermodel"></a>

```json
{
  "UserId": 0,
  "Identifier": "string",
  "ServiceId": 0
}

```

*Model describing the user of a service*

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|UserId|integer(int32)|false|none|The Id of the user in consentua|
|Identifier|string|false|none|The service identifier for this user. It should be a combination of email|claim|authorisation|
|ServiceId|integer(int32)|false|none|The consentua Id of the service|

<h2 id="tocSuserconsentaddrequestmodel">UserConsentAddRequestModel</h2>

<a id="schemauserconsentaddrequestmodel"></a>

```json
{
  "Token": "string",
  "Consent": {
    "ClientId": 0,
    "ServiceId": 0,
    "UserId": 0,
    "Purposes": [
      {
        "ConsentTemplateId": 0,
        "PurposeId": 0,
        "Consent": true
      }
    ]
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|Token|string|false|none|API access token|
|Consent|[UserConsentModel](#schemauserconsentmodel)|false|none|none|

<h2 id="tocSuserconsentmodel">UserConsentModel</h2>

<a id="schemauserconsentmodel"></a>

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "UserId": 0,
  "Purposes": [
    {
      "ConsentTemplateId": 0,
      "PurposeId": 0,
      "Consent": true
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ClientId|integer(int32)|false|none|Service Id of the service requesting the consents|
|ServiceId|integer(int32)|false|none|Service Id of the service requesting the consents|
|UserId|integer(int32)|false|none|User Id of the conset holder in the service|
|Purposes|[[UserPurposeConsentModel](#schemauserpurposeconsentmodel)]|false|none|An array of purposes and the user consent to those purposes|

<h2 id="tocSuserpurposeconsentmodel">UserPurposeConsentModel</h2>

<a id="schemauserpurposeconsentmodel"></a>

```json
{
  "ConsentTemplateId": 0,
  "PurposeId": 0,
  "Consent": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ConsentTemplateId|integer(int32)|false|none|The id of the consent template which owns the purpose|
|PurposeId|integer(int32)|false|none|The Id of the purpose of the consent|
|Consent|boolean|false|none|The state of consent for the specified purpose|

<h2 id="tocSuserconsentaddresponsemodel">UserConsentAddResponseModel</h2>

<a id="schemauserconsentaddresponsemodel"></a>

```json
{
  "Success": true,
  "Message": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|Success|boolean|false|none|Flag to show the success/faliure of the request|
|Message|string|false|none|Message associated with the request|

<h2 id="tocSuserconsentaddrequestmodelex">UserConsentAddRequestModelEx</h2>

<a id="schemauserconsentaddrequestmodelex"></a>

```json
{
  "Token": "string",
  "AuthenticationData": "string",
  "Consent": {
    "ClientId": 0,
    "ServiceId": 0,
    "UserId": 0,
    "Purposes": [
      {
        "ConsentTemplateId": 0,
        "PurposeId": 0,
        "Consent": true
      }
    ]
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|Token|string|false|none|none|
|AuthenticationData|string|false|none|none|
|Consent|[UserConsentModel](#schemauserconsentmodel)|false|none|none|

<h2 id="tocSuserconsentgetrequestmodel">UserConsentGetRequestModel</h2>

<a id="schemauserconsentgetrequestmodel"></a>

```json
{
  "ClientId": 0,
  "ServiceId": 0,
  "UserId": 0,
  "Token": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ClientId|integer(int32)|false|none|Client Id of the client owning the service|
|ServiceId|integer(int32)|false|none|Service Id of the service requesting the consents|
|UserId|integer(int32)|false|none|User Id of the conset holder in the service|
|Token|string|false|none|API access token|

<h2 id="tocSuserconsentgetresponsemodel">UserConsentGetResponseModel</h2>

<a id="schemauserconsentgetresponsemodel"></a>

```json
{
  "Success": true,
  "Message": "string",
  "Consent": {
    "ClientId": 0,
    "ServiceId": 0,
    "UserId": 0,
    "Purposes": [
      {
        "ConsentTemplateId": 0,
        "PurposeId": 0,
        "Consent": true
      }
    ]
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|Success|boolean|false|none|Flag to show the success/failure of the request|
|Message|string|false|none|Message associated with the request|
|Consent|[UserConsentModel](#schemauserconsentmodel)|false|none|none|

