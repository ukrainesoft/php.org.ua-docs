---
navigation:
  - function.seaslog-get-author.md: « seaslog\_get\_author
  - class.seaslog.md: SeasLog »
  - index.md: PHP Manual
  - ref.seaslog.md: Функції Seaslog
title: seaslog\_get\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# seaslog\_get\_version

(PECL seaslog >=1.0.0)

seaslog\_get\_version — Отримує версію SeasLog

### Опис

```methodsynopsis
seaslog_get_version(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає версію SeasLog (SEASLOG\_VERSION) у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання** seaslog\_get\_version()\*\*\*\*

```php
<?php

var_dump(seaslog_get_version());

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(5) "1.8.4"
```
