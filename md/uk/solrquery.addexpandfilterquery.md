Перевизначає запит основного фільтра, визначає, які документи включити до основної групи

-   [« SolrQuery](class.solrquery.html)
    
-   [SolrQuery::addExpandSortField »](solrquery.addexpandsortfield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
    

# SolrQuery::addExpandFilterQuery

(PECL solr> = 2.2.0)

SolrQuery::addExpandFilterQuery — Перевизначає запит основного фільтра, визначає, які документи включити до основної групи

### Опис

```methodsynopsis
public SolrQuery::addExpandFilterQuery(string $fq): SolrQuery
```

Перевизначає запит основного фільтра, визначає, які документи включити до основної групи.

### Список параметрів

`fq`

### Значення, що повертаються

[SolrQuery](class.solrquery.html)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.html) - Вмикає/вимикає компонент Expand
-   [SolrQuery::addExpandSortField()](solrquery.addexpandsortfield.html) - Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::removeExpandSortField()](solrquery.removeexpandsortfield.html) - Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::setExpandRows()](solrquery.setexpandrows.html) - Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::setExpandQuery()](solrquery.setexpandquery.html) - Встановлює параметр expand.q
-   [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.html) - Видаляє запит розширеного фільтра