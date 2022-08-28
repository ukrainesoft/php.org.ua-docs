Видаляє розширене поле сортування за допомогою параметра expand.sort

-   [« SolrQuery::removeExpandFilterQuery](solrquery.removeexpandfilterquery.html)
    
-   [SolrQuery::removeFacetDateField »](solrquery.removefacetdatefield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Видаляє розширене поле сортування за допомогою параметра expand.sort
    

# SolrQuery::removeExpandSortField

(PECL solr> = 2.2.0)

SolrQuery::removeExpandSortField — Видалення розширеного поля сортування за допомогою параметра expand.sort

### Опис

```methodsynopsis
public SolrQuery::removeExpandSortField(string $field): SolrQuery
```

Видаляє розширене поле сортування за допомогою параметра expand.sort.

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrQuery](class.solrquery.html)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.html) - Вмикає/вимикає компонент Expand
-   [SolrQuery::addExpandSortField()](solrquery.addexpandsortfield.html) - Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::setExpandRows()](solrquery.setexpandrows.html) - Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::setExpandQuery()](solrquery.setexpandquery.html) - Встановлює параметр expand.q
-   [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.html) - Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
-   [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.html) - Видаляє запит розширеного фільтра