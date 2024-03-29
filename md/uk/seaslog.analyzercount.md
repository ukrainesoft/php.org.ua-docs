---
navigation:
  - seaslog.alert.md: '« SeasLog::alert'
  - seaslog.analyzerdetail.md: 'SeasLog::analyzerDetail »'
  - index.md: PHP Manual
  - class.seaslog.md: SeasLog
title: 'SeasLog::analyzerCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeasLog::analyzerCount

(PECL seaslog >=1.1.6)

SeasLog::analyzerCount — Отримує кількість журналів за рівнем, log\_path і key\_word

### Опис

```methodsynopsis
public static SeasLog::analyzerCount(string $level, string $log_path = ?, string $key_word = ?): mixed
```

\`SeasLog\` набуває значення лічильника \`grep -ai '{level}' | grep -aic '{key\_word}'\`, використовуючи системний канал і повертає до PHP (масив чи ціле число).

### Список параметрів

`level`

Рядок. Рівень журналу.

`log_path`

Рядок. Шлях до журналу.

`key_word`

Рядок. Ключове слово для пошуку у журналі.

### Значення, що повертаються

Якщо \`level\`равен SEASLOG\_ALL чи не заданий, повертаються всі рівні як масив. Якщо \`level\`равен SEASLOG\_INFO або інший рівень повертається кількість як ціле число.

### Приклади

**Приклад #1 Приклад використання** SeasLog::analyzerCount()\*\*\*\*

```php
<?php

$countResult1 = SeasLog::analyzerCount();

//с `level`
$countResult2 = SeasLog::analyzerCount(SEASLOG_DEBUG);

//с `level` и `log_path`
$countResult3 = SeasLog::analyzerCount(SEASLOG_ERROR,date('Ymd',time()));

//с `level` и `key_word`
$countResult4 = SeasLog::analyzerCount(SEASLOG_DEBUG,NULL,'accessToken');

var_dump($countResult1,$countResult2,$countResult3,$countResult4);

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(8) {
  ["DEBUG"]=>
  int(180)
  ["INFO"]=>
  int(214)
  ["NOTICE"]=>
  int(0)
  ["WARNING"]=>
  int(0)
  ["ERROR"]=>
  int(228)
  ["CRITICAL"]=>
  int(244)
  ["ALERT"]=>
  int(1)
  ["EMERGENCY"]=>
  int(0)
}

int(180)

int(228)

int(29)
```

### Дивіться також

-   [SeasLog::analyzerDetail()](seaslog.analyzerdetail.md) \- Отримує деталізацію журналу за рівнем, log\_path, key\_word, start, limit, order
