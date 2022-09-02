---
navigation:
  - reserved.variables.get.md: GET
  - reserved.variables.files.md: FILES »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: POST
---
# POST

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

POST — Змінні HTTP POST

### Опис

Асоціативний масив даних, переданих скрипту через HTTP методом POST під час використання `application/x-www-form-urlencoded` або `multipart/form-data` у заголовку Content-Type запиту HTTP.

### Приклади

**Приклад #1 Приклад використання $POST**

```php
<?php
echo 'Привет ' . htmlspecialchars($_POST["name"]) . '!';
?>
```

Очевидно, що користувач надіслав через POST name=Іван

Результатом виконання цього прикладу буде щось подібне:

```
Привет, Иван!
```

### Примітки

> **Зауваження**
> 
> Це 'суперглобальна' або автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

### Дивіться також

-   [Обробка зовнішніх змінних](language.variables.external.md)
-   [Фільтрування даних](book.filter.md)
