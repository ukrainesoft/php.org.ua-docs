---
navigation:
  - memcache.replace.md: '« Memcache::replace'
  - memcache.setcompressthreshold.md: 'Memcache::setCompressThreshold »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::set'
---
# Memcache::set

(PECL memcache >= 0.2.0)

Memcache::set — Зберегти дані на сервері

### Опис

```methodsynopsis
Memcache::set(    string $key,    mixed $var,    int $flag = ?,    int $expire = ?): bool
```

**Memcache::set()** записує елемент зі значенням `var` на сервері memcache із зазначеним ключем `key`. Параметр `expire` задає час життя елемента. Якщо він дорівнює 0, то елемент ніколи не застаріє (але сервер memcached не гарантує, що елемент постійно зберігатиметься в кеші і він може бути видалений для звільнення місця для нових елементів). Ви можете використовувати константу **`MEMCACHE_COMPRESSED`** як значення для параметра `flag`якщо вам потрібно стиснення "на льоту" (використовується zlib).

> **Зауваження**
> 
> Пам'ятайте, що ресурси (наприклад, дескриптори файлів або підключень) не можуть бути збережені в кеші, тому що вони не можуть бути серіалізовані.

Також можна використовувати функцію **memcacheset()**

### Список параметрів

`key`

Ключ, з яким пов'язане значення елемента.

`var`

Змінна для збереження. Рядкові та числові значення зберігаються як є, інші типи серіалізуються.

`flag`

Використовуйте **`MEMCACHE_COMPRESSED`** для збереження елементів за допомогою стиснення (використовується zlib).

`expire`

Час життя елемент. Якщо дорівнює нулю, елемент ніколи не старіє. Також ви можете використовувати мітку часу Unix або число секунд, починаючи з поточного моменту, однак, у цьому випадку число секунд не може бути більше 2592000 (30 днів).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Memcache::set()****

```php
<?php
/* процедурное API */

/* подключение к серверу memcached */
$memcache_obj = memcache_connect('memcache_host', 11211);

/*
установить значение элемента с ключом 'var_key',
используя 0 в flag, без использования сжатия со
временем жизни 30 секунд
*/
memcache_set($memcache_obj, 'var_key', 'some variable', 0, 30);

echo memcache_get($memcache_obj, 'var_key');

?>
```

**Приклад #2 Приклад використання **Memcache::set()****

```php
<?php
/* объектно-ориентированное API */

$memcache_obj = new Memcache;

/* подключение к серверу memcached */
$memcache_obj->connect('memcache_host', 11211);

/*
установить значение элемента с ключом 'var_key',
используя сжатие "на лету" и временем жизни 50 секунд.
*/
$memcache_obj->set('var_key', 'some really big variable', MEMCACHE_COMPRESSED, 50);

echo $memcache_obj->get('var_key');

?>
```

### Дивіться також

-   [Memcache::add()](memcache.add.md) - Додати елемент із зазначеним ключем
-   [Memcache::replace()](memcache.replace.md) - Замінити значення наявного елемента
