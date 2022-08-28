Встановлює альтернативний запит (параметр q.alt)

-   [« SolrDisMaxQuery::setPhraseSlop](solrdismaxquery.setphraseslop.html)
    
-   [SolrDisMaxQuery::setQueryPhraseSlop »](solrdismaxquery.setqueryphraseslop.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Встановлює альтернативний запит (параметр q.alt)
    

# SolrDisMaxQuery::setQueryAlt

(No version information available, might only be in Git)

SolrDisMaxQuery::setQueryAlt — Встановлює альтернативний запит (параметр q.alt)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setQueryAlt(string $q): SolrDisMaxQuery
```

Встановлює альтернативний запит (параметр q.alt).

Коли основний параметр *до* не вказаний чи порожній. Використовується параметр *q.alt*

### Список параметрів

`q`

Рядок запиту.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::setQueryAlt()****

```php
<?php

$dismaxQuery = new DisMaxQuery();
$dismaxQuery->setQueryAlt('*:*');

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
defType=edismax&q.alt=*:*&q=
```