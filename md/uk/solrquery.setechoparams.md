---
navigation:
  - solrquery.setechohandler.md: '« SolrQuery::setEchoHandler'
  - solrquery.setexpand.md: 'SolrQuery::setExpand »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setEchoParams'
---
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
