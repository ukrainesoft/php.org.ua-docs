Встановлює змінну запиту SeasLog вручну

-   [« SeasLog::setRequestID](seaslog.setrequestid.html)
    
-   [SeasLog::warning »](seaslog.warning.html)
    
-   [PHP Manual](index.html)
    
-   [SeasLog](class.seaslog.html)
    
-   Встановлює змінну запиту SeasLog вручну
    

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

-   [SEASLOGREQUESTVARIABLEDOMAINPORT](seaslog.constants.html#constant.seaslog-request-variable-domain-port)
-   [SEASLOGREQUESTVARIABLEREQUESTURI](seaslog.constants.html#constant.seaslog-request-variable-request-uri)
-   [SEASLOGREQUESTVARIABLEREQUESTMETHOD](seaslog.constants.html#constant.seaslog-request-variable-request-method)
-   [SEASLOGREQUESTVARIABLECLIENTІП](seaslog.constants.html#constant.seaslog-request-variable-client-ip)

`value`

Значення змінної запиту.

### Значення, що повертаються

Повертає TRUE у разі успішного виконання, FALSE у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SeasLog::setRequestVariable()****

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

-   [SeasLog::getRequestVariable()](seaslog.getrequestvariable.html) - Отримує змінну запиту SeasLog