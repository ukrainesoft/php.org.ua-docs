Отримує деталізацію журналу за рівнем, logpath, keyword, start, limit, order

-   [« SeasLog::analyzerCount](seaslog.analyzercount.html)
    
-   [SeasLog::closeLoggerStream »](seaslog.closeloggerstream.html)
    
-   [PHP Manual](index.html)
    
-   [SeasLog](class.seaslog.html)
    
-   Отримує деталізацію журналу за рівнем, logpath, keyword, start, limit, order
    

# SeasLog::analyzerDetail

(PECL seaslog >=1.1.6)

SeasLog::analyzerDetail — Отримує деталізацію журналу за рівнем, logpath, keyword, start, limit, order

### Опис

```methodsynopsis
public static SeasLog::analyzerDetail(    string $level,    string $log_path = ?,    string $key_word = ?,    int $start = ?,    int $limit = ?,    int $order = ?): mixed
```

SeasLog отримує результат виконання команди grep -ai '{level}' | grep -ai '{keyword}' | sed -n '{start},{limit}'p, використовує системний канал і повертає масив у PHP

### Список параметрів

`level`

Рядок. Рівень інформації в журналі.

`log_path`

Рядок. Шлях до журналу інформації.

`key_word`

Рядок. Ключове слово для пошуку журналу інформації.

`start`

Ціле число. За замовчуванням

`limit`

Ціле число. За замовчуванням

`order`

Ціле число. За замовчуванням [SEASLOGDETAILORDERASC](seaslog.constants.html#constant.seaslog-detail-order-asc). Дивіться також:

-   [SEASLOGDETAILORDERASC](seaslog.constants.html#constant.seaslog-detail-order-asc)
-   [SEASLOGDETAILORDERDESC](seaslog.constants.html#constant.seaslog-detail-order-desc)

### Значення, що повертаються

Повертає результати як масиву.

> **Зауваження**
> 
> Якщо start, limit не дорівнює NULL, у Windows SeasLog викине виняток із повідомленням: "Param start and limit don't support Windows" (Параметри start і limit не підтримуються у Windows).

### Приклади

**Приклад #1 Приклад використання **SeasLog::analyzerDetail()****

```php
<?php

$result1 = SeasLog::analyzerDetail(SEASLOG_ERROR);

//с `logger` и `key_word`
$result2 = SeasLog::analyzerDetail(SEASLOG_ERROR,'test/logger/','neeke');

//с `start` и `limit`
$result3 = SeasLog::analyzerDetail(SEASLOG_ERROR,'test/logger/','neeke',1,2);

var_dump($result1,$result2,$result3);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(20) {
  [0]=>
  string(93) "2018-07-09 12:52:53 | ERROR | 12247 | 5b42ea2580e51 | 1531111973.528 | log message from neeke"
  [1]=>
  string(93) "2018-07-09 12:52:54 | ERROR | 12256 | 5b42ea26d6657 | 1531111974.878 | log message from neeke"
  [2]=>
  string(93) "2018-07-09 12:52:55 | ERROR | 12265 | 5b42ea277b8d4 | 1531111975.506 | log message from neeke"
  [3]=>
  string(104) "2018-07-09 12:52:55 | ERROR | 12274 | 5b42ea27db5dc | 1531111975.898 | log message from the other people"
...
}

array(3) {
  [0]=>
  string(93) "2018-07-09 12:52:53 | ERROR | 12247 | 5b42ea2580e51 | 1531111973.528 | log message from neeke"
  [1]=>
  string(93) "2018-07-09 12:52:54 | ERROR | 12256 | 5b42ea26d6657 | 1531111974.878 | log message from neeke"
  [2]=>
  string(93) "2018-07-09 12:52:55 | ERROR | 12265 | 5b42ea277b8d4 | 1531111975.506 | log message from neeke"
}

array(2) {
  [0]=>
  string(93) "2018-07-09 12:52:53 | ERROR | 12247 | 5b42ea2580e51 | 1531111973.528 | log message from neeke"
  [1]=>
  string(93) "2018-07-09 12:52:54 | ERROR | 12256 | 5b42ea26d6657 | 1531111974.878 | log message from neeke"
}
```

### Дивіться також

-   [SeasLog::analyzerCount()](seaslog.analyzercount.html) - Отримує кількість журналів за рівнем, logpath і keyслово