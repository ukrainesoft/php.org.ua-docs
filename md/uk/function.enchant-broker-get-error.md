---
navigation:
  - function.enchant-broker-get-dict-path.md: « enchant\_broker\_get\_dict\_path
  - function.enchant-broker-init.md: enchant\_broker\_init »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_broker\_get\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_broker\_get\_error

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_broker\_get\_error — Повертає останню помилку брокера

### Опис

```methodsynopsis
enchant_broker_get_error(EnchantBroker $broker): string|false
```

Повертає останню помилку на брокері.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.md)

### Значення, що повертаються

Повертає рядок з помилкою, якщо такий був, або **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
