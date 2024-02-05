---
navigation:
  - function.enchant-dict-add.md: « enchant\_dict\_add
  - function.enchant-dict-describe.md: enchant\_dict\_describe »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_dict\_check
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_dict\_check

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_dict\_check — Перевіряє, чи правильно задано слово

### Опис

```methodsynopsis
enchant_dict_check(EnchantDictionary $dictionary, string $word): bool
```

Повертає **`true`**, якщо слово написано без помилок або \*\*`false`\*\*якщо з помилками.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md)

`word`

Слово для перевірки

### Значення, що повертаються

Повертає **`true`**, якщо слово написано без помилок або \*\*`false`\*\*якщо з помилками.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
