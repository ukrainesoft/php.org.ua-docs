---
navigation:
  - memcached.getmultibykey.md: '« Memcached::getMultiByKey'
  - memcached.getresultcode.md: 'Memcached::getResultCode »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::getOption'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::getOption

(PECL memcached >= 0.1.0)

Memcached::getOption — Отримує значення Memcached параметра

### Опис

```methodsynopsis
public Memcached::getOption(int $option): mixed
```

Цей метод повертає значення Memcached параметра, зазначеного в `option`. Деякі параметри відповідають тим, що визначені в libmemcached, а деякі є специфічними для модуля. Зверніться до розділу [Memcached константи](memcached.constants.md) для отримання додаткової інформації.

### Список параметрів

`option`

Одна из`Memcached::OPT_*`констант.

### Значення, що повертаються

Повертає значення запитуваного параметра, або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Отримує значення параметра Memcached**

```php
<?php
$m = new Memcached();
var_dump($m->getOption(Memcached::OPT_COMPRESSION));
var_dump($m->getOption(Memcached::OPT_POLL_TIMEOUT));
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
int(1000)
```

### Дивіться також

-   **Memcached::getOption()**
-   [Memcached::setOption()](memcached.setoption.md) \- Встановлює значення параметра для Memcached
-   [Memcached Constants](memcached.constants.md)
