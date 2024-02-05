---
navigation:
  - solrinputdocument.getchilddocumentscount.md: '« SolrInputDocument::getChildDocumentsCount'
  - solrinputdocument.getfieldboost.md: 'SolrInputDocument::getFieldBoost »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::getField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrInputDocument::getField

(PECL solr >= 0.9.2)

SolrInputDocument::getField — Отримує поле на ім'я

### Опис

```methodsynopsis
public SolrInputDocument::getField(string $fieldName): SolrDocumentField
```

Отримує поле у ​​документі.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає об'єкт SolrDocumentField у разі успішного виконання та \*\*`false`\*\*в случае возникновения ошибки.
