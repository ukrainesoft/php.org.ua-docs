---
navigation:
  - seaslog.getrequestid.md: '« SeasLog::getRequestID'
  - seaslog.info.md: 'SeasLog::info »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::getRequestVariable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::getRequestVariable

(PECL seaslog >=1.9.0)

SeasLog::getRequestVariable — Отримує змінну запиту SeasLog

### Опис

```methodsynopsis
public static SeasLog::getRequestVariable(int $key): bool
```

Отримує змінну запиту SeasLog.

### Список параметрів

`key`

Цілочисленна константа:

-   [SEASLOG\_REQUEST\_VARIABLE\_DOMAIN\_PORT](seaslog.constants.md#constant.seaslog-request-variable-domain-port)
-   [SEASLOG\_REQUEST\_VARIABLE\_REQUEST\_URI](seaslog.constants.md#constant.seaslog-request-variable-request-uri)
-   [SEASLOG\_REQUEST\_VARIABLE\_REQUEST\_METHOD](seaslog.constants.md#constant.seaslog-request-variable-request-method)
-   [SEASLOG\_REQUEST\_VARIABLE\_CLIENT\_IP](seaslog.constants.md#constant.seaslog-request-variable-client-ip)

### Значення, що повертаються

Повертає значення змінної запиту у разі успішного виконання.

### Приклади

**Пример #1 Пример использования**SeasLog::getRequestVariable()\*\*\*\*

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

-   [SeasLog::setRequestVariable()](seaslog.setrequestvariable.md) \- Встановлює змінну запиту SeasLog вручну
