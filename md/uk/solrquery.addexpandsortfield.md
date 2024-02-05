---
navigation:
  - solrquery.addexpandfilterquery.md: '« SolrQuery::addExpandFilterQuery'
  - solrquery.addfacetdatefield.md: 'SolrQuery::addFacetDateField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addExpandSortField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::addExpandSortField

(PECL solr >= 2.2.0)

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

Порядок ASC/DESC, використовуючи константи SolrQuery::ORDER\_\*

За замовчуванням: SolrQuery::ORDER\_DESC

### Значення, що повертаються

[SolrQuery](class.solrquery.md)

### Дивіться також

-   [SolrQuery::setExpand()](solrquery.setexpand.md) \- Вмикає/вимикає компонент Expand
-   [SolrQuery::removeExpandSortField()](solrquery.removeexpandsortfield.md) \- Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::setExpandRows()](solrquery.setexpandrows.md) \- Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::setExpandQuery()](solrquery.setexpandquery.md) \- Встановлює параметр expand.q
-   [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.md) \- Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
-   [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.md) \- Видаляє запит розширеного фільтра
