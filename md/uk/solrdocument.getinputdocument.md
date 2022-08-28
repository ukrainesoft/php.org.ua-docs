SolrInputDocument повертає еквівалент об'єкта

-   [« SolrDocument::getFieldNames](solrdocument.getfieldnames.html)
    
-   [SolrDocument::hasChildDocuments »](solrdocument.haschilddocuments.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDocument](class.solrdocument.html)
    
-   SolrInputDocument повертає еквівалент об'єкта
    

# SolrDocument::getInputDocument

(PECL solr> = 0.9.2)

SolrDocument::getInputDocument — Повертає SolrInputDocument еквівалент об'єкту

### Опис

```methodsynopsis
public SolrDocument::getInputDocument(): SolrInputDocument
```

SolrInputDocument повертає еквівалент об'єкта. Це корисно, якщо потрібно повторно надіслати/оновити документ, отриманий із запиту.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає SolrInputDocument у разі успішного виконання та **`null`** у разі виникнення помилки.