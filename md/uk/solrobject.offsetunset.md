Скидає значення якості

-   [« SolrObject::offsetSet](solrobject.offsetset.html)
    
-   [SolrClient »](class.solrclient.html)
    
-   [PHP Manual](index.html)
    
-   [SolrObject](class.solrobject.html)
    
-   Скидає значення якості
    

# SolrObject::offsetUnset

(PECL solr> = 0.9.2)

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SolrObject::offsetUnset()****

```php
<?php
/* ... */
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
...
```