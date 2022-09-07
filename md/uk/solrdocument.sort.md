---
navigation:
  - solrdocument.set.md: '« SolrDocument::set'
  - solrdocument.toarray.md: 'SolrDocument::toArray »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::sort'
---
# SolrDocument::sort

(PECL solr> = 0.9.2)

SolrDocument::sort — Сортує поля в документі

### Опис

```methodsynopsis
public SolrDocument::sort(int $sortOrderBy, int $sortDirection = SolrDocument::SORT_ASC): bool
```

Поля упорядковані відповідно до зазначених критеріїв та напряму сортування.

Поля можуть бути відсортовані за значеннями підвищення, іменами полів та кількістю значень.

Параметр sortOrderBy повинен бути одним з:

SolrDocument::SORTFIELDNAME SolrDocument::SORTFIELDBOOSTVALUE SolrDocument::SORTFIELDVALUECOUNT

Напрямок sortDirection може бути одним з :

SolrDocument::SORTDEFAULT SolrDocument::SORTASC SolrDocument::SORTDESC

Спосіб за замовчуванням - сортування у порядку зростання.

### Список параметрів

`sortOrderBy`

Критерій сортування.

`sortDirection`

Напрямок сортування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
