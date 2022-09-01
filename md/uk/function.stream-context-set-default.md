---
navigation:
  - function.stream-context-get-params.html: « streamcontextgetparams
  - function.stream-context-set-option.html: streamcontextsetoption »
  - index.html: PHP Manual
  - ref.stream.html: Функції для роботи з потоками
title: streamcontextsetdefault
---
# streamcontextsetdefault

(PHP 5> = 5.3.0, PHP 7, PHP 8)

streamcontextsetdefault — Встановити контекст потоку за промовчанням

### Опис

```methodsynopsis
stream_context_set_default(array $options): resource
```

Встановити контекст потоку за промовчанням, який буде використовуватися щоразу, коли файлові операції ([fopen()](function.fopen.html) [filegetcontents()](function.file-get-contents.html) і т.д.) викликаються без параметра контексту. Використовується той же синтаксис, що і [streamcontextcreate()](function.stream-context-create.html)

### Список параметрів

`options`

Опції для встановлення для контексту за промовчанням.

> **Зауваження**
> 
> Параметр `options` має бути асоціативним масивом асоціативних масивів у форматі `$arr['wrapper']['option'] = $value`

### Значення, що повертаються

Повертає контекст потоку за промовчанням.

### Приклади

**Приклад #1 **streamcontextsetdefault()** example**

```php
<?php
$default_opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar",
    'proxy'=>"tcp://10.54.1.39:8000"
  )
);

$default = stream_context_set_default($default_opts);

/* Отправляет обычный GET-запрос к прокси-серверу по адресу 10.54.1.39
 * Для www.example.com используются опции контекста, указанные в $default_opts
 */
readfile('http://www.example.com');
?>
```

### Дивіться також

-   [streamcontextcreate()](function.stream-context-create.html) - Створює контекст потоку
-   [streamcontextgetdefault()](function.stream-context-get-default.html) - Отримує контекст потоку за умовчанням
-   Listing of supported wrappers with context options ([Підтримувані протоколи та обгортки](wrappers.html)
