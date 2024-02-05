---
navigation:
  - solrdocument.fieldexists.md: '« SolrDocument::fieldExists'
  - solrdocument.getchilddocuments.md: 'SolrDocument::getChildDocuments »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::\_\_get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::\_\_get

(PECL solr >= 0.9.2)

SolrDocument::\_\_get — Доступ до поля як властивості

### Опис

```methodsynopsis
public SolrDocument::__get(string $fieldName): SolrDocumentField
```

Магічний метод доступу до поля як властивості.

### Список параметрів

`fieldName`

Назва поля

### Значення, що повертаються

Повертає екземпляр SolrDocumentField.
