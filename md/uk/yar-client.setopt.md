---
navigation:
  - yar-client.construct.md: '« YarClient::construct'
  - class.yar-concurrent-client.md: YarConcurrentClient »
  - index.md: PHP Manual
  - class.yar-client.md: YarClient
title: 'YarClient::setOpt'
---
# YarClient::setOpt

(PECL yar >= 1.0.0)

YarClient::setOpt — Задати контекст дзвінка

### Опис

```methodsynopsis
public Yar_Client::setOpt(int $name, mixed $value): Yar_Client|false
```

### Список параметрів

`name`

Може приймати значення: YAROPTPACKAGER, YAROPTPERSISTENT (необхідна підтримка на сервері), YAROPTTIMEOUT, YAROPTCONNECTTIMEOUT, YAROPTHEADER (Доступно з версії 2.0.4)

`value`

### Значення, що повертаються

Повертає $this у разі успішного завершення або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **YarClient::setOpt()****

```php
<?php

$cient = new Yar_Client("http://host/api/");

//Установим время ожидания на 1 секунду
$client->SetOpt(YAR_OPT_CONNECT_TIMEOUT, 1000);

//Установим упаковщик JSON
$client->SetOpt(YAR_OPT_PACKAGER, "json");

//Установим собственный заголовок
$client->SetOpt(YAR_OPT_HEADER, array("hr1: val1", "hd2: val2"));

/* вызовем удалённый сервис */
$result = $client->some_method("parameter");
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [YarClient::call()](yar-client.call.md) - Виклик сервісу
