---
navigation:
  - yar-client.construct.md: '« Yar\_Client::\_\_construct'
  - class.yar-concurrent-client.md: Yar\_Concurrent\_Client »
  - index.md: PHP Manual
  - class.yar-client.md: Yar\_Client
title: 'Yar\_Client::setOpt'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yar\_Client::setOpt

(PECL yar >= 1.0.0)

Yar\_Client::setOpt — Задає контекст дзвінка

### Опис

```methodsynopsis
public Yar_Client::setOpt(int $name, mixed $value): Yar_Client|false
```

### Список параметрів

`name`

Параметр може набувати значення: **`YAR_OPT_PACKAGER`** **`YAR_OPT_PERSISTENT`**(необходима поддержка на сервере),**`YAR_OPT_TIMEOUT`** **`YAR_OPT_CONNECT_TIMEOUT`** **`YAR_OPT_HEADER`**(константа доступна с версии 2.0.4),**`YAR_OPT_PROXY`**(константа доступна с версии 2.0.4)

`value`

### Значення, що повертаються

Повертає $this у разі успішного завершення або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**Yar\_Client::setOpt()\*\*\*\*

```php
<?php

$cient = new Yar_Client("http://host/api/");

// Установим время ожидания на 1 секунду
$client->SetOpt(YAR_OPT_CONNECT_TIMEOUT, 1000);

// Установим упаковщик JSON
$client->SetOpt(YAR_OPT_PACKAGER, "json");

// Установим собственный заголовок
$client->SetOpt(YAR_OPT_HEADER, array("hr1: val1", "hd2: val2"));

// Установим HTTP-прокси
$client->SetOpt(YAR_OPT_PROXY, "127.0.0.1:8888");

/* Вызовем удалённый сервис */
$result = $client->some_method("parameter");
?>
```

Висновок наведеного прикладу буде схожим на:

### Дивіться також

-   [Yar\_Client::\_\_call()](yar-client.call.md) \- Виклик сервісу
