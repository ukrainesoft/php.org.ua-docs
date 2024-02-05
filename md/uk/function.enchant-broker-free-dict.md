---
navigation:
  - function.enchant-broker-dict-exists.md: « enchant\_broker\_dict\_exists
  - function.enchant-broker-free.md: enchant\_broker\_free »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_broker\_free\_dict
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_broker\_free\_dict

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_broker\_free\_dict - Звільняє ресурс словника

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
enchant_broker_free_dict(EnchantDictionary $dictionary): bool
```

Звільняє словник. Починаючи з PHP 8.0.0, рекомендується знищити об'єкт замість виклику цієї функції.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `dictionary` чекає [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) \- Створити новий словник, використовуючи тег
-   [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md) \- Створити словник, використовуючи файл PWL
