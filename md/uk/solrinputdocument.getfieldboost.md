Отримує значення підвищення для певного поля

-   [« SolrInputDocument::getField](solrinputdocument.getfield.html)
    
-   [SolrInputDocument::getFieldCount »](solrinputdocument.getfieldcount.html)
    
-   [PHP Manual](index.html)
    
-   [SolrInputDocument](class.solrinputdocument.html)
    
-   Отримує значення підвищення для певного поля
    

# SolrInputDocument::getFieldBoost

(PECL solr> = 0.9.2)

SolrInputDocument::getFieldBoost — Отримує значення підвищення для певного поля

### Опис

```methodsynopsis
public SolrInputDocument::getFieldBoost(string $fieldName): float
```

Отримує значення підвищення для певного поля.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає значення підвищення для поля або **`false`** у разі виникнення помилки.