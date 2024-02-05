---
navigation:
  - solrdismaxquery.removebigramphrasefield.md: '« SolrDisMaxQuery::removeBigramPhraseField'
  - solrdismaxquery.removephrasefield.md: 'SolrDisMaxQuery::removePhraseField »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::removeBoostQuery'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::removeBoostQuery

(No version information available, might only be in Git)

Solr DisMax Query::removeBoost Query — Видаляє часткове підвищення запиту на ім'я поля (bq)

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

**Пример #1 Пример использования**SolrDisMaxQuery::removeBoostQuery()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addBoostQuery('cat', 'electronics', 5.1)
    ->addBoostQuery('cat', 'hard drive')
;
echo $dismaxQuery.PHP_EOL;
// теперь удалите часть запроса с полем 'cat'
$dismaxQuery
->removeBoostQuery('cat');
echo $dismaxQuery . PHP_EOL;

?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&bq=cat:electronics^5.1 cat:hard drive
q=lucene&defType=edismax&bq=cat:hard drive
```

### Дивіться також

-   [SolrDisMaxQuery::addBoostQuery()](solrdismaxquery.addboostquery.md) \- Додає поле підвищення запиту зі значенням та необов'язковим посиленням (параметр bq)
-   [SolrDisMaxQuery::setBoostQuery()](solrdismaxquery.setboostquery.md) \- безпосередньо встановлює параметр запиту посилення (bq)
