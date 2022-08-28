Встановлює коефіцієнт, який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента

-   [« SolrQuery::setHighlightRegexPattern](solrquery.sethighlightregexpattern.html)
    
-   [SolrQuery::setHighlightRequireFieldMatch »](solrquery.sethighlightrequirefieldmatch.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Встановлює коефіцієнт, який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента
    

# SolrQuery::setHighlightRegexSlop

(PECL solr> = 0.9.2)

SolrQuery::setHighlightRegexSlop — Встановлює коефіцієнт, на який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента

### Опис

```methodsynopsis
public SolrQuery::setHighlightRegexSlop(float $factor): SolrQuery
```

Коефіцієнт, на який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента (зазначеного SolrQuery::setHighlightFragsize) для відповідності регулярному виразу.

### Список параметрів

`factor`

Коефіцієнт, який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.