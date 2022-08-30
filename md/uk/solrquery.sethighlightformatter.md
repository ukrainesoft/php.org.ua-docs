Задає засіб форматування для виведення виділення

-   [« SolrQuery::setHighlightAlternateField](solrquery.sethighlightalternatefield.md)
    
-   [SolrQuery::setHighlightFragmenter »](solrquery.sethighlightfragmenter.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Задає засіб форматування для виведення виділення
    

# SolrQuery::setHighlightFormatter

(PECL solr> = 0.9.2)

SolrQuery::setHighlightFormatter — Задає засіб форматування для виведення виділення

### Опис

```methodsynopsis
public SolrQuery::setHighlightFormatter(string $formatter, string $field_override = ?): SolrQuery
```

Задає засіб форматування для виведення виділення

### Список параметрів

`formatter`

В даний час єдине допустиме значення - "simple"

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає екземпляр [SolrQuery](class.solrquery.md)