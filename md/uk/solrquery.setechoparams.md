Визначає, які параметри включати у відповідь

-   [« SolrQuery::setEchoHandler](solrquery.setechohandler.md)
    
-   [SolrQuery::setExpand »](solrquery.setexpand.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Визначає, які параметри включати у відповідь
    

# SolrQuery::setEchoParams

(PECL solr> = 0.9.2)

SolrQuery::setEchoParams — Визначає, які параметри включати у відповідь

### Опис

```methodsynopsis
public SolrQuery::setEchoParams(string $type): SolrQuery
```

Вказує Solr, які параметри запиту повинні бути включені у відповідь для цілей налагодження, допустимі значення:

none - не включати жодних параметрів запиту для налагодження

-   explicit - включити параметри, явно вказані клієнтом
-   all - включити всі параметри, які у цьому запиті, або явно вказані клієнтом, або неявні через конфігурацію обробника запитів.

### Список параметрів

`type`

Тип параметрів, що включаються

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.