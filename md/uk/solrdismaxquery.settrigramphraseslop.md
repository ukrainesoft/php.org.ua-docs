Встановлює коефіцієнт відхилення триграми фрази (параметр ps3)

-   [« SolrDisMaxQuery::setTrigramPhraseFields](solrdismaxquery.settrigramphrasefields.html)
    
-   [SolrDisMaxQuery::setUserFields »](solrdismaxquery.setuserfields.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Встановлює коефіцієнт відхилення триграми фрази (параметр ps3)
    

# SolrDisMaxQuery::setTrigramPhraseSlop

(No version information available, might only be in Git)

SolrDisMaxQuery::setTrigramPhraseSlop — Встановлює коефіцієнт відхилення триграми фрази (параметр ps3)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setTrigramPhraseSlop(string $slop): SolrDisMaxQuery
```

Встановлює коефіцієнт відхилення триграм фрази (параметр ps3).

### Список параметрів

`slop`

Коефіцієнт відхилення.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::setTrigramPhraseSlop()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery->setTrigramPhraseSlop(2);
echo $dismaxQuery.PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&ps3=2
```

### Дивіться також

-   [SolrDisMaxQuery::addTrigramPhraseField()](solrdismaxquery.addtrigramphrasefield.html) - Додає поле триграми (параметр pf3)
-   [SolrDisMaxQuery::removeTrigramPhraseField()](solrdismaxquery.removetrigramphrasefield.html) - Видаляє поле триграми (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseFields()](solrdismaxquery.settrigramphrasefields.html) - Безпосередньо встановлює поля триграм фрази (параметр pf3)