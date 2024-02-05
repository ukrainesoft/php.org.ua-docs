---
navigation:
  - memcached.decrementbykey.md: '« Memcached::decrementByKey'
  - memcached.deletebykey.md: 'Memcached::deleteByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::delete'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::delete

(PECL memcached >= 0.1.0)

Memcached::delete — Видаляє запис

### Опис

```methodsynopsis
public Memcached::delete(string $key, int $time = 0): bool
```

Видаляє запис із ключем `key`с сервера.

### Список параметрів

`key`

Ключ запису, що видаляється.

`time`

Час, протягом якого сервер очікує видалення запису.

> **Зауваження**: Починаючи з версії memcached 1.3.0 (випущена у 2009 році), функція більше не підтримується. Передача ненульового параметра `time` призведе до помилки при видаленні. Метод [Memcached::getResultCode()](memcached.getresultcode.md) поверне **`MEMCACHED_INVALID_ARGUMENTS`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Метод[Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTFOUND`** якщо заданий ключ немає.

### Приклади

**Приклад #1 Приклад використання** Memcached::delete()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->delete('key1');
?>
```

### Дивіться також

-   [Memcached::deleteByKey()](memcached.deletebykey.md) \- Видаляє запис із вказаного сервера
-   [Memcached::deleteMulti()](memcached.deletemulti.md) \- Видаляє кілька записів
