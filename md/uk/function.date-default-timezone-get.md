---
navigation:
  - function.date-date-set.md: « date\_date\_set
  - function.date-default-timezone-set.md: date\_default\_timezone\_set »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: date\_default\_timezone\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# date\_default\_timezone\_get

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

date\_default\_timezone\_get — Повертає часовий пояс, який використовується за умовчанням усіма функціями дати/часу в скрипті

### Опис

```methodsynopsis
date_default_timezone_get(): string
```

Функція намагається отримати часовий пояс за замовчуванням таким чином:

-   Читання налаштування часового поясу за допомогою функції[date\_default\_timezone\_set()](function.date-default-timezone-set.md)(якщо можна застосувати)
    
-   Читання значення ini-налаштування[date.timezone](datetime.configuration.md#ini.date.timezone)(якщо задана)
    

Якщо жоден із способів не приніс результату, **date\_default\_timezone\_get()** поверне часовий пояс `UTC`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string).

### Приклади

**Приклад #1 Отримання часового поясу за замовчуванням**

```php
<?php
date_default_timezone_set('Europe/London');

if (date_default_timezone_get()) {
    echo 'date_default_timezone_set: ' . date_default_timezone_get() . '<br />';
}

if (ini_get('date.timezone')) {
    echo 'date.timezone: ' . ini_get('date.timezone');
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
date_default_timezone_set: Europe/London
date.timezone: Europe/London
```

**Приклад #2 Отримання абревіатури часового поясу**

```php
<?php
date_default_timezone_set('America/Los_Angeles');
echo date_default_timezone_get() . ' => ' . date('e') . ' => ' . date('T');
?>
```

Результат виконання наведеного прикладу:

```
America/Los_Angeles => America/Los_Angeles => PST
```

### Дивіться також

-   [date\_default\_timezone\_set()](function.date-default-timezone-set.md) \- Встановлює часовий пояс за промовчанням для всіх функцій дати/часу у скрипті
-   [Список підтримуваних часових поясів](timezones.md)
