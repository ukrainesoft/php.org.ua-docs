Встановлює значення збільшення індексу часу для поля

-   [« SolrInputDocument::setBoost](solrinputdocument.setboost.html)
    
-   [SolrInputDocument::sort »](solrinputdocument.sort.html)
    
-   [PHP Manual](index.html)
    
-   [SolrInputDocument](class.solrinputdocument.html)
    
-   Встановлює значення збільшення індексу часу для поля
    

# SolrInputDocument::setFieldBoost

(PECL solr> = 0.9.2)

SolrInputDocument::setFieldBoost — Встановлює значення підвищення індексу часу для поля

### Опис

```methodsynopsis
public SolrInputDocument::setFieldBoost(string $fieldName, float $fieldBoostValue): bool
```

Встановлює значення індексу часу для поля. Замінює поточне значення для цього поля.

### Список параметрів

`fieldName`

Назва поля.

`fieldBoostValue`

Індекс часу для підвищення значення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.