---
navigation:
  - function.uopz-function.md: « uopz\_function
  - function.uopz-get-hook.md: uopz\_get\_hook »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_get\_exit\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_get\_exit\_status

(PECL uopz 5, PECL uopz , PECL uopz 7)

uopz\_get\_exit\_status — Отримати останній встановлений статус виходу

### Опис

```methodsynopsis
uopz_get_exit_status(): mixed
```

Отримує останній встановлений статус виходу, тобто значення, передане в [exit()](function.exit.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ця функція повертає останній статус виходу або **`null`**, якщо [exit()](function.exit.md) не було викликано.

### Приклади

**Приклад #1 Приклад використання** uopz\_get\_exit\_status()\*\*\*\*

```php
<?php
exit(123);
echo uopz_get_exit_status();?>
```

Результат виконання наведеного прикладу:

```
123
```

### Примітки

**Застереження**

[OPcache](book.opcache.md) оптимізує мертвий код після завершення.

### Дивіться також

-   [uopz\_allow\_exit()](function.uopz-allow-exit.md) \- Дозволяє керувати вимкненим опкодом exit
