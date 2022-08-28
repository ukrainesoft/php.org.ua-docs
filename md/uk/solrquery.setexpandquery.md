Встановлює параметр expand.q

-   [« SolrQuery::setExpand](solrquery.setexpand.html)
    
-   [SolrQuery::setExpandRows »](solrquery.setexpandrows.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Встановлює параметр expand.q
    

# SolrQuery::setExpandQuery

(PECL solr> = 2.2.0)

SolrQuery::setExpandQuery — Встановлює параметр expand.q

### Опис

```methodsynopsis
public SolrQuery::setExpandQuery(string $q): SolrQuery
```

Встановлює параметр expand.q

Перевизначає основний параметр q, визначає, які документи включити до основної групи.

### Список параметрів

`q`

### Значення, що повертаються

[SolrQuery](class.solrquery.html)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.html) - Вмикає/вимикає компонент Expand
-   [SolrQuery::addExpandSortField()](solrquery.addexpandsortfield.html) - Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::removeExpandSortField()](solrquery.removeexpandsortfield.html) - Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::setExpandRows()](solrquery.setexpandrows.html) - Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.html) - Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
-   [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.html) - Видаляє запит розширеного фільтра