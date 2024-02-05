---
navigation:
  - function.apcu-exists.md: « apcu\_exists
  - function.apcu-inc.md: apcu\_inc »
  - index.md: PHP Manual
  - ref.apcu.md: Функції APCu
title: apcu\_fetch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apcu\_fetch

(PECL apcu >= 4.0.0)

apcu\_fetch - Витягує з кеша збережену змінну

### Опис

```methodsynopsis
apcu_fetch(mixed $key, bool &$success = ?): mixed
```

Витягує з кеша збережену змінну.

### Список параметрів

`key`

Ключ`key`, під яким запис було збережено в кеш (за допомогою [apcu\_store()](function.apcu-store.md)). Якщо заданий масив, то буде вилучено та повернено кожен елемент.

`success`

Устанавливается в\*\*`true`\*\* у разі успішного виконання та \*\*`false`\*\*в случае возникновения ошибки.

### Значення, що повертаються

Збережена змінна чи масив; \*\*`false`\*\*в случае возникновения ошибки

### список змін

| Версия | Опис |
| --- | --- |
| PECL apcu 3.0.17 | Добавлен параметр`success` |

### Приклади

**Пример #1 Пример использования**apcu\_fetch()\*\*\*\*

```php
<?php
$bar = 'BAR';
apcu_store('foo', $bar);
var_dump(apcu_fetch('foo'));
?>
```

Результат виконання наведеного прикладу:

```
string(3) "BAR"
```

### Дивіться також

-   [apcu\_store()](function.apcu-store.md) \- Кешує змінну
-   [apcu\_delete()](function.apcu-delete.md) \- Видаляє збережене значення з кешу
-   [APCUIterator](class.apcuiterator.md)
