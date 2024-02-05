---
navigation:
  - function.libxml-set-external-entity-loader.md: « libxml\_set\_external\_entity\_loader
  - function.libxml-use-internal-errors.md: libxml\_use\_internal\_errors »
  - index.md: PHP Manual
  - ref.libxml.md: Функції libxml
title: libxml\_set\_streams\_context
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# libxml\_set\_streams\_context

(PHP 5, PHP 7, PHP 8)

libxml\_set\_streams\_context — Встановлення контексту потоків для наступного завантаження або запису документа за допомогою libxml

### Опис

```methodsynopsis
libxml_set_streams_context(resource $context): void
```

Встановіть контекст потоку для наступного завантаження або запису документа за допомогою libxml.

### Список параметрів

`context`

Ресурс контексту потоку (створений функцією [stream\_context\_create()](function.stream-context-create.md)) .

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** libxml\_set\_streams\_context()\*\*\*\*

```php
<?php

$opts = array(
    'http' => array(
        'user_agent' => 'PHP libxml agent',
    )
);

$context = stream_context_create($opts);
libxml_set_streams_context($context);

// загрузить файл через HTTP
$doc = DOMDocument::load('http://www.example.com/file.xml');

?>
```

### Дивіться також

-   [stream\_context\_create()](function.stream-context-create.md) \- Створює контекст потоку
