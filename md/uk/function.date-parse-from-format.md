- [« date_offset_get](function.date-offset-get.md)
- [date_parse »](function.date-parse.md)

- [PHP Manual](index.md)
- [Функції дати та часу](ref.datetime.md)
- Отримання інформації про задану у визначеному форматі дату

# date_parse_from_format

(PHP 5 \>= 5.3.0, PHP 7, PHP 8)

date_parse_from_format — Отримання інформації про задану в певному
форматі дати

### Опис

**date_parse_from_format**(string `$format`, string `$datetime`): array

Повертає асоціативний масив з детальною інформацією про задану
дати/часу.

### Список параметрів

`format`
Формат, що розпізнається функцією
[DateTime::createFromFormat()](datetime.createfromformat.md).

`datetime`
Рядок, що представляє дату/час.

### Значення, що повертаються

Повертає асоціативний масив з детальною інформацією про задану
дати/часу.

### Список змін

| Версія | Опис                                                                                                                                      |
| ------ | ----------------------------------------------------------------------------------------------------------------------------------------- |
| 7.2.0  | Елемент zone масиву, що повертається, відображає тепер секунди замість хвилин, а його знак інвертується. Наприклад, -120 тепер буде 7200. |

### Приклади

**Приклад #1 Приклад використання **date_parse_from_format()****

` <?php$date = "6.1.2009 13:00+01:00";print_r(date_parse_from_format("j.n.Y H:iP", $date));?> `

Результат виконання цього прикладу:

Array
(
[year] => 2009
[month] => 1
[day] => 6
[hour] => 13
[minute] => 0
[second] => 0
[fraction] =>
[warning_count] => 0
[warnings] => Array
(
)

[error_count] => 0
[errors] => Array
(
)

[is_localtime] => 1
[zone_type] => 1
[zone] => -60
[is_dst] =>
)

### Дивіться також

- [DateTime::createFromFormat()](datetime.createfromformat.md) -
Розбирає рядок з датою згідно з вказаним форматом
- [checkdate()](function.checkdate.md) - Перевіряє правильність дати
за григоріанським календарем
