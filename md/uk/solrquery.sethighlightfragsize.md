Розмір фрагментів, які слід враховувати під час виділення

-   [« SolrQuery::setHighlightFragmenter](solrquery.sethighlightfragmenter.html)
    
-   [SolrQuery::setHighlightHighlightMultiTerm »](solrquery.sethighlighthighlightmultiterm.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Розмір фрагментів, які слід враховувати під час виділення
    

# SolrQuery::setHighlightFragsize

(PECL solr> = 0.9.2)

SolrQuery::setHighlightFragsize — Розмір фрагментів, які слід враховувати при виділенні

### Опис

```methodsynopsis
public SolrQuery::setHighlightFragsize(int $size, string $field_override = ?): SolrQuery
```

Встановлює розмір символів фрагментів для виділення. "0" вказує на те, що слід використовувати всі значення поля (без фрагментації).

### Список параметрів

`size`

Розмір у символах фрагментів, які слід враховувати при виділенні

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.