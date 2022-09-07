---
navigation:
  - function.enchant-dict-get-error.md: « enchantdictgeterror
  - function.enchant-dict-is-in-session.md: enchantdictісінsession »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantdictісadded
---
# enchantdictісadded

(PHP 8)

enchantdictісadded - Визначає, чи існує слово в цій орфографічній сесії

### Опис

```methodsynopsis
enchant_dict_is_added(EnchantDictionary $dictionary, string $word): bool
```

Визначає, чи вже існує слово в поточній сесії.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.md) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.md)

`word`

Слово для пошуку

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо слово вже існує, інакше повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchantdictaddтоsession()](function.enchant-dict-add-to-session.md) - Додати слово у поточну сесію перевірки
