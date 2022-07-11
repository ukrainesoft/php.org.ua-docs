- [« SeasLog::alert](seaslog.alert.md)
- [SeasLog::analyzerDetail »](seaslog.analyzerdetail.md)

- [PHP Manual](index.md)
- [SeasLog](class.seaslog.md)
- Отримує кількість журналів за рівнем, log_path та key_word

# SeasLog::analyzerCount

(PECL seaslog \>=1.1.6)

SeasLog::analyzerCount — Отримує кількість журналів за рівнем,
log_path та key_word

### Опис

public static **SeasLog::analyzerCount**(string `$level`, string
`$log_path` = ?, string `$key_word` = ?):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

\`SeasLog\` набуває значення лічильника \`grep -ai '{level}' \| grep -aic
'{key_word}'\`, використовуючи системний канал і повертає до PHP (масив або
ціле число).

### Список параметрів

`level`
Рядок. Рівень журналу.

`log_path`
Рядок. Дорога до журналу.

`key_word`
Рядок. Ключове слово для пошуку журналу.

### Значення, що повертаються

Якщо "level" дорівнює SEASLOG_ALL або не заданий, повертаються всі рівні
як масив. Якщо \'level\' дорівнює SEASLOG_INFO або інший рівень,
повертається кількість як ціле число.

### Приклади

**Приклад #1 Приклад використання **SeasLog::analyzerCount()****

`` <?php$countResult1 = SeasLog::analyzerCount();//с `level`$countResult2 = SeasLog::analyzerCount(SEASLOG_DEBUG);//с `level` і `log_path`$countResul SEASLOG_ERROR,date('Ymd',time())); countResult3,$countResult4);?> ``

Результатом виконання цього прикладу буде щось подібне:

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

### Дивіться також

- [SeasLog::analyzerDetail()](seaslog.analyzerdetail.md) - Отримує
деталізацію журналу за рівнем, log_path, key_word, start, limit,
order
