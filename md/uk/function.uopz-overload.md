---
navigation:
  - function.uopz-implement.md: « uopz\_implement
  - function.uopz-redefine.md: uopz\_redefine »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_overload
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_overload

(PECL uopz 1, PECL uopz 2)

uopz\_overload — Перевантажити опкод VM

**Увага**

Ця функція була *ВИДАЛЕНО*в PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_overload(int $opcode, Callable $callable): void
```

Перевантажує певний `opcode` за допомогою функції користувача

### Список параметрів

`opcode`

Коректний опкод, дивіться константи для отримання опкодів, що підтримуються

`callable`

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**uopz\_overload()\*\*\*\*

```php
<?php
uopz_overload(ZEND_EXIT, function(){});

exit();
echo "Привет, Мир";
?>
```

Результат виконання наведеного прикладу:

```
Привет, Мир
```
