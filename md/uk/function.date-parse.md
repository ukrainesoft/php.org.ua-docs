---
navigation:
  - function.date-parse-from-format.md: « date\_parse\_from\_format
  - function.date-sub.md: date\_sub »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: date\_parse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# date\_parse

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

date\_parse — Повертає асоціативний масив із детальною інформацією про задану дату/час

### Опис

```methodsynopsis
date_parse(string $datetime): array
```

Функция**date\_parse()** розбирає вказану в параметрі `datetime` рядок за тими ж правилами, що й функції [strtotime()](function.strtotime.md) і [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md). Замість повертати тимчасову мітку Unix (при використанні функції [strtotime()](function.strtotime.md)) або об'єкт [DateTimeImmutable](class.datetimeimmutable.md)(при использовании функции[DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md)), вона повертає асоціативний масив з інформацією, яку функція змогла виявити в даному рядку параметра `datetime`

Якщо інформація про певну групу елементів не знайдена, ці елементи масиву будуть встановлені у значення **`false`** або будуть відсутні. Якщо це необхідно для побудови тимчасової мітки або об'єкта [DateTimeImmutable](class.datetimeimmutable.md) з одного і того ж рядка параметра `datetime`, більша кількість полів може бути встановлена ​​в значення не **`false`**. Дивіться приклади, де це відбувається.

### Список параметрів

`datetime`

Дата/время в формате, распознаваемом функцией[DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md)

### Значення, що повертаються

Повертає масив (array), що містить інформацію про дату/час.

Масив, що повертається, містить ключі `year` `month` `day` `hour` `minute` `second` `fraction`и`is_localtime`

Якщо присутній `is_localtime`, то`zone_type` вказує тип часового поясу. Для типу (Зміщення UTC) вказується `zone`, добавляется поле`is_dst`; для типа (аббревиатура) добавляются поля`tz_abbr`и`is_dst`; для типа`3`(идентификатор часового пояса) добавляются поля`tz_abbr`и`tz_id`

Якщо у параметрі `datetime` присутні елементи відносного часу, наприклад, `+3 days`, що повертається масив включає вкладений масив з ключем `relative`. Цей масив містить ключі `year` `month` `day` `hour` `minute` `second`, і, якщо необхідно, `weekday`и`weekdays`, Залежно від переданого рядка.

Масив включає поля `warning_count`и`warnings`. Перше вказує, скільки було попереджень. Ключі елементів масиву `warnings` вказують на позицію в цьому параметрі `datetime`, Де відбулося попередження, а рядкове значення описує саме попередження.

Массив также содержит поля`error_count`и`errors`. Перше вказує, скільки помилок було знайдено. Ключі елементів масиву `errors` вказують на позицію в цьому параметрі `datetime`, де сталася помилка, а рядкове значення визначає саму помилку.

**Увага**

Кількість елементів масивів `warnings`и`errors` може бути менше, ніж `warning_count`или`error_count`якщо вони виникли в одній і тій же позиції.

### Помилки

У разі виникнення помилок форматування дати/часу, елемент масиву 'errors' міститиме повідомлення про ці помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Елемент масиву, що повертається, з ключем `zone` тепер містить секунди, а чи не хвилини. Крім того, знак інвертовано. Тобто. раніше був `-120`, а зараз `7200` |

### Приклади

**Приклад #1 Приклад использования функции**date\_parse()\*\* з повним рядком `datetime`\*\*

```php
<?php
var_dump(date_parse("2006-12-12 10:00:00.5"));
?>
```

Результат виконання наведеного прикладу:

```
array(12) {
  ["year"]=>
  int(2006)
  ["month"]=>
  int(12)
  ["day"]=>
  int(12)
  ["hour"]=>
  int(10)
  ["minute"]=>
  int(0)
  ["second"]=>
  int(0)
  ["fraction"]=>
  float(0.5)
  ["warning_count"]=>
  int(0)
  ["warnings"]=>
  array(0) {
  }
  ["error_count"]=>
  int(0)
  ["errors"]=>
  array(0) {
  }
  ["is_localtime"]=>
  bool(false)
}
```

Елементи часових поясів з'являються лише в тому випадку, якщо вони включені до заданого рядка параметра `datetime`. У цьому випадку завжди буде присутній елемент `zone_type` і ще дещо залежно від його значення.

**Приклад #2 Приклад використання** date\_parse()**с информацией об аббревиатуре часового пояса**

```php
<?php
var_dump(date_parse("June 2nd, 2022, 10:28:17 BST"));
?>
```

Результат виконання наведеного прикладу:

```
array(16) {
  ["year"]=>
  int(2022)
  ["month"]=>
  int(6)
  ["day"]=>
  int(2)
  ["hour"]=>
  int(10)
  ["minute"]=>
  int(28)
  ["second"]=>
  int(17)
  ["fraction"]=>
  float(0)
  ["warning_count"]=>
  int(0)
  ["warnings"]=>
  array(0) {
  }
  ["error_count"]=>
  int(0)
  ["errors"]=>
  array(0) {
  }
  ["is_localtime"]=>
  bool(true)
  ["zone_type"]=>
  int(2)
  ["zone"]=>
  int(0)
  ["is_dst"]=>
  bool(true)
  ["tz_abbr"]=>
  string(3) "BST"
}
```

**Приклад #3 Приклад використання** date\_parse()\*\* з інформацією про ідентифікатор часового поясу\*\*

```php
<?php
var_dump(date_parse("June 2nd, 2022, 10:28:17 Europe/London"));
?>
```

Результат виконання наведеного прикладу:

```
array(14) {
  ["year"]=>
  int(2022)
  ["month"]=>
  int(6)
  ["day"]=>
  int(2)
  ["hour"]=>
  int(10)
  ["minute"]=>
  int(28)
  ["second"]=>
  int(17)
  ["fraction"]=>
  float(0)
  ["warning_count"]=>
  int(0)
  ["warnings"]=>
  array(0) {
  }
  ["error_count"]=>
  int(0)
  ["errors"]=>
  array(0) {
  }
  ["is_localtime"]=>
  bool(true)
  ["zone_type"]=>
  int(3)
  ["tz_id"]=>
  string(13) "Europe/London"
}
```

Якщо розбирається мінімальний рядок параметра `datetime`, то інформації буде менше. У цьому прикладі всі частини часу повертаються як **`false`**

**Приклад #4 Приклад використання** date\_parse()\*\* з мінімальним рядком\*\*

```php
<?php
var_dump(date_parse("June 2nd, 2022"));
?>
```

Результат виконання наведеного прикладу:

```
array(12) {
  ["year"]=>
  int(2022)
  ["month"]=>
  int(6)
  ["day"]=>
  int(2)
  ["hour"]=>
  bool(false)
  ["minute"]=>
  bool(false)
  ["second"]=>
  bool(false)
  ["fraction"]=>
  bool(false)
  ["warning_count"]=>
  int(0)
  ["warnings"]=>
  array(0) {
  }
  ["error_count"]=>
  int(0)
  ["errors"]=>
  array(0) {
  }
  ["is_localtime"]=>
  bool(false)
}
```

Відносні формати не впливають на значення, що розбираються з абсолютних форматів, але розуміються на елементі "relative".

**Приклад #5 Приклад використання** date\_parse()\*\* з відносними форматами\*\*

```php
<?php
var_dump(date_parse("2006-12-12 10:00:00.5 +1 week +1 hour"));
?>
```

Результат виконання наведеного прикладу:

```
array(13) {
  ["year"]=>
  int(2006)
  ["month"]=>
  int(12)
  ["day"]=>
  int(12)
  ["hour"]=>
  int(10)
  ["minute"]=>
  int(0)
  ["second"]=>
  int(0)
  ["fraction"]=>
  float(0.5)
  ["warning_count"]=>
  int(0)
  ["warnings"]=>
  array(0) {
  }
  ["error_count"]=>
  int(0)
  ["errors"]=>
  array(0) {
  }
  ["is_localtime"]=>
  bool(false)
  ["relative"]=>
  array(6) {
    ["year"]=>
    int(0)
    ["month"]=>
    int(0)
    ["day"]=>
    int(7)
    ["hour"]=>
    int(1)
    ["minute"]=>
    int(0)
    ["second"]=>
    int(0)
  }
}
```

Деякі рядки, такі як `Thursday`, установят временную часть строки в значение . Якщо `Thursday` передати у функцію [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md), то це також призведе до того, що година, хвилина, секунда та дріб будуть встановлені у значення . У наведеному нижче прикладі елемент year, однак, залишений як **`false`**

**Приклад #6 Приклад використання** date\_parse()\*\* з побічними ефектами\*\*

```php
<?php
var_dump(date_parse("Thursday, June 2nd"));
?>
```

Результат виконання наведеного прикладу:

```
array(13) {
  ["year"]=>
  bool(false)
  ["month"]=>
  int(6)
  ["day"]=>
  int(2)
  ["hour"]=>
  int(0)
  ["minute"]=>
  int(0)
  ["second"]=>
  int(0)
  ["fraction"]=>
  float(0)
  ["warning_count"]=>
  int(0)
  ["warnings"]=>
  array(0) {
  }
  ["error_count"]=>
  int(0)
  ["errors"]=>
  array(0) {
  }
  ["is_localtime"]=>
  bool(false)
  ["relative"]=>
  array(7) {
    ["year"]=>
    int(0)
    ["month"]=>
    int(0)
    ["day"]=>
    int(0)
    ["hour"]=>
    int(0)
    ["minute"]=>
    int(0)
    ["second"]=>
    int(0)
    ["weekday"]=>
    int(4)
  }
}
```

### Дивіться також

-   [date\_parse\_from\_format()](function.date-parse-from-format.md) \- Отримання інформації про задану у визначеному форматі дату для розбору параметра`datetime`з певним заданим форматом
-   [checkdate()](function.checkdate.md) \- Перевіряє коректність дати за григоріанським календарем для перевірки григоріанської дати
-   [getdate()](function.getdate.md) \- Повертає інформацію про дату/час
