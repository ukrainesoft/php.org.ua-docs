---
navigation:
  - ref.enchant.md: « Функції Enchant
  - function.enchant-broker-dict-exists.md: enchant\_broker\_dict\_exists »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_broker\_describe
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_broker\_describe

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0)

enchant\_broker\_describe — Перераховує провайдерів Enchant

### Опис

```methodsynopsis
enchant_broker_describe(EnchantBroker $broker): array
```

Перераховує провайдерів Enchant та повертає мінімальну інформацію про них. Така сама інформація може бути отримана через phpinfo().

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.md)

### Значення, що повертаються

Повертає масив доступних провайдерів Enchant з їх даними.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | До цієї версії функція повертала \*\*`false`\*\*в случае возникновения ошибки. |

### Приклади

**Приклад #1 Список бекендів, що надаються конкретним брокером**

```php
<?php
$r = enchant_broker_init();
$bprovides = enchant_broker_describe($r);
echo "Брокер предоставляет следующие бэкенды:\n";
print_r($bprovides);

?>
```

Висновок наведеного прикладу буде схожим на:

```
Брокер предоставляет следующие бэкенды:
Array
(
    [0] => Array
        (
            [name] => aspell
            [desc] => Aspell Provider
            [file] => /usr/lib/enchant/libenchant_aspell.so
        )

    [1] => Array
        (
            [name] => hspell
            [desc] => Hspell Provider
            [file] => /usr/lib/enchant/libenchant_hspell.so
        )

    [2] => Array
        (
            [name] => ispell
            [desc] => Ispell Provider
            [file] => /usr/lib/enchant/libenchant_ispell.so
        )

    [3] => Array
        (
            [name] => myspell
            [desc] => Myspell Provider
            [file] => /usr/lib/enchant/libenchant_myspell.so
        )

)
```
