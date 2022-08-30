Перераховує провайдерів Enchant

-   [« Функции Enchant](ref.enchant.md)
    
-   [enchantbrokerdictexists »](function.enchant-broker-dict-exists.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Enchant](ref.enchant.md)
    
-   Перераховує провайдерів Enchant
    

# enchantbrokerdescribe

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0)

enchantbrokerdescribe — Перераховує провайдерів Enchant

### Опис

```methodsynopsis
enchant_broker_describe(EnchantBroker $broker): array
```

Перераховує провайдерів Enchant та повертає мінімальну інформацію про них. Така сама інформація може бути отримана через phpinfo().

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.html)

### Значення, що повертаються

Повертає масив доступних провайдерів Enchant з їх даними.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | До цієї версії функція повертала **`false`** у разі виникнення помилки. |

### Приклади

**Приклад #1 Список бекендів, що надаються конкретним брокером**

```php
<?php
$r = enchant_broker_init();
$bprovides = enchant_broker_describe($r);
echo "Брокер предоставляет следующие бэкенды:\n";
print_r($bprovides);

?>
```

Результатом виконання цього прикладу буде щось подібне:

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