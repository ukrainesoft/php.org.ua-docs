---
navigation:
  - function.wincache-ucache-cas.md: « wincacheucachecas
  - function.wincache-ucache-dec.md: wincacheucachedec »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincacheucacheclear
---
# wincacheucacheclear

(PECL wincache >= 1.1.0)

wincacheucacheclear — Видаляє весь вміст кешу користувача.

### Опис

```methodsynopsis
wincache_ucache_clear(): bool
```

Очищає/видалює всі значення, що зберігаються в кеші користувача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **wincacheucacheclear()****

```php
<?php
wincache_ucache_set('green', 1);
wincache_ucache_set('red', 2);
wincache_ucache_set('orange', 4);
wincache_ucache_set('blue', 8);
wincache_ucache_set('cyan', 16);
$array1 = array('green', 'red', 'orange', 'blue', 'cyan');
var_dump(wincache_ucache_get($array1));
var_dump(wincache_ucache_clear());
var_dump(wincache_ucache_get($array1));
?>
```

Результат виконання цього прикладу:

```
array(5) { ["green"]=> int(1)
           ["red"]=> int(2)
           ["orange"]=> int(4)
           ["blue"]=> int(8)
           ["cyan"]=> int(16) }
bool(true)
bool(false)
```

### Дивіться також

-   [wincacheucacheset()](function.wincache-ucache-set.md) - Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincacheucacheadd()](function.wincache-ucache-add.md) - Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші
-   [wincacheucachedelete()](function.wincache-ucache-delete.md) - Видаляє змінні з користувальницького кешу
-   [wincacheucacheget()](function.wincache-ucache-get.md) - Отримує змінну, що зберігається в користувальницькому кеші
-   [wincacheucacheexists()](function.wincache-ucache-exists.md) - Перевіряє, чи існує змінна в користувальницькому кеші
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.md) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.md) - Отримує інформацію про дані, що зберігаються в кеші користувача
