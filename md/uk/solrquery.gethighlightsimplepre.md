Повертає текст, що з'являється перед виділеним виразом

-   [« SolrQuery::getHighlightSimplePost](solrquery.gethighlightsimplepost.md)
    
-   [SolrQuery::getHighlightSnippets »](solrquery.gethighlightsnippets.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Повертає текст, що з'являється перед виділеним виразом
    

# SolrQuery::getHighlightSimplePre

(PECL solr> = 0.9.2)

SolrQuery::getHighlightSimplePre — Повертає текст, який з'являється перед виділеним виразом

### Опис

```methodsynopsis
public SolrQuery::getHighlightSimplePre(string $field_override = ?): string
```

Повертає текст, що з'являється перед виділеним виразом. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено