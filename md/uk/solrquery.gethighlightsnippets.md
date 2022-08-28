Повертає максимальну кількість виділених фрагментів для створення кожного поля

-   [« SolrQuery::getHighlightSimplePre](solrquery.gethighlightsimplepre.html)
    
-   [SolrQuery::getHighlightUsePhraseHighlighter »](solrquery.gethighlightusephrasehighlighter.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Повертає максимальну кількість виділених фрагментів для створення кожного поля
    

# SolrQuery::getHighlightSnippets

(PECL solr> = 0.9.2)

SolrQuery::getHighlightSnippets — Повертає максимальну кількість виділених фрагментів для створення кожного поля

### Опис

```methodsynopsis
public SolrQuery::getHighlightSnippets(string $field_override = ?): int
```

Повертає максимальну кількість виділених фрагментів для створення кожного поля. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає ціле число у разі успішного виконання та **`null`**, якщо значення не встановлено.