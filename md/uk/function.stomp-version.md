---
navigation:
  - function.stomp-connect-error.md: « stompconnecterror
  - class.stomp.md: Stomp »
  - index.md: PHP Manual
  - ref.stomp.md: Функции Stomp
title: stompversion
---
# stompversion

(PECL stomp >= 0.1.0)

stompversion — Повертає поточну версію модуля Stomp

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

**Приклад #1 Приклад використання **stompversion()****

```php
<?php

var_dump(stomp_version());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(5) "0.2.0"
```
