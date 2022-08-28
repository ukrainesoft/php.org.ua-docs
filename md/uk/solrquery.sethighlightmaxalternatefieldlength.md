Встановлює максимальну кількість символів поля для повернення

-   [« SolrQuery::setHighlightHighlightMultiTerm](solrquery.sethighlighthighlightmultiterm.html)
    
-   [SolrQuery::setHighlightMaxAnalyzedChars »](solrquery.sethighlightmaxanalyzedchars.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Встановлює максимальну кількість символів поля для повернення
    

# SolrQuery::setHighlightMaxAlternateFieldLength

(PECL solr> = 0.9.2)

SolrQuery::setHighlightMaxAlternateFieldLength — Встановлює максимальну кількість символів поля для повернення

### Опис

```methodsynopsis
public SolrQuery::setHighlightMaxAlternateFieldLength(int $fieldLength, string $field_override = ?): SolrQuery
```

Якщо SolrQuery::setHighlightAlternateField() було передано значення **`true`**, цей параметр вказує максимальну кількість символів поля для повернення

Будь-яке значення менше або 0 означає необмежене.

### Список параметрів

`fieldLength`

Довжина поля

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.