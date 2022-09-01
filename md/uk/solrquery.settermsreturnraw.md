---
navigation:
  - solrquery.settermsprefix.md: '« SolrQuery::setTermsPrefix'
  - solrquery.settermssort.md: 'SolrQuery::setTermsSort »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setTermsReturnRaw'
---
# SolrQuery::setTermsReturnRaw

(PECL solr> = 0.9.2)

SolrQuery::setTermsReturnRaw — Повернути необроблені символи проіндексованого виразу

### Опис

```methodsynopsis
public SolrQuery::setTermsReturnRaw(bool $flag): SolrQuery
```

Якщо true, повертає необроблені символи проіндексованого виразу, незалежно від того, чи людиночитані вони.

### Список параметрів

`value`

**`true`** ор **`false`**

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
