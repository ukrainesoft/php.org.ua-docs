---
navigation:
  - function.enchant-dict-describe.md: « enchantdictdescribe
  - function.enchant-dict-is-added.md: enchantdictісadded »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantdictgeterror
---
# enchantdictgeterror

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantdictgeterror — Повертає останню помилку поточної сесії перевірки

### Опис

```methodsynopsis
enchant_dict_get_error(EnchantDictionary $dictionary): string|false
```

Повертає останню помилку поточної сесії перевірки.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.md) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.md)

### Значення, що повертаються

Повертає рядок з помилкою або \*\*`false`\*\*якщо такої немає.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
