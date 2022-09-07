---
navigation:
  - soapclient.getcookies.md: '« SoapClient::getCookies'
  - soapclient.getlastrequest.md: 'SoapClient::getLastRequest »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::getFunctions'
---
# SoapClient::getFunctions

(PHP 5, PHP 7, PHP 8)

SoapClient::getFunctions — Повертає список доступних SOAP-функцій

### Опис

```methodsynopsis
public SoapClient::__getFunctions(): ?array
```

Повертає масив функцій, описаних у WSDL для веб-служби.

> **Зауваження**
> 
> Ця функція працює лише у режимі WSDL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) прототипів функцій SOAP c описом типу значення, що повертається, імені функції та типів параметрів.

### Приклади

**Приклад #1 Приклад використання **SoapClient::getFunctions()****

```php
<?php
$client = new SoapClient('http://soap.amazon.com/schemas3/AmazonWebServices.wsdl');
var_dump($client->__getFunctions());
?>
```

Результат виконання цього прикладу:

```
array(26) {
  [0]=>
  string(70) "ProductInfo KeywordSearchRequest(KeywordRequest $KeywordSearchRequest)"
  [1]=>
  string(79) "ProductInfo TextStreamSearchRequest(TextStreamRequest $TextStreamSearchRequest)"
  [2]=>
  string(64) "ProductInfo PowerSearchRequest(PowerRequest $PowerSearchRequest)"
...
  [23]=>
  string(107) "ShoppingCart RemoveShoppingCartItemsRequest(RemoveShoppingCartItemsRequest $RemoveShoppingCartItemsRequest)"
  [24]=>
  string(107) "ShoppingCart ModifyShoppingCartItemsRequest(ModifyShoppingCartItemsRequest $ModifyShoppingCartItemsRequest)"
  [25]=>
  string(118) "GetTransactionDetailsResponse GetTransactionDetailsRequest(GetTransactionDetailsRequest $GetTransactionDetailsRequest)"
}
```

### Дивіться також

-   [SoapClient::construct()](soapclient.construct.md) - Конструктор класу SoapClient
