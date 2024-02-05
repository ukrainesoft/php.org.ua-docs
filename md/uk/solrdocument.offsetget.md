---
navigation:
  - solrdocument.offsetexists.md: '« SolrDocument::offsetExists'
  - solrdocument.offsetset.md: 'SolrDocument::offsetSet »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::offsetGet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::offsetGet

(PECL solr >= 0.9.2)

SolrDocument::offsetGet — Отримує поле

### Опис

```methodsynopsis
public SolrDocument::offsetGet(string $fieldName): SolrDocumentField
```

Використовується для отримання поля, коли об'єкт розглядається як масив.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає об'єкт SolrDocumentFiel.
