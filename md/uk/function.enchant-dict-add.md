Додає слово до особистого словника

-   [« enchantdictaddтоsession](function.enchant-dict-add-to-session.html)
    
-   [enchantdictcheck »](function.enchant-dict-check.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Додає слово до особистого словника
    

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

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.html)

`word`

Слово, яке потрібно додати

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.html) - Створити словник, використовуючи файл PWL
-   [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) - Створити новий словник, використовуючи тег