---
navigation:
  - function.stream-register-wrapper.md: « stream\_register\_wrapper
  - function.stream-select.md: stream\_select »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_resolve\_include\_path
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_resolve\_include\_path

(PHP 5 >= 5.3.2, PHP 7, PHP 8)

stream\_resolve\_include\_path — Перетворити повне ім'я файлу за допомогою шляхів увімкнення.

### Опис

```methodsynopsis
stream_resolve_include_path(string $filename): string|false
```

Преобразовать полное имя файла из параметра`filename`, використовуючи шляхи включення відповідно до тих же правил, що і функції [fopen()](function.fopen.md) [include](function.include.md)

### Список параметрів

`filename`

Ім'я файлу, яке потрібно перетворити.

### Значення, що повертаються

Повертає рядок (string), що містить отримане абсолютне ім'я файлу або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** stream\_resolve\_include\_path()\*\*\*\*

Основний приклад використання.

```php
<?php
var_dump(stream_resolve_include_path("test.php"));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(22) "/var/www/html/test.php"
```
