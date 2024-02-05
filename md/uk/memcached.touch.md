---
navigation:
  - memcached.setsaslauthdata.md: '« Memcached::setSaslAuthData'
  - memcached.touchbykey.md: 'Memcached::touchByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::touch'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::touch

(PECL memcached >= 2.0.0)

Memcached::touch — Встановлює новий термін зберігання для запису

### Опис

```methodsynopsis
public Memcached::touch(string $key, int $expiration = 0): bool
```

**Memcached::touch()** встановлює новий термін зберігання для запису із зазначеним ключем.

### Список параметрів

`key`

Ключ, під яким зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Используйте при необходимости[Memcached::getResultCode()](memcached.getresultcode.md)

### Дивіться також

-   [Memcached::touchByKey()](memcached.touchbykey.md) \- Встановлює новий термін зберігання для запису на вказаному сервері
