---
navigation:
  - memcached.setmultibykey.md: '« Memcached::setMultiByKey'
  - memcached.setoptions.md: 'Memcached::setOptions »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::setOption'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::setOption

(PECL memcached >= 0.1.0)

Memcached::setOption — Встановлює значення параметра для Memcached

### Опис

```methodsynopsis
public Memcached::setOption(int $option, mixed $value): bool
```

Метод устанавливает значение параметра для Memcached, переданного в`option`. Деякі параметри визначені в бібліотеці libmemcached, а деякі вказані в модулі.

### Список параметрів

`option`

Одна из констант`Memcached::OPT_*`Изучите раздел[константи Memcached](memcached.constants.md) для отримання повнішої інформації.

`value`

Значення, яке потрібно встановити.

> **Зауваження** :
> 
> Параметри, наведені нижче, потребують значень, вказаних за допомогою констант.
> 
> -   `Memcached::OPT_HASH` вимагає `Memcached::HASH_*`значень.
> -   `Memcached::OPT_DISTRIBUTION` вимагає `Memcached::DISTRIBUTION_*`значень.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Встановлює параметр Memcached**

```php
<?php
$m = new Memcached();
var_dump($m->getOption(Memcached::OPT_HASH) == Memcached::HASH_DEFAULT);
$m->setOption(Memcached::OPT_HASH, Memcached::HASH_MURMUR);
$m->setOption(Memcached::OPT_PREFIX_KEY, "widgets");
echo "Prefix key is now: ", $m->getOption(Memcached::OPT_PREFIX_KEY), "\n";
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
Prefix key is now: widgets
```

### Дивіться також

-   [Memcached::getOption()](memcached.getoption.md) \- Отримує значення Memcached параметра
-   [Memcached::setOptions()](memcached.setoptions.md) \- Встановлює кілька Memcached параметрів
-   [Memcached константи](memcached.constants.md)
