---
navigation:
  - solrdocument.set.md: '« SolrDocument::\_\_set'
  - solrdocument.toarray.md: 'SolrDocument::toArray »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::sort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::sort

(PECL solr >= 0.9.2)

SolrDocument::sort — Сортує поля в документі

### Опис

```methodsynopsis
public SolrDocument::sort(int $sortOrderBy, int $sortDirection = SolrDocument::SORT_ASC): bool
```

Поля упорядковані відповідно до зазначених критеріїв та напряму сортування.

Поля можуть бути відсортовані за значеннями підвищення, іменами полів та кількістю значень.

Параметр sortOrderBy повинен бути одним з:

\*SolrDocument::SORT\_FIELD\_NAME\*SolrDocument::SORT\_FIELD\_BOOST\_VALUE\*SolrDocument::SORT\_FIELD\_VALUE\_COUNT

Напрямок sortDirection може бути одним з :

\*SolrDocument::SORT\_DEFAULT\*SolrDocument::SORT\_ASC\*SolrDocument::SORT\_DESC

Спосіб за замовчуванням - сортування у порядку зростання.

### Список параметрів

`sortOrderBy`

Критерій сортування.

`sortDirection`

Напрямок сортування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
