---
navigation:
  - solrquery.sethighlightregexslop.md: '« SolrQuery::setHighlightRegexSlop'
  - solrquery.sethighlightsimplepost.md: 'SolrQuery::setHighlightSimplePost »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightRequireFieldMatch'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setHighlightRequireFieldMatch

(PECL solr >= 0.9.2)

SolrQuery::setHighlightRequireFieldMatch — Вимагати зіставлення полів при виділенні

### Опис

```methodsynopsis
public SolrQuery::setHighlightRequireFieldMatch(bool $flag): SolrQuery
```

Якщо \*\*`true`\*\*тоді поле буде виділено тільки в тому випадку, якщо запит відповідає цьому конкретному полю.

Буде працювати тільки якщо для SolrQuery::setHighlightUsePhraseHighlighter() встановлено значення **`true`**

### Список параметрів

`flag`

**`true`** або **`false`**

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
