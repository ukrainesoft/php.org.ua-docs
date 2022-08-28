Повертає текст, який з'являється після виділеного виразу

-   [« SolrQuery::getHighlightRequireFieldMatch](solrquery.gethighlightrequirefieldmatch.html)
    
-   [SolrQuery::getHighlightSimplePre »](solrquery.gethighlightsimplepre.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Повертає текст, який з'являється після виділеного виразу
    

# SolrQuery::getHighlightSimplePost

(PECL solr> = 0.9.2)

SolrQuery::getHighlightSimplePost — Повертає текст, який з'являється після виділення.

### Опис

```methodsynopsis
public SolrQuery::getHighlightSimplePost(string $field_override = ?): string
```

Повертає текст, який з'являється після виділення. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено