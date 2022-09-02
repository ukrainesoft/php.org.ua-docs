---
navigation:
  - memcached.decrementbykey.md: '« Memcached::decrementByKey'
  - memcached.deletebykey.md: 'Memcached::deleteByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::delete'
---
# Memcached::delete

(PECL memcached >= 0.1.0)

Memcached::delete — Видаляє запис

### Опис

```methodsynopsis
public Memcached::delete(string $key, int $time = 0): bool
```

**Memcached::delete()** видаляє запис із ключем `key` із сервера. Параметр `time` задає період часу в секундах протягом якого (або тимчасову мітку у форматі Unix до якої) сервер відхилятиме `add` і `replace` запити клієнта за цим ключем. Протягом цього часу запис міститься в чергу на видалення, що означає неможливість отримання значення за допомогою команди `get`, команди `add` і `replace` за даним ключем також буде завершено невдачею (проте команда `set` буде успішно виконано). Після закінчення цього часу запис буде остаточно видалено з пам'яті сервера. За замовчуванням параметр `time` встановлений у 0 (що означає негайне видалення запису та подальші операції з цим записом будуть успішно виконані).

### Список параметрів

`key`

Ключ запису, що видаляється.

`time`

Час, протягом якого сервер очікує видалення запису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTFOUND`** якщо заданий ключ немає.

### Приклади

**Приклад #1 Приклад використання **Memcached::delete()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->delete('key1');
?>
```

### Дивіться також

-   [Memcached::deleteByKey()](memcached.deletebykey.md) - Видаляє запис із вказаного сервера
-   [Memcached::deleteMulti()](memcached.deletemulti.md) - Видаляє кілька записів
