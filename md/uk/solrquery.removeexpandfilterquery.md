Видаляє запит розширеного фільтра

-   [« SolrQuery::getTimeAllowed](solrquery.gettimeallowed.html)
    
-   [SolrQuery::removeExpandSortField »](solrquery.removeexpandsortfield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
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

[SolrQuery](class.solrquery.html)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.html) - Вмикає/вимикає компонент Expand
-   [SolrQuery::addExpandSortField()](solrquery.addexpandsortfield.html) - Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::removeExpandSortField()](solrquery.removeexpandsortfield.html) - Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::setExpandRows()](solrquery.setexpandrows.html) - Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::setExpandQuery()](solrquery.setexpandquery.html) - Встановлює параметр expand.q
-   [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.html) - Перевизначає запит основного фільтра, визначає, які документи включити до основної групи