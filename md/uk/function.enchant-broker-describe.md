- [« Функції Enchant](ref.enchant.md)
- [enchant_broker_dict_exists »](function.enchant-broker-dict-exists.md)

- [PHP Manual](index.md)
- [Функції Enchant](ref.enchant.md)
- Перераховує провайдерів Enchant

#enchant_broker_describe

(PHP 5 \>= 5.3.0, PHP 7, PHP 8, PECL enchant \>= 0.1.0)

enchant_broker_describe - Перераховує провайдерів Enchant

### Опис

**enchant_broker_describe**([EnchantBroker](class.enchantbroker.md)
`$broker`): array

Перераховує провайдерів Enchant та повертає мінімальну інформацію про
них. Така сама інформація може бути отримана через phpinfo().

### Список параметрів

`broker`
Провайдер Enchant, який повертається
[enchant_broker_init()](function.enchant-broker-init.md).

### Значення, що повертаються

Повертає масив доступних провайдерів Enchant з їх даними.

### Список змін

| Версія | Опис                                                                                                                               |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| 8.0.0  | broker чекає екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md)). |
| 8.0.0  | До цієї версії функція повертала **false** у разі виникнення помилки.                                                              |

### Приклади

**Приклад #1 Список бекендів, що надаються конкретним брокером**

` <?php$r = enchant_broker_init();$bprovides = enchant_broker_describe($r);echo "Брокер надає наступні бекенди:
";print_r($bprovides);?> `

Результатом виконання цього прикладу буде щось подібне:

Брокер надає такі бекенди:
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
