---
navigation:
  - function.enchant-dict-check.md: « enchant\_dict\_check
  - function.enchant-dict-get-error.md: enchant\_dict\_get\_error »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_dict\_describe
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_dict\_describe

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_dict\_describe — Повертає інформацію про словник

### Опис

```methodsynopsis
enchant_dict_describe(EnchantDictionary $dictionary): array
```

Повертає інформацію про словник.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | До цієї версії функція повертала \*\*`false`\*\*в случае возникновения ошибки. |

### Приклади

**Пример #1 Пример использования**enchant\_dict\_describe()\*\*\*\*

Перевіримо, що словник є за допомогою [enchant\_broker\_dict\_exists()](function.enchant-broker-dict-exists.md) та отримаємо інформацію про нього.

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

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [lang] => en_US
    [name] => aspell
    [desc] => Aspell Provider
    [file] => /usr/lib/enchant/libenchant_aspell.so
)
```
