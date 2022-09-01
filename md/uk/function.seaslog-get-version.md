---
navigation:
  - function.seaslog-get-author.html: « seasloggetauthor
  - class.seaslog.md: SeasLog »
  - index.md: PHP Manual
  - ref.seaslog.md: Функции Seaslog
title: seasloggetversion
---
# seasloggetversion

(PECL seaslog >=1.0.0)

seasloggetversion — Отримує версію SeasLog

### Опис

```methodsynopsis
seaslog_get_version(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає версію SeasLog (SEASLOGVERSION) у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **seasloggetversion()****

```php
<?php

var_dump(seaslog_get_version());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(5) "1.8.4"
```
