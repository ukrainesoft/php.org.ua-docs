Встановлює максимальну кількість виділених фрагментів для створення кожного поля

-   [« SolrQuery::setHighlightSimplePre](solrquery.sethighlightsimplepre.md)
    
-   [SolrQuery::setHighlightUsePhraseHighlighter »](solrquery.sethighlightusephrasehighlighter.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Встановлює максимальну кількість виділених фрагментів для створення кожного поля
    

# SolrQuery::setHighlightSnippets

(PECL solr> = 0.9.2)

SolrQuery::setHighlightSnippets — Встановлює максимальну кількість виділених фрагментів для створення кожного поля

### Опис

```methodsynopsis
public SolrQuery::setHighlightSnippets(int $value, string $field_override = ?): SolrQuery
```

Встановлює максимальну кількість виділених фрагментів для створення кожного поля

### Список параметрів

`value`

Максимальна кількість виділених фрагментів для створення для кожного поля

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.