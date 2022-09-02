---
navigation:
  - function.uopz-add-function.md: « uopzaddfunction
  - function.uopz-backup.md: uopzbackup »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzallowexit
---
# uopzallowexit

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzallowexit — Дозволяє керувати вимкненим опкодом exit

### Опис

```methodsynopsis
uopz_allow_exit(bool $allow): void
```

За замовчуванням uopz відключає опкод exit, тому дзвінки [exit()](function.exit.md) практично ігноруються . **uopzallowexit()** дозволяє контролювати цю поведінку.

### Список параметрів

`allow`

Дозволити виконання опкодів exit чи ні.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **uopzallowexit()****

```php
<?php
exit(1);
echo 1;
uopz_allow_exit(true);
exit(2);
echo 2;
?>
```

Результат виконання цього прикладу:

```
1
```

### Примітки

**Застереження**

[OPcache](book.opcache.md) оптимізує мертвий код після завершення.

### Дивіться також

-   [uopzgetexitstatus()](function.uopz-get-exit-status.md) - Отримати останній встановлений статус виходу
