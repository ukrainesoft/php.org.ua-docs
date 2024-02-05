---
navigation:
  - function.headers-sent.md: « headers\_sent
  - function.inet-ntop.md: inet\_ntop »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: http\_response\_code
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# http\_response\_code

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

http\_response\_code — Отримує або встановлює код відповіді HTTP

### Опис

```methodsynopsis
http_response_code(int $response_code = 0): int|bool
```

Отримує або вказує коди відповідей HTTP.

### Список параметрів

`response_code`

Код ответа устанавливается с помощью опционального параметра`response_code`

### Значення, що повертаються

Якщо `response_code` заданий, то буде повернено попередній код статусу. Якщо `response_code` не заданий, буде повернено поточний код статусу. Обидва ці значення будуть за промовчанням мати код стану `200`якщо вони використовуються в оточенні веб-сервера.

Якщо `response_code` не заданий і використовується не в оточенні веб-сервера (наприклад, CLI), то буде повернуто **`false`**. Якщо `response_code` заданий та використовується не в оточенні веб-сервера, то буде повернено **`true`** (але якщо не було встановлено попередній код статусу).

### Приклади

**Пример #1 Использование**http\_response\_code()\*\* в оточенні веб-сервера\*\*

```php
<?php

// Берём текущий код и устанавливаем новый
var_dump(http_response_code(404));

// Берём новый код
var_dump(http_response_code());
?>
```

Результат виконання наведеного прикладу:

```
int(200)
int(404)
```

**Пример #2 Использование**http\_response\_code()\*\* у CLI\*\*

```php
<?php

// Берём текущий код по умолчанию
var_dump(http_response_code());

// Устанавливаем код
var_dump(http_response_code(201));

// Берём новый код
var_dump(http_response_code());
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
int(201)
```

### Дивіться також

-   [header()](function.header.md) \- Надсилає необроблений (сирий) HTTP-заголовок
-   [headers\_list()](function.headers-list.md) \- Повертає список переданих заголовків (або готових до відправлення)
