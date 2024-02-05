---
navigation:
  - function.enchant-broker-describe.md: « enchant\_broker\_describe
  - function.enchant-broker-free-dict.md: enchant\_broker\_free\_dict »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_broker\_dict\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_broker\_dict\_exists

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_broker\_dict\_exists — Перевіряє, чи присутній словник. Використовується не пустий тег

### Опис

```methodsynopsis
enchant_broker_dict_exists(EnchantBroker $broker, string $tag): bool
```

Перевіряє, чи є словник чи ні використовуючи не порожній тег

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.md)

`tag`

Не порожній тег у форматі LOCALE, тобто: us\_US, ch\_DE і т.д.

### Значення, що повертаються

Повертає **`true`**или**`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**enchant\_broker\_dict\_exists()\*\*\*\*

```php
<?php
$tag = 'en_US';
$r = enchant_broker_init();
if (enchant_broker_dict_exists($r,$tag)) {
    echo $tag . " словарь найден.\n";
}
?>
```

### Дивіться також

-   [enchant\_broker\_describe()](function.enchant-broker-describe.md) \- Перераховує провайдерів Enchant
