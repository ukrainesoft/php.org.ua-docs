---
navigation:
  - soapclient.getcookies.md: '« SoapClient::\_\_getCookies'
  - soapclient.getlastrequest.md: 'SoapClient::\_\_getLastRequest »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::\_\_getFunctions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapClient::\_\_getFunctions

(PHP 5, PHP 7, PHP 8)

SoapClient::\_\_getFunctions — Повертає список доступних SOAP-функцій

### Опис

```methodsynopsis
public SoapClient::__getFunctions(): ?array
```

Повертає масив функцій, описаних у WSDL для веб-служби.

> **Зауваження** :
> 
> Ця функція працює лише у режимі WSDL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) прототипів функцій SOAP c описом типу значення, що повертається, імені функції та типів параметрів.

### Приклади

**Пример #1 Пример использования**SoapClient::\_\_getFunctions()\*\*\*\*

```php
<?php
$client = new SoapClient('http://soap.amazon.com/schemas3/AmazonWebServices.wsdl');
var_dump($client->__getFunctions());
?>
```

Результат виконання наведеного прикладу:

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

-   [SoapClient::\_\_construct()](soapclient.construct.md) \- Конструктор класу SoapClient
