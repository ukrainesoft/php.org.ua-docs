---
navigation:
  - function.apcu-exists.html: « apcuexists
  - function.apcu-inc.html: apcuinc »
  - index.html: PHP Manual
  - ref.apcu.html: Функции APCu
title: apcufetch
---
# apcufetch

(PECL apcu >= 4.0.0)

apcufetch - Витягує з кеша збережену змінну

### Опис

```methodsynopsis
apcu_fetch(mixed $key, bool &$success = ?): mixed
```

Витягує з кеша змінну змінну.

### Список параметрів

`key`

Ключ `key`, під яким запис було збережено в кеш (за допомогою [apcustore()](function.apcu-store.html)). Якщо заданий масив, то буде вилучено та повернено кожен елемент.

`success`

Встановлюється в **`true`** у разі успішного виконання та **`false`** у разі виникнення помилки.

### Значення, що повертаються

Збережена змінна чи масив; **`false`** у разі виникнення помилки

### список змін

| Версия | Описание |
| --- | --- |
| PECL apcu 3.0.17 | Доданий параметр `success` |

### Приклади

**Приклад #1 Приклад використання **apcufetch()****

```php
<?php
$bar = 'BAR';
apcu_store('foo', $bar);
var_dump(apcu_fetch('foo'));
?>
```

Результат виконання цього прикладу:

```
string(3) "BAR"
```

### Дивіться також

-   [apcustore()](function.apcu-store.html) - Кешує змінну
-   [apcudelete()](function.apcu-delete.html) - Видаляє збережене значення з кешу
-   [APCUIterator](class.apcuiterator.html)
