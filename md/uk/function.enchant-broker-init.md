---
navigation:
  - function.enchant-broker-get-error.md: « enchant\_broker\_get\_error
  - function.enchant-broker-list-dicts.md: enchant\_broker\_list\_dicts »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_broker\_init
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_broker\_init

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_broker\_init — Створити новий об'єкт брокера

### Опис

```methodsynopsis
enchant_broker_init(): EnchantBroker|false
```

### Список параметрів

### Значення, що повертаються

Повертає ресурс брокера або \*\*`false`\*\*якщо виникла помилка.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [EnchantBroker](class.enchantbroker.md); Раніше повертався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchant\_broker\_free()](function.enchant-broker-free.md) \- Звільняє ресурс брокера та його словники
