---
navigation:
  - function.enchant-dict-quick-check.md: « enchantdictquickcheck
  - function.enchant-dict-suggest.md: enchantdictsuggest »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantdictstorereplacement
---
# enchantdictstorereplacement

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantdictstorereplacement — Додати виправлення для слова

### Опис

```methodsynopsis
enchant_dict_store_replacement(EnchantDictionary $dictionary, string $misspelled, string $correct): void
```

Додати виправлення 'cor' для 'mis'. Зверніть увагу, що якщо ви заміните @ mis на @ cor, то в майбутньому входження @ mis будуть замінюватися на @ cor. Відповідно, це може підняти @cor вгору в списку можливих замін.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.md) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.md)

`misspelled`

Слово для виправлення

`correct`

Коректне слово

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
