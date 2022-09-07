---
navigation:
  - solrinputdocument.reset.md: '« SolrInputDocument::reset'
  - solrinputdocument.setfieldboost.md: 'SolrInputDocument::setFieldBoost »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::setBoost'
---
# SolrInputDocument::setBoost

(PECL solr> = 0.9.2)

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
