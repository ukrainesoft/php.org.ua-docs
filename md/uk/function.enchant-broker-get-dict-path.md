Повертає шлях словника для заданого бекенду

-   [« enchant\_broker\_free](function.enchant-broker-free.html)
    
-   [enchant\_broker\_get\_error »](function.enchant-broker-get-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Повертає шлях словника для заданого бекенду
    

# enchantbrokergetdictpath

(PHP 5 >= 5.3.1, PHP 7, PHP 8, PECL enchant >= 1.0.1)

enchantbrokergetdictpath — Повертає шлях словника для заданого бекенду

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
enchant_broker_get_dict_path(EnchantBroker $broker, int $type): string|false
```

Повертає шлях словника для заданого бекенда.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.html)

`type`

Тип словників, тобто . **`ENCHANT_MYSPELL`** або **`ENCHANT_ISPELL`**

### Значення, що повертаються

Повертає шлях до директорії словника у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |

### Примітки

> **Зауваження**
> 
> Функція доступна, тільки якщо модуль був скомпільований з Enchant v1.

### Дивіться також

-   [enchant\_broker\_set\_dict\_path()](function.enchant-broker-set-dict-path.html) - Встановити шлях для заданого бекенду