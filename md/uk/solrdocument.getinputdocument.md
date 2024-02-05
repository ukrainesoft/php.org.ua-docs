---
navigation:
  - solrdocument.getfieldnames.md: '« SolrDocument::getFieldNames'
  - solrdocument.haschilddocuments.md: 'SolrDocument::hasChildDocuments »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::getInputDocument'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::getInputDocument

(PECL solr >= 0.9.2)

SolrDocument::getInputDocument — Повертає SolrInputDocument еквівалент об'єкту

### Опис

```methodsynopsis
public SolrDocument::getInputDocument(): SolrInputDocument
```

SolrInputDocument повертає еквівалент об'єкта. Це корисно, якщо потрібно повторно надіслати/оновити документ, отриманий із запиту.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає SolrInputDocument у разі успішного виконання та \*\*`null`\*\*в случае возникновения ошибки.
