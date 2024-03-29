---
navigation:
  - seaslog.constants.md: « Зумовлені константи
  - ref.seaslog.md: Функції Seaslog »
  - index.md: PHP Manual
  - book.seaslog.md: Seaslog
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Приклади

**Приклад #1 Отримує та встановлює базовий шлях**

```php
<?php
  $basePath1 = SeasLog::getBasePath();

  SeasLog::setBasePath('/log/base_test');
  $basePath2 = SeasLog::getBasePath();

  var_dump($basePath1,$basePath2);

  ?>
```

Висновок наведеного прикладу буде схожим на:

```
string(12) "/var/log/www"
  string(14) "/log/base_test"
```

**Приклад #2 Отримує та встановлює логування**

```php
<?php
$lastLogger1 = SeasLog::getLastLogger();

SeasLog::setLogger('testModule/app1');
$lastLogger2 = SeasLog::getLastLogger();

var_dump($lastLogger1,$lastLogger2);

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(7) "default"
string(15) "testModule/app1"
```

**Приклад #3 Журнал швидкого запису**

```php
<?php
SeasLog::log(SEASLOG_ERROR,'тестовая ошибка, сделанная ::log');
SeasLog::debug('отладка {userName}',array('{userName}' => 'neeke'));
SeasLog::info('запись информационного сообщения в журнал');
SeasLog::notice('запись предупреждения в журнал');
SeasLog::warning('сайт {website} не работает, пожалуйста, выполните {action} как можно скорее!',array('{website}' => 'github.com','{action}' => 'rboot'));
SeasLog::error('запись ошибки в журнал');
SeasLog::critical('произошло что-то критичное');
SeasLog::alert('да, это сообщение {messageName}',array('{messageName}' => 'alertMSG'));
SeasLog::emergency('Только что полностью выгорел соседний дом! {note}',array('{note}' => 'Это шутка'));
?>
```

Шаблон по умолчанию:*seaslog.default\_template = "%T | %L | %P | %Q | %t | %M"*. Це означає, що за замовчуванням стиль запису журналу： \`{dateTime} | {level} | {pid} | {uniqid} | {timeStamp} | {logInfo}\`

Висновок наведеного прикладу буде схожим на:

*seaslog.appender = 1*

```
2014-07-27 08:53:52 | ERROR | 23625 | 599159975a9ff | 1406422432.786 | тестовая ошибка, сделанная log
2014-07-27 08:53:52 | DEBUG | 23625 | 599159975a9ff | 1406422432.786 | отладка neeke
2014-07-27 08:53:52 | INFO | 23625 | 599159975a9ff | 1406422432.787 | запись информационного сообщения в журнал
2014-07-27 08:53:52 | NOTICE | 23625 | 599159975a9ff | 1406422432.787 | запись предупреждения в журнал
2014-07-27 08:53:52 | WARNING | 23625 | 599159975a9ff | 1406422432.787 | сайт github.com не работает, пожалуйста, выполните rboot как можно скорее!
2014-07-27 08:53:52 | ERROR | 23625 | 599159975a9ff | 1406422432.787 | запись ошибки в журнал
2014-07-27 08:53:52 | CRITICAL | 23625 | 599159975a9ff | 1406422432.787 | произошло что-то критичное
2014-07-27 08:53:52 | EMERGENCY | 23625 | 599159975a9ff | 1406422432.787 | Только что полностью выгорел соседний дом! Это шутка
```

Висновок наведеного прикладу буде схожим на:

*seaslog.appender = 2*или*seaslog.appender = 3*

```
The log style finally formatted such as:
<15>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | DEBUG | 21423 | 599157af4e937 | 1466787583.322 | отладка neeke
<14>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | INFO | 21423 | 599157af4e937 | 1466787583.323 | запись информационного сообщения в журнал
<13>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | NOTICE | 21423 | 599157af4e937 | 1466787583.324 | запись предупреждения в журнал
```

**Приклад #4 Швидкий підрахунок певного типу значення підрахунку журналу**

*SeasLog* набуває значення лічильника \`grep -wc\`, використовує системний канал і повертає до PHP (масив чи ціле число).

```php
<?php
$countResult1 = SeasLog::analyzerCount();
$countResult2 = SeasLog::analyzerCount(SEASLOG_WARNING);
$countResult3 = SeasLog::analyzerCount(SEASLOG_ERROR,date('Ymd',time()));

var_dump($countResult1,$countResult2,$countResult3);

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(8) {
  ["DEBUG"]=>
  int(3)
  ["INFO"]=>
  int(3)
  ["NOTICE"]=>
  int(3)
  ["WARNING"]=>
  int(3)
  ["ERROR"]=>
  int(6)
  ["CRITICAL"]=>
  int(3)
  ["ALERT"]=>
  int(3)
  ["EMERGENCY"]=>
  int(3)
}
int(7)
int(1)
```

**Приклад #5 Отримує певний тип списку журналів**

*SeasLog* набуває значення лічильника \`grep -w\`, використовує системний канал і повертає масив у PHP

```php
<?php
$detailErrorArray = SeasLog::analyzerDetail(SEASLOG_ERROR);
var_dump($detailErrorArray);

var_dump(SeasLog::analyzerDetail(SEASLOG_ERROR,date('Ymd',time())));
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(6) {
  [0] =>
  string(83) "2014-02-24 00:14:02 | ERROR | 8568 | 599157af4e937 | 1393172042.717 | test error 3 "
  [1] =>
  string(83) "2014-02-24 00:14:04 | ERROR | 8594 | 5991576584446 | 1393172044.104 | test error 3 "
  [2] =>
  string(83) "2014-02-24 00:14:04 | ERROR | 8620 | 1502697015147 | 1393172044.862 | test error 3 "
  [3] =>
  string(83) "2014-02-24 00:14:05 | ERROR | 8646 | 599159975a9ff | 1393172045.989 | test error 3 "
  [4] =>
  string(83) "2014-02-24 00:14:07 | ERROR | 8672 | 599159986ec28 | 1393172047.882 | test error 3 "
  [5] =>
  string(83) "2014-02-24 00:14:08 | ERROR | 8698 | 5991599981cec | 1393172048.736 | test error 3 "
}

array(2) {
  [0] =>
  string(83) "2014-02-24 00:14:02 | ERROR | 8568 | 599157af4e937 | 1393172042.717 | test error 3 "
  [1] =>
  string(83) "2014-02-24 00:14:04 | ERROR | 8594 | 5991576584446 | 1393172044.104 | test error 3 "
}
```
