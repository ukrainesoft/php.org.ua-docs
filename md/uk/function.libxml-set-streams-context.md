Налаштування контексту потоків для наступного завантаження або запису документа за допомогою libxml

-   [« libxml\_set\_external\_entity\_loader](function.libxml-set-external-entity-loader.html)
    
-   [libxml\_use\_internal\_errors »](function.libxml-use-internal-errors.html)
    
-   [PHP Manual](index.html)
    
-   [Функции libxml](ref.libxml.html)
    
-   Налаштування контексту потоків для наступного завантаження або запису документа за допомогою libxml
    

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

Ресурс контексту потоку (створений функцією [stream\_context\_create()](function.stream-context-create.html)

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

-   [stream\_context\_create()](function.stream-context-create.html) - Створює контекст потоку