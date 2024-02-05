---
navigation:
  - function.apcu-inc.md: « apcu\_inc
  - function.apcu-sma-info.md: apcu\_sma\_info »
  - index.md: PHP Manual
  - ref.apcu.md: Функції APCu
title: apcu\_key\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apcu\_key\_info

(No version information available, might only be in Git)

apcu\_key\_info — Отримати детальну інформацію про ключ у кеші

### Опис

```methodsynopsis
apcu_key_info(string $key): ?array
```

Отримати детальну інформацію про ключ у кеші

### Список параметрів

`key`

Отримати детальну інформацію про ключ у кеші

### Значення, що повертаються

Массив, содержащий подробную информацию о ключе кеша или\*\*`null`\*\*якщо ключ не існує.

### Приклади

**Пример #1 Пример использования**apcu\_key\_info()\*\*\*\*

```php
<?php
apcu_add('a','b');
var_dump(apcu_key_info('a'));
?>
```

Результат виконання наведеного прикладу:

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

-   [apcu\_store()](function.apcu-store.md) \- Кешує змінну
-   [apcu\_fetch()](function.apcu-fetch.md) \- Витягує з кеша збережену змінну
-   [apcu\_delete()](function.apcu-delete.md) \- Видаляє збережене значення з кешу
