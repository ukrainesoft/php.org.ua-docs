- [« DateInterval::\_\_construct](dateinterval.construct.md)
- [DateInterval::format »](dateinterval.format.md)

- [PHP Manual](index.md)
- [DateInterval](class.dateinterval.md)
- Створює об'єкт класу DateInterval із дати у відносному форматі

# DateInterval::createFromDateString

(PHP 5 \>= 5.3.0, PHP 7, PHP 8)

DateInterval::createFromDateString — Створює об'єкт класу DateInterval
з дати у відносному форматі

### Опис

public static **DateInterval::createFromDateString**(string
`$datetime`): [DateInterval](class.dateinterval.md)\|false

Розбирає рядок, що містить часовий інтервал у звичайному
(здобутаному) вигляді і створює на його основі об'єкт класу DateInterval.

### Список параметрів

`datetime`
Дата, що складається з відносних часових фрагментів. Зокрема, для
створення об'єкта DateInterval з частин, записаних у [відносному форматі](datetime.formats.relative.md), який підтримується
парсером у функціях [DateTimeImmutable](class.datetimeimmutable.md),
[DateTime](class.datetime.md) та
[strtotime()](function.strtotime.md).

### Значення, що повертаються

Повертає новий об'єкт класу [DateInterval](class.dateinterval.md) у
у разі успішного виконання або **`false`** у разі виникнення
помилки.

### Список змін

| Версія | Опис                                                                                                                                              |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.2.0  | Тільки властивості from_string та date_string будуть видно при створенні об'єкта [DateInterval](class.dateinterval.md) за допомогою цього методу. |

### Приклади

**Приклад #1 Аналіз та розбір часових інтервалів**

` <?php// Інтервали в кожному прикладі еквівалентні.$i = new DateInterval('P1D');$i = DateInterval::createFromDateString('1 day');$i = new = DateInterval::createFromDateString('2 weeks');$i = new DateInterval('P3M');$i = DateInterval::createFromDateString('3 months');$i = neu DateInterval('$ = DateInterval::createFromDateString('4 years');$i = new DateInterval('P1Y1D');$i = DateInterval::createFromDateString('1 year + 1 day');$i == ;$i = DateInterval::createFromDateString('1 day + 12 hours');$i = new DateInterval('PT3600S');$i = DateInterval::createFromDateString('3600 ;

**Приклад #2 Розбір спеціальних відносних тимчасових інтервалів**

` <?php$i = DateInterval::createFromDateString('last day of next month');var_dump($i);$i = DateInterval::createFromDateString('last weekday');var_dump($i); `

Результат виконання цього прикладу в PHP 8.2:

object(DateInterval)#1 (2) {
["from_string"]=>
bool(true)
["date_string"]=>
string(22) "last day of next month"
}
object(DateInterval)#2 (2) {
["from_string"]=>
bool(true)
["date_string"]=>
string(12) "last weekday"
}

Результат виконання цього прикладу в PHP 8 аналогічний:

object(DateInterval)#1 (16) {
["y"]=>
int(0)
["m"]=>
int(1)
["d"]=>
int(0)
["h"]=>
int(0)
["i"]=>
int(0)
["s"]=>
int(0)
["f"]=>
float(0)
["weekday"]=>
int(0)
["weekday_behavior"]=>
int(0)
["first_last_day_of"]=>
int(2)
["invert"]=>
int(0)
["days"]=>
bool(false)
["special_type"]=>
int(0)
["special_amount"]=>
int(0)
["have_weekday_relative"]=>
int(0)
["have_special_relative"]=>
int(0)
}
object(DateInterval)#2 (16) {
["y"]=>
int(0)
["m"]=>
int(0)
["d"]=>
int(0)
["h"]=>
int(0)
["i"]=>
int(0)
["s"]=>
int(0)
["f"]=>
float(0)
["weekday"]=>
int(0)
["weekday_behavior"]=>
int(0)
["first_last_day_of"]=>
int(0)
["invert"]=>
int(0)
["days"]=>
bool(false)
["special_type"]=>
int(1)
["special_amount"]=>
int(-1)
["have_weekday_relative"]=>
int(0)
["have_special_relative"]=>
int(1)
}
