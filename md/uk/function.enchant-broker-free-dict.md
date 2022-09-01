---
navigation:
  - function.enchant-broker-dict-exists.html: « enchantbrokerdictexists
  - function.enchant-broker-free.html: enchantbrokerfree »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantbrokerfreedict
---
# enchantbrokerfreedict

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantbrokerfreedict - Звільняє ресурс словника

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
enchant_broker_free_dict(EnchantDictionary $dictionary): bool
```

Звільняє словник. Починаючи з PHP 8.0.0, рекомендується знищити об'єкт замість виклику цієї функції.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchantbrokerrequestdict()](function.enchant-broker-request-dict.md) - Створити новий словник, використовуючи тег
-   [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.md) - Створити словник, використовуючи файл PWL
