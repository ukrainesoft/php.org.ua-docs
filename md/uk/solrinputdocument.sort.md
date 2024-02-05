---
navigation:
  - solrinputdocument.setfieldboost.md: '« SolrInputDocument::setFieldBoost'
  - solrinputdocument.toarray.md: 'SolrInputDocument::toArray »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::sort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrInputDocument::sort

(PECL solr >= 0.9.2)

SolrInputDocument::sort — Сортує поля в документі

### Опис

```methodsynopsis
public SolrInputDocument::sort(int $sortOrderBy, int $sortDirection = SolrInputDocument::SORT_ASC): bool
```

Поля упорядковані відповідно до зазначених критеріїв та напряму сортування.

Поля можуть бути відсортовані за значеннями підвищення, іменами полів та кількістю значень.

Параметр $order\_by повинен бути одним з :

\*SolrInputDocument::SORT\_FIELD\_NAME\*SolrInputDocument::SORT\_FIELD\_BOOST\_VALUE\*SolrInputDocument::SORT\_FIELD\_VALUE\_COUNT

Напрямок сортування може бути одним з:

\*SolrInputDocument::SORT\_DEFAULT\*SolrInputDocument::SORT\_ASC\*SolrInputDocument::SORT\_DESC

### Список параметрів

`sortOrderBy`

Критерій сортування

`sortDirection`

Напрямок сортування

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
