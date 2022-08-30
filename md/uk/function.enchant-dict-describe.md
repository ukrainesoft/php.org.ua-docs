Повертає інформацію про словник

-   [« enchantdictcheck](function.enchant-dict-check.html)
    
-   [enchantdictgeterror »](function.enchant-dict-get-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Повертає інформацію про словник
    

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

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | До цієї версії функція повертала **`false`** у разі виникнення помилки. |

### Приклади

**Приклад #1 Приклад використання **enchantdictdescribe()****

Перевіримо, що словник є за допомогою [enchantbrokerdictexists()](function.enchant-broker-dict-exists.html) та отримаємо інформацію про нього.

```php
<?php
$tag = 'en_US';
$broker = enchant_broker_init();
if (enchant_broker_dict_exists($broker,$tag)) {
    $dict = enchant_broker_request_dict($r, $tag);
    $dict_details = enchant_dict_describe($dict);
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