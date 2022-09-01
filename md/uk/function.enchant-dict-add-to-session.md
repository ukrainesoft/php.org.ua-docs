---
navigation:
  - function.enchant-dict-add-to-personal.html: « enchantdictaddтоpersonal
  - function.enchant-dict-add.html: enchantdictadd »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantdictaddтоsession
---
# enchantdictaddтоsession

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantdictaddтоsession — Додати слово до поточної сесії перевірки

### Опис

```methodsynopsis
enchant_dict_add_to_session(EnchantDictionary $dictionary, string $word): void
```

Додає слово до заданого словника. Слово буде присутнє тільки в поточній сесії перевірки.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.html)

`word`

Слово для додавання

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) - Створити новий словник, використовуючи тег
