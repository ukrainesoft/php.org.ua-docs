---
navigation:
  - function.get-cfg-var.md: « get\_cfg\_var
  - function.get-defined-constants.md: get\_defined\_constants »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: get\_current\_user
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_current\_user

(PHP 4, PHP 5, PHP 7, PHP 8)

get\_current\_user — Отримує ім'я власника поточного скрипту PHP

### Опис

```methodsynopsis
get_current_user(): string
```

Повертає ім'я власника поточного PHP-скрипту.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я користувача як рядок.

### Приклади

**Приклад #1 Приклад використання** get\_current\_user()\*\*\*\*

```php
<?php
echo 'Текущий владелец скрипта: ' . get_current_user();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Текущий владелец скрипта: SYSTEM
```

### Дивіться також

-   [getmyuid()](function.getmyuid.md) \- Отримання UID власника скрипта PHP
-   [getmygid()](function.getmygid.md) \- Отримати GID власника скрипта PHP
-   [getmypid()](function.getmypid.md) \- Отримання ID процесу PHP
-   [getmyinode()](function.getmyinode.md) \- Отримує значення inode поточного скрипту
-   [getlastmod()](function.getlastmod.md) \- Отримує час останньої модифікації сторінки
