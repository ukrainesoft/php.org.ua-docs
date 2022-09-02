---
navigation:
  - function.wincache-ucache-delete.md: « wincacheucachedelete
  - function.wincache-ucache-get.md: wincacheucacheget »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincacheucacheexists
---
# wincacheucacheexists

(PECL wincache >= 1.1.0)

wincacheucacheexists — Перевіряє, чи існує змінна в кеші користувача.

### Опис

```methodsynopsis
wincache_ucache_exists(string $key): bool
```

Перевіряє, чи існує змінна `key` у користувальницькому кеші чи ні.

### Список параметрів

`key`

Параметр `key`, який використовувався для зберігання змінної в кеші . `key` чутливий до регістру.

### Значення, що повертаються

Повертає **`true`**, якщо змінна з `key` існує, в іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **wincacheucacheexists()****

```php
<?php
if (!wincache_ucache_exists('green'))
    wincache_ucache_set('green', 1);
var_dump(wincache_ucache_exists('green'));
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [wincacheucacheset()](function.wincache-ucache-set.md) - Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincacheucacheadd()](function.wincache-ucache-add.md) - Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші
-   [wincacheucacheget()](function.wincache-ucache-get.md) - Отримує змінну, що зберігається в користувальницькому кеші
-   [wincacheucacheclear()](function.wincache-ucache-clear.md) - Видаляє весь вміст кешу користувача.
-   [wincacheucachedelete()](function.wincache-ucache-delete.md) - Видаляє змінні з користувальницького кешу
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.md) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.md) - Отримує інформацію про дані, що зберігаються в кеші користувача
