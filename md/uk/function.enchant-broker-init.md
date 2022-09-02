---
navigation:
  - function.enchant-broker-get-error.md: « enchantbrokergeterror
  - function.enchant-broker-list-dicts.md: enchantbrokerlistdicts »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantbrokerinit
---
# enchantbrokerinit

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantbrokerinit — Створити новий об'єкт брокера

### Опис

```methodsynopsis
enchant_broker_init(): EnchantBroker|false
```

### Список параметрів

### Значення, що повертаються

Повертає ресурс брокера або \*\*`false`\*\*якщо виникла помилка.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [EnchantBroker](class.enchantbroker.md); Раніше повертався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchantbrokerfree()](function.enchant-broker-free.md) - Звільняє ресурс брокера та його словники
