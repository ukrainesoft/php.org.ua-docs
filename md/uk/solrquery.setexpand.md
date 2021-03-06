- [« SolrQuery::setEchoParams](solrquery.setechoparams.md)
- [SolrQuery::setExpandQuery »](solrquery.setexpandquery.md)

- [PHP Manual](index.md)
- [SolrQuery](class.solrquery.md)
- Вмикає/вимикає компонент Expand

# SolrQuery::setExpand

(PECL solr \>= 2.2.0)

SolrQuery::setExpand — Вмикає/вимикає компонент Expand

### Опис

public **SolrQuery::setExpand**(bool `$value`):
[SolrQuery](class.solrquery.md)

Вмикає/вимикає компонент Expand.

### Список параметрів

`value`
Логічний прапор (так чи ні)

### Значення, що повертаються

[SolrQuery](class.solrquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrQuery::setExpand()****

`<?php$query = new SolrQuery('lucene');$query   ->setExpand(true) setExpandRows(50)   -> >addExpandFilterQuery('inStock:true')  ->addExpandSortField('score', SolrQuery::ORDER_DESC)   ->addExpandSortField('title', SolrQuery::

Результатом виконання цього прикладу буде щось подібне:

q=lucene&expand=true&expand.rows=50&expand.q=text:product&expand.fq=manu:apple&expand.fq=inStock:true&expand.sort=score desc,title asc

### Дивіться також

- [SolrQuery::addExpandSortField()](solrquery.addexpandsortfield.md) -
Впорядковує документи у розширених групах (параметр expand.sort)
- [SolrQuery::removeExpandSortField()](solrquery.removeexpandsortfield.md) -
Видаляє розширене поле сортування за допомогою параметра expand.sort
- [SolrQuery::setExpandRows()](solrquery.setexpandrows.md) -
Встановлює кількість рядків для відображення у кожній групі
(expand.rows). Типово 5
- [SolrQuery::setExpandQuery()](solrquery.setexpandquery.md) -
Встановлює параметр expand.q
- [SolrQuery::addExpandFilterQuery()](solrquery.addexpandfilterquery.md) -
Перевизначає запит основного фільтра, визначає, які документи
включити до основної групи
- [SolrQuery::removeExpandFilterQuery()](solrquery.removeexpandfilterquery.md) -
Видаляє запит розширеного фільтра
