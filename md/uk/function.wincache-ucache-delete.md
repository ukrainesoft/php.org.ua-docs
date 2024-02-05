---
navigation:
  - function.wincache-ucache-dec.md: « wincache\_ucache\_dec
  - function.wincache-ucache-exists.md: wincache\_ucache\_exists »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ucache\_delete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ucache\_delete

(PECL wincache >= 1.1.0)

wincache\_ucache\_delete — Видаляє змінні з кешу користувача.

### Опис

```methodsynopsis
wincache_ucache_delete(mixed $key): bool
```

Видаляє елементи з кешу користувача, на які вказує параметр `key`

### Список параметрів

`key`

Параметр`key`, який використовувався для зберігання змінної в кеші . `key`чувствителен к регистру`key` може бути масивом ключів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

Якщо параметр `key` є масивом, функція повертає **`false`**, якщо не вдається видалити кожен елемент масиву з кешу користувача, в іншому випадку повертається масив, що складається з усіх видалених ключів.

### Приклади

**Приклад #1 Приклад використання** wincache\_ucache\_delete()**с`key` у вигляді рядка**

```php
<?php
wincache_ucache_set('foo', 'bar');
var_dump(wincache_ucache_delete('foo'));
var_dump(wincache_ucache_exists('foo'));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

**Приклад #2 Приклад використання** wincache\_ucache\_delete()**с`key` у вигляді масиву**

```php
<?php
$array1 = array('green' => '5', 'blue' => '6', 'yellow' => '7', 'cyan' => '8');
wincache_ucache_set($array1);
$array2 = array('green', 'blue', 'yellow', 'cyan');
var_dump(wincache_ucache_delete($array2));
?>
```

Результат виконання наведеного прикладу:

```
array(4) { [0]=> string(5) "green"
           [1]=> string(4) "Blue"
           [2]=> string(6) "yellow"
           [3]=> string(4) "cyan" }
```

**Приклад #3 Приклад використання** wincache\_ucache\_delete()**с`key` у вигляді масиву, з якого не можна видалити деякі елементи**

```php
<?php
$array1 = array('green' => '5', 'blue' => '6', 'yellow' => '7', 'cyan' => '8');
wincache_ucache_set($array1);
$array2 = array('orange', 'red', 'yellow', 'cyan');
var_dump(wincache_ucache_delete($array2));
?>
```

Результат виконання наведеного прикладу:

```
array(2) { [0]=> string(6) "yellow"
           [1]=> string(4) "cyan" }
```

### Дивіться також

-   [wincache\_ucache\_set()](function.wincache-ucache-set.md) \- Додає змінну в кеш користувача і перезаписує змінну, якщо вона вже існує в кеші
-   [wincache\_ucache\_add()](function.wincache-ucache-add.md) \- Додає змінну в кеш користувача, тільки якщо змінна ще не існує в кеші
-   [wincache\_ucache\_get()](function.wincache-ucache-get.md) \- Отримує змінну, що зберігається в користувальницькому кеші
-   [wincache\_ucache\_clear()](function.wincache-ucache-clear.md) \- Видаляє весь вміст користувальницького кешу
-   [wincache\_ucache\_exists()](function.wincache-ucache-exists.md) \- Перевіряє, чи існує змінна в кеші користувача
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
