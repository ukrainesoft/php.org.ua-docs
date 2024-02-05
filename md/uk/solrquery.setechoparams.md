---
navigation:
  - solrquery.setechohandler.md: '« SolrQuery::setEchoHandler'
  - solrquery.setexpand.md: 'SolrQuery::setExpand »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setEchoParams'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setEchoParams

(PECL solr >= 0.9.2)

SolrQuery::setEchoParams — Визначає, які параметри включати у відповідь

### Опис

```methodsynopsis
public SolrQuery::setEchoParams(string $type): SolrQuery
```

Вказує Solr, які параметри запиту мають бути включені у відповідь для цілей налагодження, допустимі значення:

\- none - не включати жодних параметрів запиту для налагодження

-   explicit - включити параметри, явно вказані клієнтом
-   all - включити всі параметри, які у цьому запиті, або явно вказані клієнтом, або неявні через конфігурацію обробника запитів.

### Список параметрів

`type`

Тип параметрів, що включаються

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
