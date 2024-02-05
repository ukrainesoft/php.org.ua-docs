---
navigation:
  - function.libxml-get-errors.md: « libxml\_get\_errors
  - function.libxml-get-last-error.md: libxml\_get\_last\_error »
  - index.md: PHP Manual
  - ref.libxml.md: Функції libxml
title: libxml\_get\_external\_entity\_loader
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# libxml\_get\_external\_entity\_loader

(PHP 8 >= 8.2.0)

libxml\_get\_external\_entity\_loader — Отримує поточний зовнішній завантажувач сутностей

### Опис

```methodsynopsis
libxml_get_external_entity_loader(): ?callable
```

Отримує зовнішній завантажувач сутностей, встановлений раніше за допомогою функції [libxml\_set\_external\_entity\_loader()](function.libxml-set-external-entity-loader.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Зовнішній завантажувач сутностей, встановлений раніше за допомогою функції [libxml\_set\_external\_entity\_loader()](function.libxml-set-external-entity-loader.md). Якщо ця функція ніколи не викликалася або якщо вона була викликана з **`null`**, буде повернутий **`null`**

### Дивіться також

-   [libxml\_set\_external\_entity\_loader()](function.libxml-set-external-entity-loader.md) \- Зміна завантажувача за умовчанням для зовнішніх об'єктів
