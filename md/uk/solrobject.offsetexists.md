---
navigation:
  - solrobject.getpropertynames.md: '« SolrObject::getPropertyNames'
  - solrobject.offsetget.md: 'SolrObject::offsetGet »'
  - index.md: PHP Manual
  - class.solrobject.md: SolrObject
title: 'SolrObject::offsetExists'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrObject::offsetExists

(PECL solr >= 0.9.2)

SolrObject::offsetExists — Перевіряє, чи існує властивість

### Опис

```methodsynopsis
public SolrObject::offsetExists(string $property_name): bool
```

Перевіряє, чи існує властивість. Використовується, коли об'єкт обробляється масивом.

### Список параметрів

`property_name`

Назва якості.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
