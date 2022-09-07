---
navigation:
  - memcached.deletebykey.md: '« Memcached::deleteByKey'
  - memcached.deletemultibykey.md: 'Memcached::deleteMultiByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::deleteMulti'
---
# Memcached::deleteMulti

(PECL memcached >= 2.0.0)

Memcached::deleteMulti — Видаляє кілька записів

### Опис

```methodsynopsis
public Memcached::deleteMulti(array $keys, int $time = 0): array
```

**Memcached::deleteMulti()** видаляє записи, передані в масиві `keys`з сервера. Параметр `time` задає період часу в секундах протягом якого (або тимчасову мітку у форматі Unix до якої) сервер відхилятиме `add` і `replace` запити клієнта за цим ключем. Протягом цього часу запис міститься в чергу на видалення, що означає неможливість отримання значення за допомогою команди `get`, команди `add` і `replace` за даним ключем також буде завершено невдачею (проте команда `set` буде успішно виконано). Після закінчення цього часу запис буде остаточно видалено з пам'яті сервера. За замовчуванням параметр `time` встановлений у 0 (що означає негайне видалення запису та подальші операції з цим записом будуть успішно виконані).

### Список параметрів

`keys`

Ключ запису, що видаляється.

`time`

Час, протягом якого сервер очікує видалення запису.

### Значення, що повертаються

Повертає масив із індексами `keys` і значеннями, що позначають вдало чи ні, завершилася операція. Метод [Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTFOUND`** якщо заданий ключ не існує.

### Дивіться також

-   [Memcached::delete()](memcached.delete.md) - Видаляє запис
-   [Memcached::deleteByKey()](memcached.deletebykey.md) - Видаляє запис із вказаного сервера
-   [Memcached::deleteMultiByKey()](memcached.deletemultibykey.md) - Видаляє кілька записів із вказаного сервера
