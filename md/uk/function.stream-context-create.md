---
navigation:
  - function.stream-bucket-prepend.md: « stream\_bucket\_prepend
  - function.stream-context-get-default.md: stream\_context\_get\_default »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_context\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_context\_create

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

stream\_context\_create — Створює контекст потоку

### Опис

```methodsynopsis
stream_context_create(?array $options = null, ?array $params = null): resource
```

Створює та повертає контекст потоку з опціями, вказаними в масиві `options`

### Список параметрів

`options`

Має бути асоціативним масивом у форматі `$arr['wrapper']['option'] = $value`или\*\*`null`\*\*. Список доступних обгорток та опцій дивіться у розділі [Опції контексту](context.md)

Значение по умолчанию -**`null`**

`params`

Має бути асоціативним масивом у форматі `$arr['parameter'] = $value`или\*\*`null`\*\*. Зверніться до розділу [Опції контексту](context.params.md) за списком стандартних параметрів потоку.

### Значення, що повертаються

Ресурс контексту потоку.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметри `options`и`params` тепер допускають значення null. |

### Приклади

**Приклад #1 Использование**stream\_context\_create()\*\*\*\*

```php
<?php
$opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar\r\n"
  )
);

$context = stream_context_create($opts);

/* Отправляет http-запрос на домен www.example.com
   с дополнительными заголовкам, показанными выше */
$fp = fopen('http://www.example.com', 'r', false, $context);
fpassthru($fp);
fclose($fp);
?>
```

### Дивіться також

-   [stream\_context\_set\_option()](function.stream-context-set-option.md) \- Встановлює опцію для потоку/обгортки/контексту
-   Список підтримуваних обгорток ([Підтримувані протоколи та обгортки](wrappers.md)) .
-   Опції контексту ([Контекстні опції та параметри](context.md)) .
