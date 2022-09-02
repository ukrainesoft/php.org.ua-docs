---
navigation:
  - solrquery.addgroupsortfield.md: '« SolrQuery::addGroupSortField'
  - solrquery.addmltfield.md: 'SolrQuery::addMltField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addHighlightField'
---
# SolrQuery::addHighlightField

(PECL solr> = 0.9.2)

SolrQuery::addHighlightField — Відповідає hl.fl

### Опис

```methodsynopsis
public SolrQuery::addHighlightField(string $field): SolrQuery
```

Відповідає hl.fl. Використовується, щоб вказати, що виділені фрагменти мають бути створені для певного поля.

### Список параметрів

`field`

Назва поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
