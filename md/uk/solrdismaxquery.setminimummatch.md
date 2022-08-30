Встановлює мінімальну відповідність "Should" (mm)

-   [« SolrDisMaxQuery::setBoostQuery](solrdismaxquery.setboostquery.md)
    
-   [SolrDisMaxQuery::setPhraseFields »](solrdismaxquery.setphrasefields.md)
    
-   [PHP Manual](index.md)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.md)
    
-   Встановлює мінімальну відповідність "Should" (mm)
    

# SolrDisMaxQuery::setMinimumMatch

(No version information available, might only be in Git)

SolrDisMaxQuery::setMinimumMatch - Встановлює мінімальну відповідність "Should" (mm)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setMinimumMatch(string $value): SolrDisMaxQuery
```

Встановлює параметр мінімальної відповідності "Should" (mm). Якщо оператор запиту за замовчуванням – AND (І), тоді mm = 100%, якщо оператор запиту за замовчуванням (q.op) – OR (АБО), то mm = 0%.

### Список параметрів

`value`

Мінімальне значення відповідності/вираз.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::setMinimumMatch()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
// 75% предложений запроса должны соответствовать
$dismaxQuery->setMinimumMatch("75%");
echo $dismaxQuery . PHP_EOL;
?>
```

Результат виконання цього прикладу:

```
q=lucene&defType=edismax&mm=75%
```