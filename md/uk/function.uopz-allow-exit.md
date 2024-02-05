---
navigation:
  - function.uopz-add-function.md: « uopz\_add\_function
  - function.uopz-backup.md: uopz\_backup »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_allow\_exit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_allow\_exit

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_allow\_exit — Дозволяє керувати вимкненим опкодом exit

### Опис

```methodsynopsis
uopz_allow_exit(bool $allow): void
```

За замовчуванням uopz відключає опкод exit, тому дзвінки [exit()](function.exit.md) практично ігноруються . **uopz\_allow\_exit()** дозволяє контролювати цю поведінку.

### Список параметрів

`allow`

Дозволити виконання опкодів exit чи ні.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** uopz\_allow\_exit()\*\*\*\*

```php
<?php
exit(1);
echo 1;
uopz_allow_exit(true);
exit(2);
echo 2;
?>
```

Результат виконання наведеного прикладу:

```
1
```

### Примітки

**Застереження**

[OPcache](book.opcache.md) оптимізує мертвий код після завершення.

### Дивіться також

-   [uopz\_get\_exit\_status()](function.uopz-get-exit-status.md) \- Отримати останній встановлений статус виходу
