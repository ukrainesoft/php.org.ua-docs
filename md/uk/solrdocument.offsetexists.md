Перевіряє, чи існує конкретне поле

-   [« SolrDocument::next](solrdocument.next.md)
    
-   [SolrDocument::offsetGet »](solrdocument.offsetget.md)
    
-   [PHP Manual](index.md)
    
-   [SolrDocument](class.solrdocument.md)
    
-   Перевіряє, чи існує конкретне поле
    

# SolrDocument::offsetExists

(PECL solr> = 0.9.2)

SolrDocument::offsetExists — Перевіряє, чи існує конкретне поле

### Опис

```methodsynopsis
public SolrDocument::offsetExists(string $fieldName): bool
```

Перевіряє, чи існує певне поле. Використовується, коли об'єкт обробляється масивом.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.