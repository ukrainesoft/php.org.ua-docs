Отримує змінну запиту SeasLog

-   [« SeasLog::getRequestID](seaslog.getrequestid.md)
    
-   [SeasLog::info »](seaslog.info.md)
    
-   [PHP Manual](index.md)
    
-   [SeasLog](class.seaslog.md)
    
-   Отримує змінну запиту SeasLog
    

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

-   [SEASLOGREQUESTVARIABLEDOMAINPORT](seaslog.constants.html#constant.seaslog-request-variable-domain-port)
-   [SEASLOGREQUESTVARIABLEREQUESTURI](seaslog.constants.html#constant.seaslog-request-variable-request-uri)
-   [SEASLOGREQUESTVARIABLEREQUESTMETHOD](seaslog.constants.html#constant.seaslog-request-variable-request-method)
-   [SEASLOGREQUESTVARIABLECLIENTІП](seaslog.constants.html#constant.seaslog-request-variable-client-ip)

### Значення, що повертаються

Повертає значення змінної запиту у разі успішного виконання.

### Приклади

**Приклад #1 Приклад використання **SeasLog::getRequestVariable()****

```php
<?php

$sDomainPort = 'domain:port';
$sRequestUri = 'uri';
$sRequestMethod = 'method';
$sClientIp = 'client_ip';

$iErrorKey = 1000;

$oSeasLog = new SeasLog();

var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT, $sDomainPort));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_URI, $sRequestUri));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD, $sRequestMethod));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_CLIENT_IP, $sClientIp));

var_dump($oSeasLog->setRequestVariable($iErrorKey,NULL));

var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT) == $sDomainPort);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_URI) == $sRequestUri);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD) == $sRequestMethod);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_CLIENT_IP) == $sClientIp);

var_dump($oSeasLog->getRequestVariable($iErrorKey));

?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [SeasLog::setRequestVariable()](seaslog.setrequestvariable.md) - Встановлює змінну запиту SeasLog вручну