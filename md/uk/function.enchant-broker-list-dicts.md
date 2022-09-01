---
navigation:
  - function.enchant-broker-init.html: « enchantbrokerinit
  - function.enchant-broker-request-dict.html: enchantbrokerrequestdict »
  - index.html: PHP Manual
  - ref.enchant.html: Функции Enchant
title: enchantbrokerlistdicts
---
# enchantbrokerlistdicts

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 1.0.1)

enchantbrokerlistdicts — Повертає список доступних словників

### Опис

```methodsynopsis
enchant_broker_list_dicts(EnchantBroker $broker): array
```

Повертає список доступних словників.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.html)

### Значення, що повертаються

Повертає масив (array) доступних словників зі своїми даними.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | До цієї версії функція повертала **`false`** у разі виникнення помилки. |

### Приклади

**Приклад #1 Список всіх словників, що доступні на брокері**

```php
<?php
$r = enchant_broker_init();
$dicts = enchant_broker_list_dicts($r);
print_r($dicts);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => Array
        (
            [lang_tag] => de
            [provider_name] => aspell
            [provider_desc] => Aspell Provider
            [provider_file] => /usr/lib/enchant/libenchant_aspell.so
        )

    [1] => Array
        (
            [lang_tag] => de_DE
            [provider_name] => aspell
            [provider_desc] => Aspell Provider
            [provider_file] => /usr/lib/enchant/libenchant_aspell.so
        )

    [3] => Array
        (
            [lang_tag] => en
            [provider_name] => aspell
            [provider_desc] => Aspell Provider
            [provider_file] => /usr/lib/enchant/libenchant_aspell.so
        )

    [4] => Array
        (
            [lang_tag] => en_GB
            [provider_name] => aspell
            [provider_desc] => Aspell Provider
            [provider_file] => /usr/lib/enchant/libenchant_aspell.so
        )

    [5] => Array
        (
            [lang_tag] => en_US
            [provider_name] => aspell
            [provider_desc] => Aspell Provider
            [provider_file] => /usr/lib/enchant/libenchant_aspell.so
        )

    [6] => Array
        (
            [lang_tag] => hi_IN
            [provider_name] => myspell
            [provider_desc] => Myspell Provider
            [provider_file] => /usr/lib/enchant/libenchant_myspell.so
        )

)
```

### Дивіться також

-   [enchantbrokerdescribe()](function.enchant-broker-describe.html) - Перераховує провайдерів Enchant
