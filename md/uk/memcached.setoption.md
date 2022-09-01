---
navigation:
  - memcached.setmultibykey.html: '« Memcached::setMultiByKey'
  - memcached.setoptions.html: 'Memcached::setOptions »'
  - index.html: PHP Manual
  - class.memcached.html: Memcached
title: 'Memcached::setOption'
---
# Memcached::setOption

(PECL memcached >= 0.1.0)

Memcached::setOption — Встановлює значення параметра для Memcached

### Опис

```methodsynopsis
public Memcached::setOption(int $option, mixed $value): bool
```

Метод встановлює значення параметра Memcached, переданого в `option`. Деякі параметри визначені в бібліотеці libmemcached, а деякі вказані в модулі.

### Список параметрів

`option`

Одна з констант `Memcached::OPT_*`. Вивчіть розділ [константи Memcached](memcached.constants.html) для отримання повнішої інформації.

`value`

Значення, яке потрібно встановити.

> **Зауваження**
> 
> Параметри, наведені нижче, потребують значень, вказаних за допомогою констант.
> 
> -   `Memcached::OPT_HASH` вимагає `Memcached::HASH_*` значень.
> -   `Memcached::OPT_DISTRIBUTION` вимагає `Memcached::DISTRIBUTION_*` значень.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлює параметр Memcached**

```php
<?php
$m = new Memcached();
var_dump($m->getOption(Memcached::OPT_HASH) == Memcached::HASH_DEFAULT);
$m->setOption(Memcached::OPT_HASH, Memcached::HASH_MURMUR);
$m->setOption(Memcached::OPT_PREFIX_KEY, "widgets");
echo "Prefix key is now: ", $m->getOption(Memcached::OPT_PREFIX_KEY), "\n";
?>
```

Результат виконання цього прикладу:

```
bool(true)
Prefix key is now: widgets
```

### Дивіться також

-   [Memcached::getOption()](memcached.getoption.html) - Отримує значення Memcached параметра
-   [Memcached::setOptions()](memcached.setoptions.html) - Встановлює кілька Memcached параметрів
-   [Memcached константи](memcached.constants.html)
