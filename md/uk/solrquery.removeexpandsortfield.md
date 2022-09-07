---
navigation:
  - solrquery.removeexpandfilterquery.md: '« SolrQuery::removeExpandFilterQuery'
  - solrquery.removefacetdatefield.md: 'SolrQuery::removeFacetDateField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::removeExpandSortField'
---
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

[SolrQuery](class.solrquery.md)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.md) - Вмикає/вимикає компонент Expand
-   [SolrQuery::addExpandSortField()](solrquery.addexpandsortfield.md) - Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::setExpandRows()](solrquery.setexpandrows.md) - Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::setExpandQuery()](solrquery.setexpandquery.md) - Встановлює параметр expand.q
-   [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.md) - Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
-   [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.md) - Видаляє запит розширеного фільтра
