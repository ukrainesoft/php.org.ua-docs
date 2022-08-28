Звільняє ресурс брокера та його словники

-   [« enchant\_broker\_free\_dict](function.enchant-broker-free-dict.html)
    
-   [enchant\_broker\_get\_dict\_path »](function.enchant-broker-get-dict-path.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Звільняє ресурс брокера та його словники
    

# enchantbrokerfree

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantbrokerfree — Звільняє ресурс брокера та його словники

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
enchant_broker_free(EnchantBroker $broker): bool
```

Звільняє брокера з його словниками. Починаючи з PHP 8.0.0, рекомендується знищити об'єкт замість виклику цієї функції.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                  |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
|        | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [enchant\_broker\_init()](function.enchant-broker-init.html) - Створити новий об'єкт брокера