Отримує поле на ім'я

-   [« SolrInputDocument::getChildDocumentsCount](solrinputdocument.getchilddocumentscount.html)
    
-   [SolrInputDocument::getFieldBoost »](solrinputdocument.getfieldboost.html)
    
-   [PHP Manual](index.html)
    
-   [SolrInputDocument](class.solrinputdocument.html)
    
-   Отримує поле на ім'я
    

# SolrInputDocument::getField

(PECL solr> = 0.9.2)

SolrInputDocument::getField — Отримує поле на ім'я

### Опис

```methodsynopsis
public SolrInputDocument::getField(string $fieldName): SolrDocumentField
```

Отримує поле у ​​документі.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає об'єкт SolrDocumentField у разі успішного виконання та **`false`** у разі виникнення помилки.