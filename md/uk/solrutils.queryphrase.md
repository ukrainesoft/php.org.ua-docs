---
navigation:
  - solrutils.getsolrversion.md: '« SolrUtils::getSolrVersion'
  - class.solrinputdocument.md: SolrInputDocument »
  - index.md: PHP Manual
  - class.solrutils.md: SolrUtils
title: 'SolrUtils::queryPhrase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrUtils::queryPhrase

(PECL solr >= 0.9.2)

SolrUtils::queryPhrase — Підготовка фрази з неекранованого рядка запиту Lucene

### Опис

```methodsynopsis
public static SolrUtils::queryPhrase(string $str): string
```

Підготовка фрази з неекранованого рядка запиту Lucene.

### Список параметрів

`str`

Рядок запиту Lucene.

### Значення, що повертаються

Повертає рядок запиту, поданий у подвійні лапки.
