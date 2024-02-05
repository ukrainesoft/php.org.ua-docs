---
navigation:
  - function.stomp-connect-error.md: « stomp\_connect\_error
  - class.stomp.md: Stomp »
  - index.md: PHP Manual
  - ref.stomp.md: Опції Stomp
title: stomp\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stomp\_version

(PECL stomp >= 0.1.0)

stomp\_version — Повертає поточну версію модуля Stomp

### Опис

```methodsynopsis
stomp_version(): string
```

Повертає рядок, який містить версію поточного модуля Stomp.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточну версію модуля Stomp

### Приклади

**Приклад #1 Приклад використання** stomp\_version()\*\*\*\*

```php
<?php

var_dump(stomp_version());

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(5) "0.2.0"
```
