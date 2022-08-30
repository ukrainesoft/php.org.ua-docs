Видаляє запит розширеного фільтра

-   [« SolrQuery::getTimeAllowed](solrquery.gettimeallowed.md)
    
-   [SolrQuery::removeExpandSortField »](solrquery.removeexpandsortfield.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Видаляє запит розширеного фільтра
    

# SolrQuery::removeExpandFilterQuery

(PECL solr> = 2.2.0)

SolrQuery::removeExpandFilterQuery — Видалення запиту розширеного фільтра

### Опис

```methodsynopsis
public SolrQuery::removeExpandFilterQuery(string $fq): SolrQuery
```

Видаляє запит на розширений фільтр.

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
-   [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.md) - Перевизначає запит основного фільтра, визначає, які документи включити до основної групи