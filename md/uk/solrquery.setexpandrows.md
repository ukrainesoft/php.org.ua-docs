---
navigation:
  - solrquery.setexpandquery.md: '« SolrQuery::setExpandQuery'
  - solrquery.setexplainother.md: 'SolrQuery::setExplainOther »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setExpandRows'
---
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

[SolrQuery](class.solrquery.md)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.md) - Вмикає/вимикає компонент Expand
-   [SolrQuery::addExpandSortField()](solrquery.addexpandsortfield.md) - Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::removeExpandSortField()](solrquery.removeexpandsortfield.md) - Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::setExpandQuery()](solrquery.setexpandquery.md) - Встановлює параметр expand.q
-   [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.md) - Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
-   [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.md) - Видаляє запит розширеного фільтра
