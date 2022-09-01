---
navigation:
  - memcached.setoption.md: '« Memcached::setOption'
  - memcached.setsaslauthdata.md: 'Memcached::setSaslAuthData »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::setOptions'
---
# Memcached::setOptions

(PECL memcached >= 2.0.0)

Memcached::setOptions — Встановлює декілька параметрів Memcached

### Опис

```methodsynopsis
public Memcached::setOptions(array $options): bool
```

**Memcached::setOptions()** аналогічний методу [Memcached::setOption()](memcached.setoption.md)але приймає масив параметрів.

### Список параметрів

`options`

Асоціативний масив з параметрами, де як ключ виступає назва параметра, а як значення- нове значення даного параметра.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлює декілька параметрів Memcached**

```php
<?php
$m = new Memcached();
var_dump($m->getOption(Memcached::OPT_HASH) == Memcached::HASH_DEFAULT);

$m->setOptions(array(Memcached::OPT_HASH => Memcached::HASH_MURMUR, Memcached::OPT_PREFIX_KEY => "widgets"));

var_dump($m->getOption(Memcached::OPT_HASH) == Memcached::HASH_DEFAULT);
echo "Prefix key is now: ", $m->getOption(Memcached::OPT_PREFIX_KEY), "\n";
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
Prefix key is now: widgets
```

### Дивіться також

-   [Memcached::getOption()](memcached.getoption.md) - Отримує значення Memcached параметра
-   [Memcached::setOption()](memcached.setoption.md) - Встановлює значення параметра для Memcached
-   [Memcached Constants](memcached.constants.md)
