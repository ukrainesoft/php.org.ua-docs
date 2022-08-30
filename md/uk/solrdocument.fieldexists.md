Перевіряє, чи існує поле у ​​документі

-   [« SolrDocument::destruct](solrdocument.destruct.html)
    
-   [SolrDocument::get »](solrdocument.get.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDocument](class.solrdocument.html)
    
-   Перевіряє, чи існує поле у ​​документі
    

# SolrDocument::fieldExists

(PECL solr> = 0.9.2)

SolrDocument::fieldExists — Перевіряє, чи існує поле в документі

### Опис

```methodsynopsis
public SolrDocument::fieldExists(string $fieldName): bool
```

Перевіряє, чи поле поле в документі є коректним ім'ям поля.

### Список параметрів

`fieldName`

Назва поля

### Значення, що повертаються

Повертає **`true`** якщо поле є і **`false`** якщо це не так.