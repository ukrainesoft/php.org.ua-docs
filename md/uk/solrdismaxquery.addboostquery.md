---
navigation:
  - solrdismaxquery.addbigramphrasefield.md: '« SolrDisMaxQuery::addBigramPhraseField'
  - solrdismaxquery.addphrasefield.md: 'SolrDisMaxQuery::addPhraseField »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::addBoostQuery'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::addBoostQuery

(No version information available, might only be in Git)

SolrDisMaxQuery::addBoostQuery — Додає поле підвищення запиту зі значенням та необов'язковим посиленням (параметр bq)

### Опис

```methodsynopsis
public SolrDisMaxQuery::addBoostQuery(string $field, string $value, string $boost = ?): SolrDisMaxQuery
```

Додає поле для підвищення запиту зі значенням \[та підвищення\](параметр bq)

### Список параметрів

`field`

`value`

`boost`

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання** SolrDisMaxQuery::addBoostQuery()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addBoostQuery('cat', 'clothing', 2)
    ->addBoostQuery('cat', 'electronics', 5.1)
;
echo $dismaxQuery.PHP_EOL;
?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&bq=cat:clothing^2 cat:electronics^5.1
```

### Дивіться також

-   [SolrDisMaxQuery::removeBoostQuery()](solrdismaxquery.removeboostquery.md) \- Видаляє часткове підвищення запиту на ім'я поля (bq)
-   [SolrDisMaxQuery::setBoostQuery()](solrdismaxquery.setboostquery.md) \- безпосередньо встановлює параметр запиту посилення (bq)
