Доступ до поля як властивості

-   [« SolrDocument::fieldExists](solrdocument.fieldexists.html)
    
-   [SolrDocument::getChildDocuments »](solrdocument.getchilddocuments.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDocument](class.solrdocument.html)
    
-   Доступ до поля як властивості
    

# SolrDocument::get

(PECL solr> = 0.9.2)

SolrDocument::get — Доступ до поля як властивості

### Опис

```methodsynopsis
public SolrDocument::__get(string $fieldName): SolrDocumentField
```

Магічний метод доступу до поля як властивості.

### Список параметрів

`fieldName`

Назва поля

### Значення, що повертаються

Повертає екземпляр SolrDocumentField.