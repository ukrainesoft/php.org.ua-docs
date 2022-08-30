Перевизначає запит основного фільтра, визначає, які документи включити до основної групи

-   [« SolrQuery](class.solrquery.md)
    
-   [SolrQuery::addExpandSortField »](solrquery.addexpandsortfield.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
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

[SolrQuery](class.solrquery.md)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.md) - Вмикає/вимикає компонент Expand
-   [SolrQuery::addExpandSortField()](solrquery.addexpandsortfield.md) - Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::removeExpandSortField()](solrquery.removeexpandsortfield.md) - Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::setExpandRows()](solrquery.setexpandrows.md) - Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::setExpandQuery()](solrquery.setexpandquery.md) - Встановлює параметр expand.q
-   [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.md) - Видаляє запит розширеного фільтра