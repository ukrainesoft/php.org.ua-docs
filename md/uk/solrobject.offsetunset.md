---
navigation:
  - solrobject.offsetset.md: '« SolrObject::offsetSet'
  - class.solrclient.md: SolrClient »
  - index.md: PHP Manual
  - class.solrobject.md: SolrObject
title: 'SolrObject::offsetUnset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrObject::offsetUnset

(PECL solr >= 0.9.2)

SolrObject::offsetUnset — Скидає значення властивості

### Опис

```methodsynopsis
public SolrObject::offsetUnset(string $property_name): void
```

Скидає значення якості. Використовується, коли об'єкт обробляється масивом. Цей об'єкт доступний лише для читання. Цього ніколи не слід робити.

### Список параметрів

`property_name`

Ім'я якості.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SolrObject::offsetUnset()\*\*\*\*

```php
<?php
/* ... */
?>
```

Висновок наведеного прикладу буде схожим на:

```
...
```
