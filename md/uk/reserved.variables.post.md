---
navigation:
  - reserved.variables.get.md: « $\_GET
  - reserved.variables.files.md: $\_FILES »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: $\_POST
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# $\_POST

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

$\_POST — Змінні HTTP POST

### Опис

Асоціативний масив даних, переданих скрипту через HTTP методом POST під час використання `application/x-www-form-urlencoded`или`multipart/form-data`в заголовке Content-Type запроса HTTP.

### Приклади

**Приклад #1 Приклад використання $\_POST**

```php
<?php
echo 'Привет ' . htmlspecialchars($_POST["name"]) . '!';
?>
```

Очевидно, що користувач надіслав через POST name=Іван

Висновок наведеного прикладу буде схожим на:

```
Привет, Иван!
```

### Примітки

> **Зауваження** :
> 
> Це «суперглобальна» чи автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

### Дивіться також

-   [Обробка зовнішніх змінних](language.variables.external.md)
-   [Фільтрування даних](book.filter.md)
