---
navigation:
  - seaslog.setrequestid.md: '« SeasLog::setRequestID'
  - seaslog.warning.md: 'SeasLog::warning »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::setRequestVariable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::setRequestVariable

(PECL seaslog >=1.9.0)

SeasLog::setRequestVariable — Встановлює змінну запиту SeasLog вручну

### Опис

```methodsynopsis
public static SeasLog::setRequestVariable(int $key, string $value): bool
```

Встановлює змінну запиту SeasLog вручну.

### Список параметрів

`key`

Константа, ціле число.

-   [SEASLOG\_REQUEST\_VARIABLE\_DOMAIN\_PORT](seaslog.constants.md#constant.seaslog-request-variable-domain-port)
-   [SEASLOG\_REQUEST\_VARIABLE\_REQUEST\_URI](seaslog.constants.md#constant.seaslog-request-variable-request-uri)
-   [SEASLOG\_REQUEST\_VARIABLE\_REQUEST\_METHOD](seaslog.constants.md#constant.seaslog-request-variable-request-method)
-   [SEASLOG\_REQUEST\_VARIABLE\_CLIENT\_IP](seaslog.constants.md#constant.seaslog-request-variable-client-ip)

`value`

Значення змінної запиту.

### Значення, що повертаються

Повертає TRUE у разі успішного виконання, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** SeasLog::setRequestVariable()\*\*\*\*

```php
<?php

$sDomainPort = 'domain:port';
$sRequestUri = 'uri';
$sRequestMethod = 'method';
$sClientIp = 'client_ip';

$iErrorKey = 1000;

$oSeasLog = new SeasLog();

var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT, $sDomainPort));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_URI, $sRequestUri));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD, $sRequestMethod));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_CLIENT_IP, $sClientIp));

var_dump($oSeasLog->setRequestVariable($iErrorKey,NULL));

var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT) == $sDomainPort);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_URI) == $sRequestUri);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD) == $sRequestMethod);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_CLIENT_IP) == $sClientIp);

var_dump($oSeasLog->getRequestVariable($iErrorKey));

?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
bool(true)
bool(true)
bool(false)
bool(true)
bool(true)
bool(true)
bool(true)
bool(false)
```

### Дивіться також

-   [SeasLog::getRequestVariable()](seaslog.getrequestvariable.md) \- Отримує змінну запиту SeasLog
