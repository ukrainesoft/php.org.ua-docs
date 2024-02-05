---
navigation:
  - function.enchant-dict-describe.md: « enchant\_dict\_describe
  - function.enchant-dict-is-added.md: enchant\_dict\_is\_added »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_dict\_get\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_dict\_get\_error

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_dict\_get\_error — Повертає останню помилку поточної сесії перевірки

### Опис

```methodsynopsis
enchant_dict_get_error(EnchantDictionary $dictionary): string|false
```

Повертає останню помилку поточної сесії перевірки.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md)

### Значення, що повертаються

Повертає рядок з помилкою або \*\*`false`\*\*якщо такої немає.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
