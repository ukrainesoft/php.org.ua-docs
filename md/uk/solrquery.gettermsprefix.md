---
navigation:
  - solrquery.gettermsmincount.md: '« SolrQuery::getTermsMinCount'
  - solrquery.gettermsreturnraw.md: 'SolrQuery::getTermsReturnRaw »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getTermsPrefix'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getTermsPrefix

(PECL solr >= 0.9.2)

SolrQuery::getTermsPrefix — Повертає префікс виразу

### Опис

```methodsynopsis
public SolrQuery::getTermsPrefix(): string
```

Повертає префікс, яким повинні бути обмежені вирази, що збігаються. Обмежить збіги лише виразами, що починаються з префікса

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає рядок та **`null`**, якщо значення не встановлено.
