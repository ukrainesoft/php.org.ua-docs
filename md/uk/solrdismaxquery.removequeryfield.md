---
navigation:
  - solrdismaxquery.removephrasefield.md: '« SolrDisMaxQuery::removePhraseField'
  - solrdismaxquery.removetrigramphrasefield.md: 'SolrDisMaxQuery::removeTrigramPhraseField »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::removeQueryField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::removeQueryField

(No version information available, might only be in Git)

SolrDisMaxQuery::removeQueryField — Видалення поля запиту (параметр qf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::removeQueryField(string $field): SolrDisMaxQuery
```

Видаляє поле запиту (параметр qf) зі списку полів, доданих за допомогою [SolrDisMaxQuery::addQueryField()](solrdismaxquery.addqueryfield.md)

qf: При створенні DisjunctionMaxQueries з запиту користувача він вказує поля для пошуку і збільшує їх кількість.

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Пример #1 Пример использования**SolrDisMaxQuery::removeQueryField()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
    ->addQueryField('first', 3)
    ->addQueryField('second', 0.2)
    ->addQueryField('cat');
echo $dismaxQuery . PHP_EOL;
// удалите поле 'second'
echo $dismaxQuery->removeQueryField('second');
?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&qf=first^3 second^0.2 cat
q=lucene&defType=edismax&qf=first^3 cat
```

### Дивіться також

-   [SolrDisMaxQuery::addQueryField()](solrdismaxquery.addqueryfield.md) \- Додає поле запиту із необов'язковим підвищенням (параметр qf)
