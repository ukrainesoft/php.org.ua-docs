---
navigation:
  - solrobject.getpropertynames.html: '« SolrObject::getPropertyNames'
  - solrobject.offsetget.html: 'SolrObject::offsetGet »'
  - index.html: PHP Manual
  - class.solrobject.html: SolrObject
title: 'SolrObject::offsetExists'
---
# SolrObject::offsetExists

(PECL solr> = 0.9.2)

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
