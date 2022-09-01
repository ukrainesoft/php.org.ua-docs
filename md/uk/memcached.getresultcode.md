---
navigation:
  - memcached.getoption.html: '« Memcached::getOption'
  - memcached.getresultmessage.html: 'Memcached::getResultMessage »'
  - index.html: PHP Manual
  - class.memcached.html: Memcached
title: 'Memcached::getResultCode'
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

**Приклад #1 Приклад використання **Memcached::getResultCode()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->add('foo', 'bar');
if ($m->getResultCode() == Memcached::RES_NOTSTORED) {
    /* ... */
}
?>
```
