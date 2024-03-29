---
navigation:
  - memcached.quit.md: '« Memcached::quit'
  - memcached.replacebykey.md: 'Memcached::replaceByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::replace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::replace

(PECL memcached >= 0.1.0)

Memcached::replace — Замінює існуючий запис із зазначеним ключем

### Опис

```methodsynopsis
public Memcached::replace(string $key, mixed $value, int $expiration = 0): bool
```

\*\*Memcached::replace()\*\*похож на метод[Memcached::set()](memcached.set.md), але операція завершиться невдачею у випадку, якщо ключ `key` відсутня на сервері.

### Список параметрів

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Метод[Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTSTORED`** якщо вказаного ключа немає.

### Дивіться також

-   [Memcached::replaceByKey()](memcached.replacebykey.md) \- Замінює існуючий запис із заданим ключем на вказаному сервері
-   [Memcached::set()](memcached.set.md) \- Зберігає запис
-   [Memcached::add()](memcached.add.md) \- Додає елемент із новим ключем
