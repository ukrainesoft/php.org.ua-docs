---
navigation:
  - solrdismaxquery.removephrasefield.md: '« SolrDisMaxQuery::removePhraseField'
  - solrdismaxquery.removetrigramphrasefield.md: 'SolrDisMaxQuery::removeTrigramPhraseField »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'Solr DisMax Query::remove Query Field'
---
# Solr DisMax Query::remove Query Field

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

**Приклад #1 Приклад використання **Solr DisMax Query::remove Query Field()****

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

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&qf=first^3 second^0.2 cat
q=lucene&defType=edismax&qf=first^3 cat
```

### Дивіться також

-   [SolrDisMaxQuery::addQueryField()](solrdismaxquery.addqueryfield.md) - Додає поле запиту із необов'язковим підвищенням (параметр qf)
