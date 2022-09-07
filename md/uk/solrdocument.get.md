---
navigation:
  - solrdocument.fieldexists.md: '« SolrDocument::fieldExists'
  - solrdocument.getchilddocuments.md: 'SolrDocument::getChildDocuments »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::get'
---
# SolrDocument::get

(PECL solr> = 0.9.2)

SolrDocument::get — Доступ до поля як властивості

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
