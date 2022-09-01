---
navigation:
  - solrdismaxquery.removebigramphrasefield.md: '« SolrDisMaxQuery::removeBigramPhraseField'
  - solrdismaxquery.removephrasefield.md: 'SolrDisMaxQuery::removePhraseField »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::removeBoostQuery'
---
# SolrDisMaxQuery::removeBoostQuery

(No version information available, might only be in Git)

SolrDisMaxQuery::removeBoostQuery — Видаляє часткове підвищення запиту на ім'я поля (bq)

### Опис

```methodsynopsis
public SolrDisMaxQuery::removeBoostQuery(string $field): SolrDisMaxQuery
```

Видаляє частковий запит на підвищення з існуючого запиту, тільки якщо було виконано [SolrDisMaxQuery::addBoostQuery()](solrdismaxquery.addboostquery.md)

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::removeBoostQuery()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addBoostQuery('cat', 'electronics', 5.1)
    ->addBoostQuery('cat', 'hard drive')
;
echo $dismaxQuery.PHP_EOL;
// теперь удалите часть запроса с полем 'cat'
$dismaxQuery
->removeBoostQuery('cat');
echo $dismaxQuery . PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&bq=cat:electronics^5.1 cat:hard drive
q=lucene&defType=edismax&bq=cat:hard drive
```

### Дивіться також

-   [SolrDisMaxQuery::addBoostQuery()](solrdismaxquery.addboostquery.md) - Додає поле підвищення запиту зі значенням та необов'язковим посиленням (параметр bq)
-   [SolrDisMaxQuery::setBoostQuery()](solrdismaxquery.setboostquery.md) - безпосередньо встановлює параметр запиту посилення (bq)
