Видаляє поле запиту (параметр qf)

-   [« SolrDisMaxQuery::removePhraseField](solrdismaxquery.removephrasefield.html)
    
-   [SolrDisMaxQuery::removeTrigramPhraseField »](solrdismaxquery.removetrigramphrasefield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Видаляє поле запиту (параметр qf)
    

# Solr DisMax Query::remove Query Field

(No version information available, might only be in Git)

SolrDisMaxQuery::removeQueryField — Видалення поля запиту (параметр qf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::removeQueryField(string $field): SolrDisMaxQuery
```

Видаляє поле запиту (параметр qf) зі списку полів, доданих за допомогою [SolrDisMaxQuery::addQueryField()](solrdismaxquery.addqueryfield.html)

qf: При створенні DisjunctionMaxQueries з запиту користувача він вказує поля для пошуку і збільшує їх кількість.

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::remove Query Field()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
    ->addQueryField('first', 3)
    ->addQueryField('second', 0.2)
    ->addQueryField('cat');
echo $dismaxQuery . PHP_EOL;
// удалите поле 'second'
echo $dismaxQuery->removeQueryField('second');
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&qf=first^3 second^0.2 cat
q=lucene&defType=edismax&qf=first^3 cat
```

### Дивіться також

-   [SolrDisMaxQuery::addQueryField()](solrdismaxquery.addqueryfield.html) - Додає поле запиту із необов'язковим підвищенням (параметр qf)