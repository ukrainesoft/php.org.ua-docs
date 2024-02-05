---
navigation:
  - function.enchant-dict-add-to-personal.md: « enchant\_dict\_add\_to\_personal
  - function.enchant-dict-add.md: enchant\_dict\_add »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_dict\_add\_to\_session
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_dict\_add\_to\_session

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_dict\_add\_to\_session — Додати слово до поточної сесії перевірки

### Опис

```methodsynopsis
enchant_dict_add_to_session(EnchantDictionary $dictionary, string $word): void
```

Додає слово до заданого словника. Слово буде присутнє тільки в поточній сесії перевірки.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md)

`word`

Слово для додавання

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) \- Створити новий словник, використовуючи тег
