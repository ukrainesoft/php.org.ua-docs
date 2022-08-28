Впорядковує документи у розширених групах (параметр expand.sort)

-   [« SolrQuery::addExpandFilterQuery](solrquery.addexpandfilterquery.html)
    
-   [SolrQuery::addFacetDateField »](solrquery.addfacetdatefield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Впорядковує документи у розширених групах (параметр expand.sort)
    

# SolrQuery::addExpandSortField

(PECL solr> = 2.2.0)

SolrQuery::addExpandSortField — Упорядкування документів у розширених групах (параметр expand.sort)

### Опис

```methodsynopsis
public SolrQuery::addExpandSortField(string $field, string $order = ?): SolrQuery
```

Впорядковує документи у розширених групах (параметр expand.sort).

### Список параметрів

`field`

Ім'я поля

`order`

Порядок ASC/DESC, використовуючи константи SolrQuery::ORDER

За замовчуванням: SolrQuery::ORDERDESC

### Значення, що повертаються

[SolrQuery](class.solrquery.html)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.html) - Вмикає/вимикає компонент Expand
-   [SolrQuery::removeExpandSortField()](solrquery.removeexpandsortfield.html) - Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::setExpandRows()](solrquery.setexpandrows.html) - Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::setExpandQuery()](solrquery.setexpandquery.html) - Встановлює параметр expand.q
-   [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.html) - Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
-   [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.html) - Видаляє запит розширеного фільтра