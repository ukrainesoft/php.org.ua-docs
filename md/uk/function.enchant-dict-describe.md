---
navigation:
  - function.enchant-dict-check.md: « enchantdictcheck
  - function.enchant-dict-get-error.md: enchantdictgeterror »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantdictdescribe
---
# enchantdictdescribe

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantdictdescribe — Повертає інформацію про словник

### Опис

```methodsynopsis
enchant_dict_describe(EnchantDictionary $dictionary): array
```

Повертає інформацію про словник.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.md) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | До цієї версії функція повертала **`false`** у разі виникнення помилки. |

### Приклади

**Приклад #1 Приклад використання **enchantdictdescribe()****

Перевіримо, що словник є за допомогою [enchantbrokerdictexists()](function.enchant-broker-dict-exists.md) та отримаємо інформацію про нього.

```php
<?php
$tag = 'en_US';
$broker = enchant_broker_init();
if (enchant_broker_dict_exists($broker,$tag)) {
    $dict = enchant_broker_request_dict($r, $tag);
    $dict_details = enchant_dict_describe($dict);
    print_r($dict_details);
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [lang] => en_US
    [name] => aspell
    [desc] => Aspell Provider
    [file] => /usr/lib/enchant/libenchant_aspell.so
)
```
