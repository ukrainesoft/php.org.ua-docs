Перевіряє, чи є словник чи ні. Використовується не пустий тег

-   [« enchant\_broker\_describe](function.enchant-broker-describe.html)
    
-   [enchant\_broker\_free\_dict »](function.enchant-broker-free-dict.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Перевіряє, чи є словник чи ні. Використовується не пустий тег
    

# enchantbrokerdictexists

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantbrokerdictexists — Перевіряє, чи присутній словник. Використовується не пустий тег

### Опис

```methodsynopsis
enchant_broker_dict_exists(EnchantBroker $broker, string $tag): bool
```

Перевіряє, чи присутній словник чи ні використовуючи не порожній тег

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.html)

`tag`

Не порожній тег у форматі LOCALE, тобто: usUS, chDE і т.д.

### Значення, що повертаються

Повертає **`true`** або **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **enchantbrokerdictexists()****

```php
<?php
$tag = 'en_US';
$r = enchant_broker_init();
if (enchant_broker_dict_exists($r,$tag)) {
    echo $tag . " словарь найден.\n";
}
?>
```

### Дивіться також

-   [enchant\_broker\_describe()](function.enchant-broker-describe.html) - Перераховує провайдерів Enchant