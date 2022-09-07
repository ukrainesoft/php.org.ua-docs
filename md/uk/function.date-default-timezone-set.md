---
navigation:
  - function.date-default-timezone-get.md: « datedefaulttimezoneget
  - function.date-diff.md: datediff »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: datedefaulttimezoneset
---
# datedefaulttimezoneset

(PHP 5> = 5.1.0, PHP 7, PHP 8)

datedefaulttimezoneset — Встановлює часовий пояс за промовчанням для всіх функцій дати/часу у скрипті

### Опис

```methodsynopsis
date_default_timezone_set(string $timezoneId): bool
```

**datedefaulttimezoneset()** встановлює часовий пояс за промовчанням для всіх функцій дати/часу у скрипті.

Замість використання цієї функції, ви можете скористатися INI-налаштуванням [date.timezone](datetime.configuration.md#ini.date.timezone) для встановлення часового поясу за промовчанням.

### Список параметрів

`timezoneId`

Ідентифікатор часового поясу, наприклад, `UTC` `Africa/Lagos` `Asia/Hong_Kong` або `Europe/Lisbon`. Список допустимих ідентифікаторів часових поясів можна знайти у розділі [Список підтримуваних часових поясів](timezones.md)

### Значення, що повертаються

Функція повертає **`false`**, якщо `timezoneId` має неправильне значення, в інших випадках **`true`**

### Приклади

**Приклад #1 Отримання часового поясу за замовчуванням**

```php
<?php
date_default_timezone_set('America/Los_Angeles');

$script_tz = date_default_timezone_get();

if (strcmp($script_tz, ini_get('date.timezone'))){
    echo 'Часовой пояс скрипта отличается от заданного в INI-файле.';
} else {
    echo 'Часовой пояс скрипта и настройки INI-файла совпадают.';
}
?>
```

### Дивіться також

-   [datedefaulttimezoneget()](function.date-default-timezone-get.md) - Повертає часовий пояс, який використовується за умовчанням всіма функціями дати/часу в скрипті
-   [Список підтримуваних часових поясів](timezones.md)
