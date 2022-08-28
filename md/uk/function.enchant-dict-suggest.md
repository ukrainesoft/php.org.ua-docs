Поверне список можливих варіантів для слова з помилкою

-   [« enchant\_dict\_store\_replacement](function.enchant-dict-store-replacement.html)
    
-   [EnchantBroker »](class.enchantbroker.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Поверне список можливих варіантів для слова з помилкою
    

# enchantdictsuggest

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantdictsuggest — Поверне список можливих варіантів для слова з помилкою

### Опис

```methodsynopsis
enchant_dict_suggest(EnchantDictionary $dictionary, string $word): array
```

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.html) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.html)

`word`

Слово для перевірки.

### Значення, що повертаються

Поверне масив припущень для заданого помилкою слова.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **enchantdictsuggest()****

```php
<?php
$tag = 'en_US';
$r = enchant_broker_init();
if (enchant_broker_dict_exists($r,$tag)) {
    $d = enchant_broker_request_dict($r, $tag);

    $wordcorrect = enchant_dict_check($d, "soong");
    if (!$wordcorrect) {
        $suggs = enchant_dict_suggest($d, "soong");
        echo "Подсказки для 'soong':";
        print_r($suggs);
    }
    enchant_broker_free_dict($d);
}
enchant_broker_free($r);
?>
```

### Дивіться також

-   [enchant\_dict\_check()](function.enchant-dict-check.html) - Перевіряє, чи правильно задано слово
-   [enchant\_dict\_quick\_check()](function.enchant-dict-quick-check.html) - Перевірити, чи правильно написано слово та запропонувати варіанти заміни