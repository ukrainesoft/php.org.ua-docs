---
navigation:
  - memcached.getmultibykey.html: '« Memcached::getMultiByKey'
  - memcached.getresultcode.html: 'Memcached::getResultCode »'
  - index.html: PHP Manual
  - class.memcached.html: Memcached
title: 'Memcached::getOption'
---
# Memcached::getOption

(PECL memcached >= 0.1.0)

Memcached::getOption — Отримує значення Memcached параметра

### Опис

```methodsynopsis
public Memcached::getOption(int $option): mixed
```

Цей метод повертає значення Memcached параметра, зазначеного в `option`. Деякі параметри відповідають тим, що визначені в libmemcached, а деякі є специфічними для модуля. Зверніться до розділу [Memcached константи](memcached.constants.html) для отримання додаткової інформації.

### Список параметрів

`option`

Одна з `Memcached::OPT_*` констант.

### Значення, що повертаються

Повертає значення запитуваного параметра, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Отримує значення параметра Memcached**

```php
<?php
$m = new Memcached();
var_dump($m->getOption(Memcached::OPT_COMPRESSION));
var_dump($m->getOption(Memcached::OPT_POLL_TIMEOUT));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
int(1000)
```

### Дивіться також

-   **Memcached::getOption()**
-   [Memcached::setOption()](memcached.setoption.html) - Встановлює значення параметра для Memcached
-   [Memcached Constants](memcached.constants.html)
