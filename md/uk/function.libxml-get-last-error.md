---
navigation:
  - function.libxml-get-external-entity-loader.md: « libxml\_get\_external\_entity\_loader
  - function.libxml-set-external-entity-loader.md: libxml\_set\_external\_entity\_loader »
  - index.md: PHP Manual
  - ref.libxml.md: Функції libxml
title: libxml\_get\_last\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# libxml\_get\_last\_error

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

libxml\_get\_last\_error — Вилучення останньої помилки з libxml

### Опис

```methodsynopsis
libxml_get_last_error(): LibXMLError|false
```

Вилучення останньої помилки з libxml.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [LibXMLError](class.libxmlerror.md)якщо в буфері є помилки, або **`false`** в іншому випадку.

### Дивіться також

-   [libxml\_get\_errors()](function.libxml-get-errors.md) \- Отримання масиву помилок, що відбулися.
-   [libxml\_clear\_errors()](function.libxml-clear-errors.md) \- Очищення буфера помилок libxml
