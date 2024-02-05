---
navigation:
  - memcached.prependbykey.md: '« Memcached::prependByKey'
  - memcached.replace.md: 'Memcached::replace »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::quit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::quit

(PECL memcached >= 2.0.0)

Memcached::quit — Закриває всі відкриті з'єднання.

### Опис

```methodsynopsis
public Memcached::quit(): bool
```

**Memcached::quit()** закриває всі відкриті з'єднання із серверами memcache.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
