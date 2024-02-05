---
navigation:
  - function.wincache-ucache-delete.md: « wincache\_ucache\_delete
  - function.wincache-ucache-get.md: wincache\_ucache\_get »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ucache\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ucache\_exists

(PECL wincache >= 1.1.0)

wincache\_ucache\_exists — Перевіряє, чи існує змінна в кеші користувача.

### Опис

```methodsynopsis
wincache_ucache_exists(string $key): bool
```

Перевіряє, чи існує змінна `key` у користувальницькому кеші чи ні.

### Список параметрів

`key`

Параметр`key`, який використовувався для зберігання змінної в кеші . `key`чувствителен к регистру.

### Значення, що повертаються

Повертає **`true`**, якщо змінна з `key` існує, в іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** wincache\_ucache\_exists()\*\*\*\*

```php
<?php
if (!wincache_ucache_exists('green'))
    wincache_ucache_set('green', 1);
var_dump(wincache_ucache_exists('green'));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [wincache\_ucache\_set()](function.wincache-ucache-set.md) \- Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincache\_ucache\_add()](function.wincache-ucache-add.md) \- Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші
-   [wincache\_ucache\_get()](function.wincache-ucache-get.md) \- Отримує змінну, що зберігається в користувальницькому кеші
-   [wincache\_ucache\_clear()](function.wincache-ucache-clear.md) \- Видаляє весь вміст користувальницького кешу
-   [wincache\_ucache\_delete()](function.wincache-ucache-delete.md) \- Видаляє змінні з користувальницького кешу
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
