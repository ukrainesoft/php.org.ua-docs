---
navigation:
  - function.enchant-broker-init.md: « enchant\_broker\_init
  - function.enchant-broker-request-dict.md: enchant\_broker\_request\_dict »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_broker\_list\_dicts
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_broker\_list\_dicts

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 1.0.1)

enchant\_broker\_list\_dicts — Повертає список доступних словників

### Опис

```methodsynopsis
enchant_broker_list_dicts(EnchantBroker $broker): array
```

Повертає список доступних словників.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.md)

### Значення, що повертаються

Повертає масив (array) доступних словників зі своїми даними.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | До цієї версії функція повертала \*\*`false`\*\*в случае возникновения ошибки. |

### Приклади

**Приклад #1 Список всіх словників, що доступні на брокері**

```php
<?php
$r = enchant_broker_init();
$dicts = enchant_broker_list_dicts($r);
print_r($dicts);
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [enchant\_broker\_describe()](function.enchant-broker-describe.md) \- Перераховує провайдерів Enchant
