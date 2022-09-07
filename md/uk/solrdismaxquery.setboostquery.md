---
navigation:
  - solrdismaxquery.setboostfunction.md: '« SolrDisMaxQuery::setBoostFunction'
  - solrdismaxquery.setminimummatch.md: 'SolrDisMaxQuery::setMinimumMatch »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setBoostQuery'
---
# SolrDisMaxQuery::setBoostQuery

(No version information available, might only be in Git)

SolrDisMaxQuery::setBoostQuery - Безпосередньо встановлює параметр запиту посилення (bq)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setBoostQuery(string $q): SolrDisMaxQuery
```

Задає параметр запиту посилення (bq).

### Список параметрів

`q`

Запит.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::setBoostQuery()****

```php
<?php
$dismaxQuery = new SolrDisMaxQuery("lucene");

$dismaxQuery->setBoostQuery('cat:electronics manu:local^2');
echo $dismaxQuery.PHP_EOL;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&bq=cat:electronics manu:local^2
```

### Дивіться також

-   [SolrDisMaxQuery::addBoostQuery()](solrdismaxquery.addboostquery.md) - Додає поле підвищення запиту зі значенням та необов'язковим посиленням (параметр bq)
-   [SolrDisMaxQuery::removeBoostQuery()](solrdismaxquery.removeboostquery.md) - Видаляє часткове підвищення запиту на ім'я поля (bq)
