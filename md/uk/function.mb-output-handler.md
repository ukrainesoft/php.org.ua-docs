---
navigation:
  - function.mb-ord.md: « mb\_ord
  - function.mb-parse-str.md: mb\_parse\_str »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_output\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_output\_handler

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_output\_handler - Перетворює кодування символів у буфері виводу, виступаючи в ролі callback-функції

### Опис

```methodsynopsis
mb_output_handler(string $string, int $status): string
```

Функция**mb\_output\_handler()** - Це callback-функція функції [ob\_start()](function.ob-start.md)Функция**mb\_output\_handler()** перетворює символи буфера виведення з внутрішнього кодування символів кодування HTTP-виводу.

### Список параметрів

`string`

Вміст буфера виводу.

`status`

Стан буфера виведення.

### Значення, що повертаються

Повертає перетворений рядок (string).

### Приклади

**Пример #1 Пример использования функции**mb\_output\_handler()\*\*\*\*

```php
<?php
mb_http_output("UTF-8");
ob_start("mb_output_handler");
?>
```

### Примітки

> **Зауваження** :
> 
> Якщо потрібно вивести двійкові дані, зображення, наприклад, необхідно передати заголовок Content-Type функцією [header()](function.header.md) перед тим, як будь-які двійкові дані будуть передані клієнту (наприклад, header("Content-Type: image/png")). Якщо заголовок Content-Type передано, перетворення кодувань вихідних символів не виконується.
> 
> Зауважте, якщо надіслано заголовок «Content-Type: text/\*», дані, що пересилаються, будуть розглянуті як текст; відбудеться перетворення.

### Дивіться також

-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу
