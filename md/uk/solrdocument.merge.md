---
navigation:
  - solrdocument.key.md: '« SolrDocument::key'
  - solrdocument.next.md: 'SolrDocument::next »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::merge'
---
# SolrDocument::merge

(PECL solr> = 0.9.2)

SolrDocument::merge — Зливає джерело в поточний SolrDocument

### Опис

```methodsynopsis
public SolrDocument::merge(SolrDocument $sourceDoc, bool $overwrite = true): bool
```

Зливає джерело у поточний SolrDocument.

### Список параметрів

`sourceDoc`

Початковий документ.

`overwrite`

Якщо вказано **`true`**, тоді поля з тим самим ім'ям у цільовому документі будуть перезаписані.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
