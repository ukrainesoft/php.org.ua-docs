---
navigation:
  - ref.seaslog.md: « Функції Seaslog
  - function.seaslog-get-version.md: seaslog\_get\_version »
  - index.md: PHP Manual
  - ref.seaslog.md: Функції Seaslog
title: seaslog\_get\_author
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# seaslog\_get\_author

(PECL seaslog >=1.0.0)

seaslog\_get\_author — Отримує автора SeasLog

### Опис

```methodsynopsis
seaslog_get_author(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає автора SeasLog у вигляді рядка.

### Приклади

**Пример #1 Пример использования**seaslog\_get\_author()\*\*\*\*

```php
<?php

var_dump(seaslog_get_author());

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(29) "Chitao.Gao  [ neeke@php.net ]"
```
