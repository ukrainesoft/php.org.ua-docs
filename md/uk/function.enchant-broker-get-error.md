Повертає останню помилку брокера

-   [« enchantbrokergetdictpath](function.enchant-broker-get-dict-path.html)
    
-   [enchantbrokerinit »](function.enchant-broker-init.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Повертає останню помилку брокера
    

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

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.html)

### Значення, що повертаються

Повертає рядок з помилкою, якщо такий був, або **`false`**

### список змін

| Версия | Описание                                                                                                                                  |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
|        | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |