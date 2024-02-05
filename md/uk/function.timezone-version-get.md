---
navigation:
  - function.timezone-transitions-get.md: « timezone\_transitions\_get
  - datetime.error.tree.md: Date/Time Errors and Exceptions »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: timezone\_version\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# timezone\_version\_get

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

timezone\_version\_get — отримання номера версії бази даних часових поясів

### Опис

```methodsynopsis
timezone_version_get(): string
```

Повертає номер версії бази даних часового поясу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string) у форматі `YYYY.increment`, наПриклад,`2022.2`

Якщо у вас стара версія бази даних часових поясів (наприклад, вона показує не поточний рік), то ви можете оновити інформацію про часові пояси, або оновивши версію PHP, або встановивши пакет PECL [» timezonedb](https://pecl.php.net/package/timezonedb)

Деякі Linux-дистрибутиви виправляють підтримку дати/часу в PHP, щоб використовувати альтернативне джерело інформації про часові пояси. У такій ситуації функція повертатиме `0.system`. У цьому випадку рекомендується встановити пакет PECL [» timezonedb](https://pecl.php.net/package/timezonedb)

### Приклади

**Приклад #1 Визначення версії бази даних часових поясів**

```php
<?php
echo timezone_version_get();
?>
```

Висновок наведеного прикладу буде схожим на:

```
2022.2
```

### Дивіться також

-   [Список підтримуваних часових поясів](timezones.md)
