---
navigation:
  - class.memcached.md: « Memcached
  - memcached.addbykey.md: 'Memcached::addByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::add

(PECL memcached >= 0.1.0)

Memcached::add — Додає елемент із новим ключем

### Опис

```methodsynopsis
public Memcached::add(string $key, mixed $value, int $expiration = 0): bool
```

Метод\*\*Memcached::add()\*\*похож на[Memcached::set()](memcached.set.md), але операція додавання завершиться помилкою, якщо ключ `key` вже існує на сервері.

### Список параметрів

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Метод[Memcached::getResultCode()](memcached.getresultcode.md) повертає \*\*`Memcached::RES_NOTSTORED`\*\*якщо переданий ключ вже існує.

### Дивіться також

-   [Memcached::addByKey()](memcached.addbykey.md) \- Додає новий елемент на заданий сервер
-   [Memcached::set()](memcached.set.md) \- Зберігає запис
-   [Memcached::replace()](memcached.replace.md) \- Замінює існуючий запис із зазначеним ключем
