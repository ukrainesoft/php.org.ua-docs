---
navigation:
  - function.wincache-ucache-cas.md: « wincache\_ucache\_cas
  - function.wincache-ucache-dec.md: wincache\_ucache\_dec »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ucache\_clear
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ucache\_clear

(PECL wincache >= 1.1.0)

wincache\_ucache\_clear — Видаляє весь вміст кешу користувача.

### Опис

```methodsynopsis
wincache_ucache_clear(): bool
```

Очищає/видалює всі значення, що зберігаються в кеші користувача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** wincache\_ucache\_clear()\*\*\*\*

```php
<?php
wincache_ucache_set('green', 1);
wincache_ucache_set('red', 2);
wincache_ucache_set('orange', 4);
wincache_ucache_set('blue', 8);
wincache_ucache_set('cyan', 16);
$array1 = array('green', 'red', 'orange', 'blue', 'cyan');
var_dump(wincache_ucache_get($array1));
var_dump(wincache_ucache_clear());
var_dump(wincache_ucache_get($array1));
?>
```

Результат виконання наведеного прикладу:

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

-   [wincache\_ucache\_set()](function.wincache-ucache-set.md) \- Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincache\_ucache\_add()](function.wincache-ucache-add.md) \- Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші
-   [wincache\_ucache\_delete()](function.wincache-ucache-delete.md) \- Видаляє змінні з користувальницького кешу
-   [wincache\_ucache\_get()](function.wincache-ucache-get.md) \- Отримує змінну, що зберігається в користувальницькому кеші
-   [wincache\_ucache\_exists()](function.wincache-ucache-exists.md) \- Перевіряє, чи існує змінна в кеші користувача
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
