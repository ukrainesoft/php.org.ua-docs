Отримує або встановлює код відповіді HTTP

-   [« headers\_sent](function.headers-sent.html)
    
-   [inet\_ntop »](function.inet-ntop.html)
    
-   [PHP Manual](index.html)
    
-   [Сетевые функции](ref.network.html)
    
-   Отримує або встановлює код відповіді HTTP
    

# httpresponsecode

(PHP 5> = 5.4.0, PHP 7, PHP 8)

httpresponsecode — Отримує або встановлює код відповіді HTTP

### Опис

```methodsynopsis
http_response_code(int $response_code = 0): int|bool
```

Отримує або вказує коди відповідей HTTP.

### Список параметрів

`response_code`

Код відповіді встановлюється за допомогою опціонального параметра `response_code`

### Значення, що повертаються

Якщо `response_code` заданий, то буде повернено попередній код статусу. Якщо `response_code` не заданий, буде повернено поточний код статусу. Обидва ці значення будуть за промовчанням мати код стану `200`якщо вони використовуються в оточенні веб-сервера.

Якщо `response_code` не заданий і використовується не в оточенні веб-сервера (наприклад, CLI), то буде повернуто **`false`**. Якщо `response_code` заданий та використовується не в оточенні веб-сервера, то буде повернено **`true`** (але якщо не було встановлено попередній код статусу).

### Приклади

**Приклад #1 Використання **httpresponsecode()** в оточенні веб-сервера**

```php
<?php

// Берём текущий код и устанавливаем новый
var_dump(http_response_code(404));

// Берём новый код
var_dump(http_response_code());
?>
```

Результат виконання цього прикладу:

```
int(200)
int(404)
```

**Приклад #2 Використання **httpresponsecode()** у CLI**

```php
<?php

// Берём текущий код по умолчанию
var_dump(http_response_code());

// Устанавливаем код
var_dump(http_response_code(201));

// Берём новый код
var_dump(http_response_code());
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
int(201)
```

### Дивіться також

-   [header()](function.header.html) - Надсилання HTTP-заголовка
-   [headers\_list()](function.headers-list.html) - Повертає список переданих заголовків (або готових до відправлення)