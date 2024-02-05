---
navigation:
  - solrquery.settermsprefix.md: '« SolrQuery::setTermsPrefix'
  - solrquery.settermssort.md: 'SolrQuery::setTermsSort »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setTermsReturnRaw'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setTermsReturnRaw

(PECL solr >= 0.9.2)

SolrQuery::setTermsReturnRaw — Повернути необроблені символи проіндексованого виразу

### Опис

```methodsynopsis
public SolrQuery::setTermsReturnRaw(bool $flag): SolrQuery
```

Якщо true, повертає необроблені символи проіндексованого виразу, незалежно від того, чи людиночитані вони.

### Список параметрів

`value`

**`true`**or**`false`**

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
