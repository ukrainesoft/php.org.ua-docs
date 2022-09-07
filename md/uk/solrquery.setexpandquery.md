---
navigation:
  - solrquery.setexpand.md: '« SolrQuery::setExpand'
  - solrquery.setexpandrows.md: 'SolrQuery::setExpandRows »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setExpandQuery'
---
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

[SolrQuery](class.solrquery.md)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.md) - Вмикає/вимикає компонент Expand
-   [SolrQuery::addExpandSortField()](solrquery.addexpandsortfield.md) - Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::removeExpandSortField()](solrquery.removeexpandsortfield.md) - Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::setExpandRows()](solrquery.setexpandrows.md) - Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.md) - Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
-   [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.md) - Видаляє запит розширеного фільтра
