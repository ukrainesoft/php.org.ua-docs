---
navigation:
  - soapclient.getlastresponseheaders.md: '« SoapClient::getLastResponseHeaders'
  - soapclient.setcookie.md: 'SoapClient::setCookie »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::getTypes'
---
# SoapClient::getTypes

(PHP 5, PHP 7, PHP 8)

SoapClient::getTypes — Повертає список типів SOAP

### Опис

```methodsynopsis
public SoapClient::__getTypes(): ?array
```

Повертає масив типів, описаних у WSDL для веб-служби.

> **Зауваження**
> 
> Ця функція працює лише у режимі WSDL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) SOAP-типів з докладним описом всіх структур та типів.

### Приклади

**Приклад #1 Приклад використання **SoapClient::getTypes()****

```php
<?php
$client = new SoapClient('http://soap.amazon.com/schemas3/AmazonWebServices.wsdl');
var_dump($client->__getTypes());
?>
```

Результат виконання цього прикладу:

```
array(88) {
  [0]=>
  string(30) "ProductLine ProductLineArray[]"
  [1]=>
  string(85) "struct ProductLine {
 string Mode;
 string RelevanceRank;
 ProductInfo ProductInfo;
}"
  [2]=>
  string(105) "struct ProductInfo {
 string TotalResults;
 string TotalPages;
 string ListName;
 DetailsArray Details;
}"
...
  [85]=>
  string(32) "ShortSummary ShortSummaryArray[]"
  [86]=>
  string(121) "struct GetTransactionDetailsRequest {
 string tag;
 string devtag;
 string key;
 OrderIdArray OrderIds;
 string locale;
}"
  [87]=>
  string(75) "struct GetTransactionDetailsResponse {
 ShortSummaryArray ShortSummaries;
}"
}
```

### Дивіться також

-   [SoapClient::construct()](soapclient.construct.md) - Конструктор класу SoapClient
