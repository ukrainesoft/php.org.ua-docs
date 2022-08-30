Задає максимальну кількість токенів для аналізу

-   [« SolrQuery::setMltMaxNumQueryTerms](solrquery.setmltmaxnumqueryterms.md)
    
-   [SolrQuery::setMltMaxWordLength »](solrquery.setmltmaxwordlength.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Задає максимальну кількість токенів для аналізу
    

# SolrQuery::setMltMaxNumTokens

(PECL solr> = 0.9.2)

SolrQuery::setMltMaxNumTokens — Задає максимальну кількість токенів для аналізу

### Опис

```methodsynopsis
public SolrQuery::setMltMaxNumTokens(int $value): SolrQuery
```

Задає максимальну кількість токенів для аналізу у кожному прикладі поля документа, яке не зберігається за допомогою TermVector.

### Список параметрів

`value`

Максимальна кількість токенів для аналізу

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.