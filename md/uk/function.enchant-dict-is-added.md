---
navigation:
  - function.enchant-dict-get-error.md: « enchant\_dict\_get\_error
  - function.enchant-dict-is-in-session.md: enchant\_dict\_is\_in\_session »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_dict\_is\_added
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_dict\_is\_added

(PHP 8)

enchant\_dict\_is\_added - Визначає, чи існує слово в цій орфографічній сесії

### Опис

```methodsynopsis
enchant_dict_is_added(EnchantDictionary $dictionary, string $word): bool
```

Визначає, чи вже існує слово в поточній сесії.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md)

`word`

Слово для пошуку

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо слово вже існує, інакше повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchant\_dict\_add\_to\_session()](function.enchant-dict-add-to-session.md) \- Додати слово у поточну сесію перевірки
