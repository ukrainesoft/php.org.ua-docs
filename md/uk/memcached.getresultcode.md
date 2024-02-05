---
navigation:
  - memcached.getoption.md: '« Memcached::getOption'
  - memcached.getresultmessage.md: 'Memcached::getResultMessage »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::getResultCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::getResultCode

(PECL memcached >= 0.1.0)

Memcached::getResultCode — Повертає результуючий код останньої виконаної операції

### Опис

```methodsynopsis
public Memcached::getResultCode(): int
```

**Memcached::getResultCode()** повертає одну з констант **`Memcached::RES_*`**, що є результуючим кодом виконання останнього методу Memcached.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Результуючий код останньої операції Memcached.

### Приклади

**Приклад #1 Приклад використання** Memcached::getResultCode()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->add('foo', 'bar');
if ($m->getResultCode() == Memcached::RES_NOTSTORED) {
    /* ... */
}
?>
```
