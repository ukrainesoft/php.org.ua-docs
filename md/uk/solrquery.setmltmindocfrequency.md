Встановлює частоту mltMinDoc

-   [« SolrQuery::setMltMaxWordLength](solrquery.setmltmaxwordlength.html)
    
-   [SolrQuery::setMltMinTermFrequency »](solrquery.setmltmintermfrequency.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Встановлює частоту mltMinDoc
    

# SolrQuery::setMltMinDocFrequency

(PECL solr> = 0.9.2)

SolrQuery::setMltMinDocFrequency — Встановлює частоту mltMinDoc

### Опис

```methodsynopsis
public SolrQuery::setMltMinDocFrequency(int $minDocFrequency): SolrQuery
```

Частота, з якої ігноруватимуться слова, яких немає принаймні в такій кількості документів.

### Список параметрів

`minDocFrequency`

Частота, з якої ігноруватимуться слова, яких немає принаймні в такій кількості документів.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.