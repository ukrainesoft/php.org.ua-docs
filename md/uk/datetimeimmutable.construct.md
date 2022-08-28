Повертає новий об'єкт DateTimeImmutable

-   [« DateTimeImmutable::add](datetimeimmutable.add.html)
    
-   [DateTimeImmutable::createFromFormat »](datetimeimmutable.createfromformat.html)
    
-   [PHP Manual](index.html)
    
-   [DateTimeImmutable](class.datetimeimmutable.html)
    
-   Повертає новий об'єкт DateTimeImmutable
    

# DateTimeImmutable::construct

# datecreateimmutable

(PHP 5> = 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::construct - datecreateimmutable — Повертає новий об'єкт DateTimeImmutable

### Опис

Об'єктно-орієнтований стиль

public **DateTimeImmutable::construct**(string `$datetime` = "now", ?[DateTimeZone](class.datetimezone.html) `$timezone` **`null`**

Процедурний стиль

```methodsynopsis
date_create_immutable(string $datetime = "now", ?DateTimeZone $timezone = null): DateTimeImmutable|false
```

Повертає новий об'єкт DateTimeImmutable.

### Список параметрів

`datetime`

Рядок дати/часу. Пояснення коректних форматів наведено в розділі [Форматы даты и времени](datetime.formats.html)

Вкажіть `"now"` для отримання поточного часу під час використання параметра `timezone`

`timezone`

Об'єкт [DateTimeZone](class.datetimezone.html), що представляє часовий пояс параметра `datetime`

Якщо параметр `timezone` опущений або дорівнює **`null`**, використовуватиметься поточний часовий пояс.

> **Зауваження**
> 
> Параметр `timezone` та поточний часовий пояс ігноруються, якщо параметр `datetime` або є тимчасовою міткою UNIX (наприклад, `@946684800`), або вказаний часовий пояс (наприклад, `2010-01-28T15:00:00+02:00` або `2010-07-05T06:00:00Z`

### Значення, що повертаються

Повертає новий екземпляр DateTimeImmutable. Процедурний стиль повертає **`false`** у разі виникнення помилки.

### Помилки

Викидає [Exception](class.exception.html) у разі виникнення помилки.

### список змін

| Версия | Описание                                                               |
|--------|------------------------------------------------------------------------|
|        | Відтепер мікросекунди заповнюються фактичним значенням. Чи не '00000'. |

### Приклади

**Приклад #1 Приклад використання **DateTimeImmutable::construct()****

Об'єктно-орієнтований стиль

```php
<?php
try {
    $date = new DateTimeImmutable('2000-01-01');
} catch (Exception $e) {
    echo $e->getMessage();
    exit(1);
}

echo $date->format('Y-m-d');
?>
```

Процедурний стиль

```php
<?php
$date = date_create('2000-01-01');
if (!$date) {
    $e = date_get_last_errors();
    foreach ($e['errors'] as $error) {
        echo "$error\n";
    }
    exit(1);
}

echo date_format($date, 'Y-m-d');
?>
```

Результат виконання даних прикладів:

```
2000-01-01
```

**Приклад #2 Тонкощі **DateTimeImmutable::construct()****

```php
<?php
// Указанная дата/время в часовом поясе вашего компьютера.
$date = new DateTimeImmutable('2000-01-01');
echo $date->format('Y-m-d H:i:sP') . "\n";

// Указанная дата/время в указанном часовом поясе.
$date = new DateTimeImmutable('2000-01-01', new DateTimeZone('Pacific/Nauru'));
echo $date->format('Y-m-d H:i:sP') . "\n";

// Текущая дата/время в часовом поясе вашего компьютера.
$date = new DateTimeImmutable();
echo $date->format('Y-m-d H:i:sP') . "\n";

// Текущая дата/время в указанном часовом поясе.
$date = new DateTimeImmutable(null, new DateTimeZone('Pacific/Nauru'));
echo $date->format('Y-m-d H:i:sP') . "\n";

// Использование временной метки UNIX. Обратите внимание, что результат в часовом поясе UTC.
$date = new DateTimeImmutable('@946684800');
echo $date->format('Y-m-d H:i:sP') . "\n";

// Несуществующие значения переворачиваются.
$date = new DateTimeImmutable('2000-02-30');
echo $date->format('Y-m-d H:i:sP') . "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
2000-01-01 00:00:00-05:00
2000-01-01 00:00:00+12:00
2010-04-24 10:24:16-04:00
2010-04-25 02:24:16+12:00
2000-01-01 00:00:00+00:00
2000-03-01 00:00:00-05:00
```

**Приклад #3 Зміна пов'язаного часового поясу**

```php
<?php
$timeZone = new \DateTimeZone('Asia/Tokyo');

$time = new \DateTimeImmutable();
$time = $time->setTimezone($timeZone);

echo $time->format('Y/m/d H:i:s'), "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
2022/08/12 23:49:23
```

**Приклад #4 Використання відносного рядка дати/часу**

```php
<?php
$time = new \DateTimeImmutable("-1 year");

echo $time->format('Y/m/d H:i:s'), "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
2021/08/12 15:43:51
```