Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5

-   [« SolrQuery::setExpandQuery](solrquery.setexpandquery.html)
    
-   [SolrQuery::setExplainOther »](solrquery.setexplainother.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
    

# SolrQuery::setExpandRows

(PECL solr> = 2.2.0)

SolrQuery::setExpandRows — Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5

### Опис

```methodsynopsis
public SolrQuery::setExpandRows(int $value): SolrQuery
```

Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5

### Список параметрів

`value`

### Значення, що повертаються

[SolrQuery](class.solrquery.html)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.html) - Вмикає/вимикає компонент Expand
-   [SolrQuery::addExpandSortField()](solrquery.addexpandsortfield.html) - Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::removeExpandSortField()](solrquery.removeexpandsortfield.html) - Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::setExpandQuery()](solrquery.setexpandquery.html) - Встановлює параметр expand.q
-   [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.html) - Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
-   [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.html) - Видаляє запит розширеного фільтра