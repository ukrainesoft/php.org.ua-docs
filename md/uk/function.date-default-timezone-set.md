Встановлює часовий пояс за промовчанням для всіх функцій дати/часу у скрипті

-   [« datedefaulttimezoneget](function.date-default-timezone-get.html)
    
-   [datediff »](function.date-diff.html)
    
-   [PHP Manual](index.html)
    
-   [Функции даты и времени](ref.datetime.html)
    
-   Встановлює часовий пояс за промовчанням для всіх функцій дати/часу у скрипті
    

# datedefaulttimezoneset

(PHP 5> = 5.1.0, PHP 7, PHP 8)

datedefaulttimezoneset — Встановлює часовий пояс за промовчанням для всіх функцій дати/часу у скрипті

### Опис

```methodsynopsis
date_default_timezone_set(string $timezoneId): bool
```

**datedefaulttimezoneset()** встановлює часовий пояс за промовчанням для всіх функцій дати/часу у скрипті.

Замість використання цієї функції, ви можете скористатися INI-налаштуванням [date.timezone](datetime.configuration.html#ini.date.timezone) для встановлення часового поясу за промовчанням.

### Список параметрів

`timezoneId`

Ідентифікатор часового поясу, наприклад, `UTC` `Africa/Lagos` `Asia/Hong_Kong` або `Europe/Lisbon`. Список допустимих ідентифікаторів часових поясів можна знайти у розділі [Список підтримуваних часових поясів](timezones.html)

### Значення, що повертаються

Функція повертає **`false`**, якщо `timezoneId` має неправильне значення, в інших випадках **`true`**

### Приклади

**Приклад #1 Отримання часового поясу за замовчуванням**

```php
<?php
date_default_timezone_set('America/Los_Angeles');

$script_tz = date_default_timezone_get();

if (strcmp($script_tz, ini_get('date.timezone'))){
    echo 'Часовой пояс скрипта отличается от заданного в INI-файле.';
} else {
    echo 'Часовой пояс скрипта и настройки INI-файла совпадают.';
}
?>
```

### Дивіться також

-   [datedefaulttimezoneget()](function.date-default-timezone-get.html) - Повертає часовий пояс, який використовується за умовчанням всіма функціями дати/часу в скрипті
-   [Список підтримуваних часових поясів](timezones.html)