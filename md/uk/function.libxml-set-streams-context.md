---
navigation:
  - function.libxml-set-external-entity-loader.md: « libxmlsetexternalentityloader
  - function.libxml-use-internal-errors.md: libxmluseinternalerrors »
  - index.md: PHP Manual
  - ref.libxml.md: Функції libxml
title: libxmlsetstreamscontext
---
# libxmlsetstreamscontext

(PHP 5, PHP 7, PHP 8)

libxmlsetstreamscontext — Встановлення контексту потоків для наступного завантаження або запису документа за допомогою libxml

### Опис

```methodsynopsis
libxml_set_streams_context(resource $context): void
```

Встановіть контекст потоку для наступного завантаження або запису документа за допомогою libxml.

### Список параметрів

`context`

Ресурс контексту потоку (створений функцією [streamcontextcreate()](function.stream-context-create.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **libxmlsetstreamscontext()****

```php
<?php

$opts = array(
    'http' => array(
        'user_agent' => 'PHP libxml agent',
    )
);

$context = stream_context_create($opts);
libxml_set_streams_context($context);

// загрузить файл через HTTP
$doc = DOMDocument::load('http://www.example.com/file.xml');

?>
```

### Дивіться також

-   [streamcontextcreate()](function.stream-context-create.md) - Створює контекст потоку
