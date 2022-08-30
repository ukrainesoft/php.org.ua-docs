Видаляє поле з документа

-   [« SolrInputDocument::construct](solrinputdocument.construct.md)
    
-   [SolrInputDocument::destruct »](solrinputdocument.destruct.md)
    
-   [PHP Manual](index.md)
    
-   [SolrInputDocument](class.solrinputdocument.md)
    
-   Видаляє поле з документа
    

# SolrInputDocument::deleteField

(PECL solr> = 0.9.2)

SolrInputDocument::deleteField — Видаляє поле з документа

### Опис

```methodsynopsis
public SolrInputDocument::deleteField(string $fieldName): bool
```

Видаляє поле з документа.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.