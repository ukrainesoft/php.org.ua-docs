---
navigation:
  - function.stream-context-get-params.md: « stream\_context\_get\_params
  - function.stream-context-set-option.md: stream\_context\_set\_option »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_context\_set\_default
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_context\_set\_default

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

stream\_context\_set\_default — Встановити контекст потоку за промовчанням

### Опис

```methodsynopsis
stream_context_set_default(array $options): resource
```

Встановити контекст потоку за замовчуванням, який буде використовуватися щоразу, коли файлові операції ([fopen()](function.fopen.md) [file\_get\_contents()](function.file-get-contents.md) і т.д.) викликаються без параметра контексту. Використовується той же синтаксис, що і [stream\_context\_create()](function.stream-context-create.md)

### Список параметрів

`options`

Опції для встановлення для контексту за промовчанням.

> **Зауваження** :
> 
> Параметр`options` має бути асоціативним масивом асоціативних масивів у форматі `$arr['wrapper']['option'] = $value`

### Значення, що повертаються

Повертає контекст потоку за промовчанням.

### Приклади

**Приклад #1**stream\_context\_set\_default()**example**

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

$default = stream_context_set_default($default_opts);

/* Отправляет обычный GET-запрос к прокси-серверу по адресу 10.54.1.39
 * Для www.example.com используются опции контекста, указанные в $default_opts
 */
readfile('http://www.example.com');
?>
```

### Дивіться також

-   [stream\_context\_create()](function.stream-context-create.md) \- Створює контекст потоку
-   [stream\_context\_get\_default()](function.stream-context-get-default.md) \- Отримує контекст потоку за умовчанням
-   Listing of supported wrappers with context options ([Підтримувані протоколи та обгортки](wrappers.md)
