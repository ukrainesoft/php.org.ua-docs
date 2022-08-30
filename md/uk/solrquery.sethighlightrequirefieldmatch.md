Вимагати зіставлення полів при виділенні

-   [« SolrQuery::setHighlightRegexSlop](solrquery.sethighlightregexslop.html)
    
-   [SolrQuery::setHighlightSimplePost »](solrquery.sethighlightsimplepost.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Вимагати зіставлення полів при виділенні
    

# SolrQuery::setHighlightRequireFieldMatch

(PECL solr> = 0.9.2)

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