Відповідає facet.missing

-   [« SolrQuery::setFacetMinCount](solrquery.setfacetmincount.html)
    
-   [SolrQuery::setFacetOffset »](solrquery.setfacetoffset.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Відповідає facet.missing
    

# SolrQuery::setFacetMissing

(PECL solr> = 0.9.2)

SolrQuery::setFacetMissing — Відповідає facet.missing

### Опис

```methodsynopsis
public SolrQuery::setFacetMissing(bool $flag, string $field_override = ?): SolrQuery
```

Використовується для позначення того, що на додаток до обмежень поля фасету, що базуються на виразах, повинна бути обчислена кількість усіх результатів зіставлення, які не мають значення для поля.

### Список параметрів

`flag`

**`true`** включає цю функцію, **`false`** відключає її.

`field_override`

Ім'я поля.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.