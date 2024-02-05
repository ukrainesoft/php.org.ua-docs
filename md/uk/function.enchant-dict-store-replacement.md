---
navigation:
  - function.enchant-dict-quick-check.md: « enchant\_dict\_quick\_check
  - function.enchant-dict-suggest.md: enchant\_dict\_suggest »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_dict\_store\_replacement
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_dict\_store\_replacement

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_dict\_store\_replacement — Додати виправлення для слова

### Опис

```methodsynopsis
enchant_dict_store_replacement(EnchantDictionary $dictionary, string $misspelled, string $correct): void
```

Додати виправлення 'cor' для 'mis'. Зверніть увагу, що якщо ви заміните @ mis на @ cor, то в майбутньому входження @ mis будуть замінюватися на @ cor. Відповідно, це може підняти @cor вгору в списку можливих замін.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md)

`misspelled`

Слово для виправлення

`correct`

Коректне слово

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
