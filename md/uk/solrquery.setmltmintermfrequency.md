---
navigation:
  - solrquery.setmltmindocfrequency.md: '« SolrQuery::setMltMinDocFrequency'
  - solrquery.setmltminwordlength.md: 'SolrQuery::setMltMinWordLength »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setMltMinTermFrequency'
---
# SolrQuery::setMltMinTermFrequency

(PECL solr> = 0.9.2)

SolrQuery::setMltMinTermFrequency — Встановлює частоту, нижче за яку вирази будуть ігноруватися у вихідній документації

### Опис

```methodsynopsis
public SolrQuery::setMltMinTermFrequency(int $minTermFrequency): SolrQuery
```

Встановлює частоту, нижче за яку вирази ігноруватимуться у вихідній документації

### Список параметрів

`minTermFrequency`

Частота, нижче за яку вирази будуть ігноруватися у вихідній документації.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
