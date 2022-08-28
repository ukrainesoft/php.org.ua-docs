Отримує поле на ім'я

-   [« SolrDocument::getChildDocumentsCount](solrdocument.getchilddocumentscount.html)
    
-   [SolrDocument::getFieldCount »](solrdocument.getfieldcount.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDocument](class.solrdocument.html)
    
-   Отримує поле на ім'я
    

# SolrDocument::getField

(PECL solr> = 0.9.2)

SolrDocument::getField — Отримує поле на ім'я

### Опис

```methodsynopsis
public SolrDocument::getField(string $fieldName): SolrDocumentField
```

Отримує поле на ім'я.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає SolrDocumentField у разі успішного виконання та **`false`** у разі виникнення помилки.