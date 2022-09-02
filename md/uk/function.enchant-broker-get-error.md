---
navigation:
  - function.enchant-broker-get-dict-path.md: « enchantbrokergetdictpath
  - function.enchant-broker-init.md: enchantbrokerinit »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantbrokergeterror
---
# enchantbrokergeterror

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantbrokergeterror — Повертає останню помилку брокера

### Опис

```methodsynopsis
enchant_broker_get_error(EnchantBroker $broker): string|false
```

Повертає останню помилку на брокері.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.md)

### Значення, що повертаються

Повертає рядок з помилкою, якщо такий був, або **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
