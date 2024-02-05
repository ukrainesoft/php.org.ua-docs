---
navigation:
  - solrinputdocument.reset.md: '« SolrInputDocument::reset'
  - solrinputdocument.setfieldboost.md: 'SolrInputDocument::setFieldBoost »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::setBoost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrInputDocument::setBoost

(PECL solr >= 0.9.2)

SolrInputDocument::setBoost — Встановлює значення підвищення документа

### Опис

```methodsynopsis
public SolrInputDocument::setBoost(float $documentBoostValue): bool
```

Встановлює значення підвищення документа.

### Список параметрів

`documentBoostValue`

Значення індексу часу документа.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
