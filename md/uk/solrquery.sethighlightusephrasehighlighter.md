---
navigation:
  - solrquery.sethighlightsnippets.html: '« SolrQuery::setHighlightSnippets'
  - solrquery.setmlt.html: 'SolrQuery::setMlt »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
title: 'SolrQuery::setHighlightUsePhraseHighlighter'
---
# SolrQuery::setHighlightUsePhraseHighlighter

(PECL solr> = 0.9.2)

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
