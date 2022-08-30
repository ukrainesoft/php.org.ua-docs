Перевіряє, чи є словник чи ні. Використовується не пустий тег

-   [« enchantbrokerdescribe](function.enchant-broker-describe.html)
    
-   [enchantbrokerfreedict »](function.enchant-broker-free-dict.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Enchant](ref.enchant.md)
    
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

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.html)

`tag`

Не порожній тег у форматі LOCALE, тобто: usUS, chDE і т.д.

### Значення, що повертаються

Повертає **`true`** або **`false`**

### список змін

| Версия | Описание                                                                                                                              |
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
|        | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

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

-   [enchantbrokerdescribe()](function.enchant-broker-describe.html) - Перераховує провайдерів Enchant