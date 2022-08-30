Встановлює функцію посилення (параметр bf)

-   [« SolrDisMaxQuery::setBigramPhraseSlop](solrdismaxquery.setbigramphraseslop.md)
    
-   [SolrDisMaxQuery::setBoostQuery »](solrdismaxquery.setboostquery.md)
    
-   [PHP Manual](index.md)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.md)
    
-   Встановлює функцію посилення (параметр bf)
    

# SolrDisMaxQuery::setBoostFunction

(No version information available, might only be in Git)

SolrDisMaxQuery::setBoostFunction - Встановлює функцію посилення (параметр bf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setBoostFunction(string $function): SolrDisMaxQuery
```

Встановлює функцію посилення (параметр bf)

Функції (з необов'язковими посиленнями), які будуть включені до запиту користувача, щоб вплинути на оцінку. Можна використовувати будь-яку функцію, що спочатку підтримується Solr, разом зі значенням підвищення, наприклад:

recip(rord(myfield),1,2,3)^1.5

### Список параметрів

`function`

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::setBoostFunction()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');

$boostRecentDocsFunction = "recip(ms(NOW,mydatefield),3.16e-11,1,1)";
$dismaxQuery->setBoostFunction($boostRecentDocsFunction);

echo $dismaxQuery.PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&bf=recip(ms(NOW,mydatefield),3.16e-11,1,1)
```