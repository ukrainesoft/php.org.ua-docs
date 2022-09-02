---
navigation:
  - function.enchant-dict-add-to-session.md: « enchantdictaddтоsession
  - function.enchant-dict-check.md: enchantdictcheck »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantdictadd
---
# enchantdictadd

(PHP 8)

enchantdictadd — Додає слово до особистого словника

### Опис

```methodsynopsis
enchant_dict_add(EnchantDictionary $dictionary, string $word): void
```

Додає слово до особистого словника.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.md) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.md)

`word`

Слово, яке потрібно додати

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

**Приклад #1 Додавання слова до PWL**

```php
<?php

$filename = './my_word_list.pwl';
$word = 'Supercalifragilisticexpialidocious';

$broker = enchant_broker_init();
$dict = enchant_broker_request_pwl_dict($broker, $filename);

enchant_dict_add($dict, $word);

enchant_broker_free($broker);

?>
```

### Дивіться також

-   [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.md) - Створити словник, використовуючи файл PWL
-   [enchantbrokerrequestdict()](function.enchant-broker-request-dict.md) - Створити новий словник, використовуючи тег
