---
navigation:
  - solrquery.sethighlightsnippets.md: '« SolrQuery::setHighlightSnippets'
  - solrquery.setmlt.md: 'SolrQuery::setMlt »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightUsePhraseHighlighter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setHighlightUsePhraseHighlighter

(PECL solr >= 0.9.2)

SolrQuery::setHighlightUsePhraseHighlighter — Чи слід виділяти вирази лише тоді, коли вони з'являються у фразі запиту

### Опис

```methodsynopsis
public SolrQuery::setHighlightUsePhraseHighlighter(bool $flag): SolrQuery
```

Встановлює, чи слід використовувати SpanScorer для виділення виразів лише тоді, коли вони з'являються у фразі запиту документа.

### Список параметрів

`value`

Встановлює, чи слід використовувати SpanScorer для виділення виразів лише тоді, коли вони з'являються у фразі запиту документа.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
