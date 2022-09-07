---
navigation:
  - ref.solr.md: « Функции Solr
  - solr.examples.md: Приклади »
  - index.md: PHP Manual
  - ref.solr.md: Функции Solr
title: solrgetversion
---
# solrgetversion

(PECL solr> = 0.9.1)

solrgetversion — Повертає поточну версію Apache Solr

### Опис

```methodsynopsis
solr_get_version(): string
```

Функція повертає поточну версію модуля у вигляді рядка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`false`** у разі виникнення помилки.

### Помилки

Функція не викидає помилок чи винятків.

### Приклади

**Приклад #1 Приклад використання **solrgetversion()****

```php
<?php

$solr_version = solr_get_version();

print $solr_version;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
0.9.6
```

### Дивіться також

-   [SolrUtils::getSolrVersion()](solrutils.getsolrversion.md) - Повертає поточну версію модуля Solr
