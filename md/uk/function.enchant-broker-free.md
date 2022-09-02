---
navigation:
  - function.enchant-broker-free-dict.md: « enchantbrokerfreedict
  - function.enchant-broker-get-dict-path.md: enchantbrokergetdictpath »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantbrokerfree
---
# enchantbrokerfree

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantbrokerfree — Звільняє ресурс брокера та його словники

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
enchant_broker_free(EnchantBroker $broker): bool
```

Звільняє брокера з його словниками. Починаючи з PHP 8.0.0, рекомендується знищити об'єкт замість виклику цієї функції.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchantbrokerinit()](function.enchant-broker-init.md) - Створити новий об'єкт брокера
