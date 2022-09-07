---
navigation:
  - solrinputdocument.setfieldboost.md: '« SolrInputDocument::setFieldBoost'
  - solrinputdocument.toarray.md: 'SolrInputDocument::toArray »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::sort'
---
# SolrInputDocument::sort

(PECL solr> = 0.9.2)

SolrInputDocument::sort — Сортує поля в документі

### Опис

```methodsynopsis
public SolrInputDocument::sort(int $sortOrderBy, int $sortDirection = SolrInputDocument::SORT_ASC): bool
```

Поля упорядковані відповідно до зазначених критеріїв та напряму сортування.

Поля можуть бути відсортовані за значеннями підвищення, іменами полів та кількістю значень.

Параметр $orderby повинен бути одним з :

SolrInputDocument::SORTFIELDNAME SolrInputDocument::SORTFIELDBOOSTVALUE SolrInputDocument::SORTFIELDVALUECOUNT

Напрямок сортування може бути одним з:

SolrInputDocument::SORTDEFAULT SolrInputDocument::SORTASC SolrInputDocument::SORTDESC

### Список параметрів

`sortOrderBy`

Критерій сортування

`sortDirection`

Напрямок сортування

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
