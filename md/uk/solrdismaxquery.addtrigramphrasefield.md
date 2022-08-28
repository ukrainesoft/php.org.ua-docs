Додає поле триграми (параметр pf3)

-   [« SolrDisMaxQuery::addQueryField](solrdismaxquery.addqueryfield.html)
    
-   [SolrDisMaxQuery::addUserField »](solrdismaxquery.adduserfield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Додає поле триграми (параметр pf3)
    

# SolrDisMaxQuery::addTrigramPhraseField

(No version information available, might only be in Git)

SolrDisMaxQuery::addTrigramPhraseField — Додає поле триграми (параметр pf3)

### Опис

```methodsynopsis
public SolrDisMaxQuery::addTrigramPhraseField(string $field, string $boost, string $slop = ?): SolrDisMaxQuery
```

Додає поле триграми (параметр pf3)

### Список параметрів

`field`

Ім'я поля

`boost`

Поле Boost

`slop`

Поле Slop

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::addTrigramPhraseField()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
->addTrigramPhraseField('cat', 2, 5.1)
->addTrigramPhraseField('feature', 4.5)
;
echo $dismaxQuery.PHP_EOL;

?>
```

Результат виконання цього прикладу:

```
q=lucene&defType=%s&pf3=cat~5.1^2 feature^4.5
```

### Дивіться також

-   [SolrDisMaxQuery::removeTrigramPhraseField()](solrdismaxquery.removetrigramphrasefield.html) - Видаляє поле триграми (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseFields()](solrdismaxquery.settrigramphrasefields.html) - Безпосередньо встановлює поля триграм фрази (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseSlop()](solrdismaxquery.settrigramphraseslop.html) - Встановлює коефіцієнт відхилення триграми фрази (параметр PS3)