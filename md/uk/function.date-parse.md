- [« date_parse_from_format](function.date-parse-from-format.md)
- [date_sub »](function.date-sub.md)

- [PHP Manual](index.md)
- [Функції дати та часу](ref.datetime.md)
- Повертає асоціативний масив із детальною інформацією про задану
дати/часу

#date_parse

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

date_parse — Повертає асоціативний масив з детальною інформацією про
заданої дати/часу

### Опис

**date_parse**(string `$datetime`): array

Функція **date_parse()** розбирає вказану у параметрі `datetime`
рядок за тими ж правилами, що й функції
[strtotime()](function.strtotime.md) та
[DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md).
Замість того, щоб повертати тимчасову мітку Unix (при використанні
функції [strtotime()](function.strtotime.md)) або об'єкт
[DateTimeImmutable](class.datetimeimmutable.md) (при використанні
функції
[DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md)),
вона повертає асоціативний масив із інформацією, яку функція
спромоглася виявити в даному рядку параметра `datetime`.

Якщо інформацію про певну групу елементів не знайдено, ці
елементи масиву будуть встановлені у значення **`false`** або будуть
відсутня. Якщо це необхідно для побудови тимчасової мітки або
об'єкта [DateTimeImmutable](class.datetimeimmutable.md) з однієї і тієї
ж рядки параметра `datetime`, більша кількість полів може бути
встановлено значення не **`false`**. Дивіться приклади, у яких це
відбувається.

### Список параметрів

`datetime`
Дата/час у форматі, що розпізнається функцією
[DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md).

### Значення, що повертаються

Повертає масив (array), що містить інформацію про дату/час у разі
успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

У разі виникнення помилок форматування дати/часу, елемент
масив 'errors' міститиме повідомлення про ці помилки.

### Список змін

| Версія | Опис                                                                                                                                 |
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0  | Елемент масива з ключем zone тепер містить секунди, а не хвилини. Крім того, знак інвертовано. Тобто. раніше був -120, а тепер 7200. |

### Приклади

**Приклад #1 Приклад використання функції **date_parse()** з повною
рядком `datetime`**

` <?phpvar_dump(date_parse("2006-12-12 10:00:00.5"));?> `

Результат виконання цього прикладу:

array(12) {
'year' => int(2006)
'month' => int(12)
'day' => int(12)
'hour' => int(10)
'minute' => int(0)
'second' => int(0)
'fraction' => double(0.5)
'warning_count' => int(0)
'warnings' => array(0) {
}
'error_count' => int(0)
'errors' => array(0) {
}
'is_localtime' => bool(false)
}

Елементи часових поясів з'являються лише в тому випадку, якщо вони
включені в заданий рядок параметра 'datetime'. В цьому випадку завжди
буде присутній елемент `zone_type` і ще трохи залежно
від його значення.

**Приклад #2 Приклад використання **date_parse()** з інформацією про
абревіатурі часового поясу**

` <?phpvar_dump(date_parse("June 2nd, 2022, 10:28:17 BST"));?> `

Результат виконання цього прикладу:

array(16) {
'year' => int(2022)
'month' => int(6)
'day' => int(2)
'hour' => int(10)
'minute' => int(28)
'second' => int(17)
'fraction' => double(0)
'warning_count' => int(0)
'warnings' => array(0) {
}
'error_count' => int(0)
'errors' => array(0) {
}
'is_localtime' => bool(true)
'zone_type' => int(2)
'zone' => int(0)
'is_dst' => bool(true)
'tz_abbr' => string(3) "BST"
}

**Приклад #3 Приклад використання **date_parse()** з інформацією про
ідентифікатор часового поясу**

` <?phpvar_dump(date_parse("June 2nd, 2022, 10:28:17 Europe/London"));?> `

Результат виконання цього прикладу:

array(14) {
'year' => int(2022)
'month' => int(6)
'day' => int(2)
'hour' => int(10)
'minute' => int(28)
'second' => int(17)
'fraction' => double(0)
'warning_count' => int(0)
'warnings' => array(0) {
}
'error_count' => int(0)
'errors' => array(0) {
}
'is_localtime' => bool(true)
'zone_type' => int(3)
'tz_id' => string(13) "Europe/London"
}

Якщо розбирається мінімальний рядок параметра `datetime`, то
інформації буде менше. У цьому прикладі всі частини часу повертаються
як **`false`**.

**Приклад #4 Приклад використання **date_parse()** з мінімальною
рядком**

` <?phpvar_dump(date_parse("June 2nd, 2022"));?> `

Результат виконання цього прикладу:

array(12) {
'year' => int(2022)
'month' => int(6)
'day' => int(2)
'hour' => bool(false)
'minute' => bool(false)
'second' => bool(false)
'fraction' => bool(false)
'warning_count' => int(0)
'warnings' => array(0) {
}
'error_count' => int(0)
'errors' => array(0) {
}
'is_localtime' => bool(false)
}

[Відносні формати](datetime.formats.relative.md) не впливають на
значення, що розбираються з абсолютних форматів, але розбираються в елемент
"relative".

**Приклад #5 Приклад використання **date_parse()** з відносними
форматами**

` <?phpvar_dump(date_parse("2006-12-12 10:00:00.5 +1 week +1 hour"));?> `

Результат виконання цього прикладу:

array(13) {
'year' => int(2006)
'month' => int(12)
'day' => int(12)
'hour' => int(10)
'minute' => int(0)
'second' => int(0)
'fraction' => double(0.5)
'warning_count' => int(0)
'warnings' => array(0) {
}
'error_count' => int(0)
'errors' => array(0) {
}
'is_localtime' => bool(false)
'relative' =>
array(6) {
'year' => int(0)
'month' => int(0)
'day' => int(7)
'hour' => int(1)
'minute' => int(0)
'second' => int(0)
}
}

Деякі рядки, такі як Thursday, встановлять тимчасову частину рядка
значення "0". Якщо `Thursday` передати у функцію
[DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md),
то це також призведе до того, що година, хвилина, секунда та дріб будуть
встановлені у значення `0`. У наведеному нижче прикладі елемент year,
однак залишений як **`false`**.

**Приклад #6 Приклад використання **date_parse()** з побічними
ефектами**

` <?phpvar_dump(date_parse("Thursday, June 2nd"));?> `

Результат виконання цього прикладу:

array(13) {
'year' => bool(false)
'month' => int(6)
'day' => int(2)
'hour' => int(0)
'minute' => int(0)
'second' => int(0)
'fraction' => double(0)
'warning_count' => int(0)
'warnings' => array(0) {
}
'error_count' => int(0)
'errors' => array(0) {
}
'is_localtime' => bool(false)
'relative' =>
array(7) {
'year' => int(0)
'month' => int(0)
'day' => int(0)
'hour' => int(0)
'minute' => int(0)
'second' => int(0)
'weekday' => int(4)
}
}

### Дивіться також

- [date_parse_from_format()](function.date-parse-from-format.md) -
Отримання інформації про задану у визначеному форматі дату для
аналізу параметра `datetime` з певним заданим форматом
- [checkdate()](function.checkdate.md) - Перевіряє правильність дати
за григоріанським календарем
- [getdate()](function.getdate.md) - Повертає інформацію про
дати/часу
