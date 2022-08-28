Повертає мінімальну кількість полів аспектів, які мають бути включені у відповідь

-   [« SolrQuery::getFacetMethod](solrquery.getfacetmethod.html)
    
-   [SolrQuery::getFacetMissing »](solrquery.getfacetmissing.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Повертає мінімальну кількість полів аспектів, які мають бути включені у відповідь
    

# SolrQuery::getFacetMinCount

(PECL solr> = 0.9.2)

SolrQuery::getFacetMinCount — Повертає мінімальну кількість полів аспектів, які повинні бути включені у відповідь

### Опис

```methodsynopsis
public SolrQuery::getFacetMinCount(string $field_override = ?): int
```

Повертає мінімальну кількість полів аспектів, які мають бути включені у відповідь. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає ціле число у разі успішного виконання та **`null`**, якщо значення не встановлено