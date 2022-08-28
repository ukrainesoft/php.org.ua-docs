Використовувати SpanScorer для виділення виразів

-   [« SolrQuery::setHighlightFragsize](solrquery.sethighlightfragsize.html)
    
-   [SolrQuery::setHighlightMaxAlternateFieldLength »](solrquery.sethighlightmaxalternatefieldlength.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Використовувати SpanScorer для виділення виразів
    

# SolrQuery::setHighlightHighlightMultiTerm

(PECL solr> = 0.9.2)

SolrQuery::setHighlightHighlightMultiTerm — Використовувати SpanScorer для виділення виразів

### Опис

```methodsynopsis
public SolrQuery::setHighlightHighlightMultiTerm(bool $flag): SolrQuery
```

Використовувати SpanScorer для виділення фразових виразів лише тоді, коли вони з'являються у фразі запиту в документі.

### Список параметрів

`flag`

Чи слід використовувати SpanScorer для виділення фразових виразів лише тоді, коли вони з'являються у фразі запиту у документі.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.