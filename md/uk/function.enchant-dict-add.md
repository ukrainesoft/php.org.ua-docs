---
navigation:
  - function.enchant-dict-add-to-session.md: « enchant\_dict\_add\_to\_session
  - function.enchant-dict-check.md: enchant\_dict\_check »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_dict\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_dict\_add

(PHP 8)

enchant\_dict\_add — Додає слово до особистого словника

### Опис

```methodsynopsis
enchant_dict_add(EnchantDictionary $dictionary, string $word): void
```

Додає слово до особистого словника.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md)

`word`

Слово, яке потрібно додати

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

**Приклад #1 Додавання слова до PWL**

```php
<?php

$filename = './my_word_list.pwl';
$word = 'Supercalifragilisticexpialidocious';

$broker = enchant_broker_init();
$dict = enchant_broker_request_pwl_dict($broker, $filename);

enchant_dict_add($dict, $word);

enchant_broker_free($broker);

?>
```

### Дивіться також

-   [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md) \- Створити словник, використовуючи файл PWL
-   [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) \- Створити новий словник, використовуючи тег
