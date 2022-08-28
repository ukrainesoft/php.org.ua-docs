Додає поле до документа

-   [« SolrDocument::offsetGet](solrdocument.offsetget.html)
    
-   [SolrDocument::offsetUnset »](solrdocument.offsetunset.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDocument](class.solrdocument.html)
    
-   Додає поле до документа
    

# SolrDocument::offsetSet

(PECL solr> = 0.9.2)

SolrDocument::offsetSet — Додає поле до документа

### Опис

```methodsynopsis
public SolrDocument::offsetSet(string $fieldName, string $fieldValue): void
```

Використовується, коли об'єкт обробляється як масив, щоб додати поле до документа.

### Список параметрів

`fieldName`

Назва поля.

`fieldValue`

Значення цього поля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.