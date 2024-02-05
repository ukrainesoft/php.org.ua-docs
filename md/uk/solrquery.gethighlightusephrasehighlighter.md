---
navigation:
  - solrquery.gethighlightsnippets.md: '« SolrQuery::getHighlightSnippets'
  - solrquery.getmlt.md: 'SolrQuery::getMlt »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightUsePhraseHighlighter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getHighlightUsePhraseHighlighter

(PECL solr >= 0.9.2)

SolrQuery::getHighlightUsePhraseHighlighter — Повертає стан параметра hl.usePhraseHighlighter

### Опис

```methodsynopsis
public SolrQuery::getHighlightUsePhraseHighlighter(): bool
```

Повертає, чи слід використовувати SpanScorer для виділення фразових виразів, лише коли вони з'являються у фразі запиту у документі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає логічне значення та **`null`**, якщо значення не встановлено.
