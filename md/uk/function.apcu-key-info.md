---
navigation:
  - function.apcu-inc.md: « apcuinc
  - function.apcu-sma-info.md: apcusmainfo »
  - index.md: PHP Manual
  - ref.apcu.md: Функции APCu
title: apcukeyinfo
---
# apcukeyinfo

(No version information available, might only be in Git)

apcukeyinfo — Отримати детальну інформацію про ключ у кеші

### Опис

```methodsynopsis
apcu_key_info(string $key): ?array
```

Отримати детальну інформацію про ключ у кеші

### Список параметрів

`key`

Отримати детальну інформацію про ключ у кеші

### Значення, що повертаються

Масив, що містить докладну інформацію про ключ кеша або \*\*`null`\*\*якщо ключ не існує.

### Приклади

**Приклад #1 Приклад використання **apcukeyinfo()****

```php
<?php
apcu_add('a','b');
var_dump(apcu_key_info('a'));
?>
```

Результат виконання цього прикладу:

```
array(7) {
  ["hits"]=>
  int(0)
  ["access_time"]=>
  int(1606701783)
  ["mtime"]=>
  int(1606701783)
  ["creation_time"]=>
  int(1606701783)
  ["deletion_time"]=>
  int(0)
  ["ttl"]=>
  int(0)
  ["refs"]=>
  int(0)
}
```

### Дивіться також

-   [apcustore()](function.apcu-store.md) - Кешує змінну
-   [apcufetch()](function.apcu-fetch.md) - Витягує з кеша збережену змінну
-   [apcudelete()](function.apcu-delete.md) - Видаляє збережене значення з кешу
