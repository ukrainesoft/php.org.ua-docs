---
navigation:
  - memcache.flush.html: '« Memcache::flush'
  - memcache.getextendedstats.html: 'Memcache::getExtendedStats »'
  - index.html: PHP Manual
  - class.memcache.html: Memcache
title: 'Memcache::get'
---
# Memcache::get

(PECL memcache >= 0.2.0)

Memcache::get — Вийняти елемент із сервера

### Опис

```methodsynopsis
Memcache::get(string $key, int &$flags = ?): string
```

```methodsynopsis
Memcache::get(array $keys, array &$flags = ?): array
```

**Memcache::get()** повертає раніше збережений елемент із ключем `key`, якщо він на даний момент існує на сервері.

Ви можете передати масив ключів у **Memcache::get()**, щоб отримати масив елементів. Результуючий масив міститиме лише існуючі пари ключ-значення.

### Список параметрів

`key`

Ключ або масив ключів для читання.

`flags`

Якщо встановлено, прапори, отримані разом із значеннями, будуть записані в цей параметр. Це точно ті прапори, що і передані, наприклад в [Memcache::set()](memcache.set.md). Молодший байт значення зарезервований для внутрішнього використання pecl/memcache (наприклад, для індикації стиснення або серіалізації статусу).

### Значення, що повертаються

Повертає значення, пов'язане з ключем `key` або масив знайдених пар ключ-значення, якщо в `key` заданий масив. Повертає **`false`** у разі виникнення помилки або якщо вказаний ключ `key` не було знайдено чи є порожнім масивом.

### Приклади

**Приклад #1 Приклад використання **Memcache::get()****

```php
<?php

/* процедурное API */
$memcache_obj = memcache_connect('memcache_host', 11211);
$var = memcache_get($memcache_obj, 'some_key');

/* объектно-ориентированное API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
$var = $memcache_obj->get('some_key');

/*
Также в качестве параметра вы можете использовать Масив ключей.
Если элемент не будет найден, то в результирующий Масив просто не будет
включён этот ключ.
*/

/* процедурное API */
$memcache_obj = memcache_connect('memcache_host', 11211);
$var = memcache_get($memcache_obj, Array('some_key', 'another_key'));

/* объектно-ориентированное API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
$var = $memcache_obj->get(Array('some_key', 'second_key'));

?>
```
