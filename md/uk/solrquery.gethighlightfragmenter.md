Повертає генератор фрагментів тексту для виділеного тексту

-   [« SolrQuery::getHighlightFormatter](solrquery.gethighlightformatter.html)
    
-   [SolrQuery::getHighlightFragsize »](solrquery.gethighlightfragsize.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Повертає генератор фрагментів тексту для виділеного тексту
    

# SolrQuery::getHighlightFragmenter

(PECL solr> = 0.9.2)

SolrQuery::getHighlightFragmenter — Повертає генератор фрагментів тексту для виділеного тексту

### Опис

```methodsynopsis
public SolrQuery::getHighlightFragmenter(string $field_override = ?): string
```

Повертає генератор фрагментів тексту виділеного тексту. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено