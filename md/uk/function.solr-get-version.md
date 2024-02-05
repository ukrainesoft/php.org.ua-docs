---
navigation:
  - ref.solr.md: « Функції Solr
  - solr.examples.md: Приклади »
  - index.md: PHP Manual
  - ref.solr.md: Функції Solr
title: solr\_get\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# solr\_get\_version

(PECL solr >= 0.9.1)

solr\_get\_version — Повертає поточну версію Apache Solr

### Опис

```methodsynopsis
solr_get_version(): string
```

Функція повертає поточну версію модуля у вигляді рядка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок у разі успішного виконання та \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Функція не викидає помилок чи винятків.

### Приклади

**Пример #1 Пример использования**solr\_get\_version()\*\*\*\*

```php
<?php

$solr_version = solr_get_version();

print $solr_version;

?>
```

Висновок наведеного прикладу буде схожим на:

```
0.9.6
```

### Дивіться також

-   [SolrUtils::getSolrVersion()](solrutils.getsolrversion.md) \- Повертає поточну версію модуля Solr
