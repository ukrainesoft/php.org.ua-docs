---
navigation:
  - solrquery.sethighlightformatter.md: '« SolrQuery::setHighlightFormatter'
  - solrquery.sethighlightfragsize.md: 'SolrQuery::setHighlightFragsize »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightFragmenter'
---
# SolrQuery::setHighlightFragmenter

(PECL solr> = 0.9.2)

SolrQuery::setHighlightFragmenter — Встановлює генератор текстових фрагментів для виділеного тексту

### Опис

```methodsynopsis
public SolrQuery::setHighlightFragmenter(string $fragmenter, string $field_override = ?): SolrQuery
```

Задає генератор текстового фрагмента виділеного тексту.

### Список параметрів

`fragmenter`

Стандартний фрагментер – розрив. Інший варіант - регулярний вираз, який намагається створити фрагменти, схожі на певний регулярний вираз.

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
