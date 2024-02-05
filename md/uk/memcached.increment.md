---
navigation:
  - memcached.getversion.md: '« Memcached::getVersion'
  - memcached.incrementbykey.md: 'Memcached::incrementByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::increment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::increment

(PECL memcached >= 0.1.0)

Memcached::increment — Збільшує числове значення запису

### Опис

```methodsynopsis
public Memcached::increment(    string $key,    int $offset = 1,    int $initial_value = 0,    int $expiry = 0): int|false
```

**Memcached::increment()** збільшує числове значення запису на величину, вказану у параметрі `offset`. Якщо запис містить не числове значення, повернеться помилка. Метод \*\*Memcached::increment()\*\*установит записи значение, переданное в`initial_value`, якщо запису із зазначеним ключем не існує.

### Список параметрів

`key`

Ключ запису, що збільшується.

`offset`

Величина, на яку відбувається збільшення значення запису.

`initial_value`

Ініціює значення, яке буде встановлено запису, якщо переданого ключа немає.

`expiry`

Час, коли термін дії запису спливає.

### Значення, що повертаються

Повертає нове значення запису у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**Memcached::increment()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('counter', 0);
$m->increment('counter');
$n = $m->increment('counter', 10);
var_dump($n);

$m->set('counter', 'abc');
$n = $m->increment('counter');
// Завершится неудачей т.к. значение записи не является числовым
var_dump($n);
?>
```

Результат виконання наведеного прикладу:

```
int(11)
bool(false)
```

### Дивіться також

-   [Memcached::decrement()](memcached.decrement.md) \- Зменшує числове значення запису
-   [Memcached::decrementByKey()](memcached.decrementbykey.md) \- Зменшує числове значення запису, що зберігається на певному сервері
-   [Memcached::incrementByKey()](memcached.incrementbykey.md) \- Збільшує числове значення запису, що зберігається на вказаному сервері
