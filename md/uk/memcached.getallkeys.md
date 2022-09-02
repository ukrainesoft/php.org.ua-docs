---
navigation:
  - memcached.get.md: '« Memcached::get'
  - memcached.getbykey.md: 'Memcached::getByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::getAllKeys'
---
# Memcached::getAllKeys

(PECL memcached >= 2.0.0)

Memcached::getAllKeys — Отримує всі ключі, що зберігаються на серверах

### Опис

```methodsynopsis
public Memcached::getAllKeys(): array|false
```

**Memcached::getAllKeys()** відправляє запит на кожен сервер і отримує масив усіх ключів, що зберігаються на ньому в даний момент. Це не атомарна операція, тому це не по-справжньому несуперечливий знімок ключів в даний момент часу. Memcache не може гарантувати повернення всіх ключів, ви також не можете покладатися на те, що всі ключі повернуто.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає список ключів, що зберігаються на всіх серверах у разі успішного виконання або **`false`** у разі виникнення помилки.
