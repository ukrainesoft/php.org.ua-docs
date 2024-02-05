---
navigation:
  - function.enchant-dict-store-replacement.md: « enchant\_dict\_store\_replacement
  - class.enchantbroker.md: EnchantBroker »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_dict\_suggest
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_dict\_suggest

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_dict\_suggest — Поверне список можливих варіантів для слова з помилкою

### Опис

```methodsynopsis
enchant_dict_suggest(EnchantDictionary $dictionary, string $word): array
```

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.md) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.md)

`word`

Слово для перевірки.

### Значення, що повертаються

Поверне масив припущень для заданого помилкою слова.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** enchant\_dict\_suggest()\*\*\*\*

```php
<?php
$tag = 'en_US';
$r = enchant_broker_init();
if (enchant_broker_dict_exists($r,$tag)) {
    $d = enchant_broker_request_dict($r, $tag);

    $wordcorrect = enchant_dict_check($d, "soong");
    if (!$wordcorrect) {
        $suggs = enchant_dict_suggest($d, "soong");
        echo "Подсказки для 'soong':";
        print_r($suggs);
    }
    enchant_broker_free_dict($d);
}
enchant_broker_free($r);
?>
```

### Дивіться також

-   [enchant\_dict\_check()](function.enchant-dict-check.md) \- Перевіряє, чи правильно задано слово
-   [enchant\_dict\_quick\_check()](function.enchant-dict-quick-check.md) \- Перевірити, чи правильно написано слово та запропонувати варіанти заміни
