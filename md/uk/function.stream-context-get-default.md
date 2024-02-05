---
navigation:
  - function.stream-context-create.md: « stream\_context\_create
  - function.stream-context-get-options.md: stream\_context\_get\_options »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_context\_get\_default
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_context\_get\_default

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

stream\_context\_get\_default — Отримує контекст потоку за промовчанням

### Опис

```methodsynopsis
stream_context_get_default(?array $options = null): resource
```

Повертає контекст потоку за замовчуванням, який використовується у будь-яких файлових операціях ([fopen()](function.fopen.md) [file\_get\_contents()](function.file-get-contents.md) і т.д.), викликаних без параметра контексту. Опції для контексту за умовчанням можуть бути опціонально вказані за допомогою цієї функції використовуючи той же синтаксис, що і для [stream\_context\_create()](function.stream-context-create.md)

### Список параметрів

`options`

`options` має бути асоціативним масивом асоціативних масивів у форматі `$arr['wrapper']['option'] = $value`или\*\*`null`\*\*

### Значення, що повертаються

Ресурс контексту потоку.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`options` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**stream\_context\_get\_default()\*\*\*\*

```php
<?php
$default_opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar",
    'proxy'=>"tcp://10.54.1.39:8000"
  )
);


$alternate_opts = array(
  'http'=>array(
    'method'=>"POST",
    'header'=>"Content-type: application/x-www-form-urlencoded\r\n" .
              "Content-length: " . strlen("baz=bomb"),
    'content'=>"baz=bomb"
  )
);

$default = stream_context_get_default($default_opts);
$alternate = stream_context_create($alternate_opts);

/* Отправляет обычный GET-запрос на прокси-сервер 10.54.1.39
 * Для www.example.com используются опции контекста, указанные в $default_opts
 */
readfile('http://www.example.com');

/* Отправляет POST-запрос напрямую к www.example.com
 * Используемые опции контекста определены в $alternate_opts
 */
readfile('http://www.example.com', false, $alternate);

?>
```

### Дивіться також

-   [stream\_context\_create()](function.stream-context-create.md) \- Створює контекст потоку
-   [stream\_context\_set\_default()](function.stream-context-set-default.md) \- Встановити контекст потоку за промовчанням
-   Список підтримуваних обгорток з опціями контексту ([Підтримувані протоколи та обгортки](wrappers.md)
