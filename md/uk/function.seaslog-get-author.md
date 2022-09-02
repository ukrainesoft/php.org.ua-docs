---
navigation:
  - ref.seaslog.md: « Функции Seaslog
  - function.seaslog-get-version.md: seasloggetversion »
  - index.md: PHP Manual
  - ref.seaslog.md: Функции Seaslog
title: seasloggetauthor
---
# seasloggetauthor

(PECL seaslog >=1.0.0)

seasloggetauthor — Отримує автора SeasLog

### Опис

```methodsynopsis
seaslog_get_author(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає автора SeasLog у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **seasloggetauthor()****

```php
<?php

var_dump(seaslog_get_author());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(29) "Chitao.Gao  [ neeke@php.net ]"
```
