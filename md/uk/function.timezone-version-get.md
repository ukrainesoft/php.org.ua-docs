---
navigation:
  - function.timezone-transitions-get.md: « timezonetransitionsget
  - datetime.formats.md: Допустимі формати дати/часу »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: timezoneversionget
---
# timezoneversionget

(PHP 5> = 5.3.0, PHP 7, PHP 8)

timezoneversionget — отримання номера версії бази даних часових поясів

### Опис

```methodsynopsis
timezone_version_get(): string
```

Повертає номер версії бази даних часового поясу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string).

### Приклади

**Приклад #1 Визначення версії бази даних часових поясів**

```php
<?php
echo timezone_version_get();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
2009.7
```

### Дивіться також

-   [Список підтримуваних часових поясів](timezones.md)
