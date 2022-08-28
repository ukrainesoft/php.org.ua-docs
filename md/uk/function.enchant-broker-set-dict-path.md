Встановити шлях для заданого бекенду

-   [« enchant\_broker\_request\_pwl\_dict](function.enchant-broker-request-pwl-dict.html)
    
-   [enchant\_broker\_set\_ordering »](function.enchant-broker-set-ordering.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Встановити шлях для заданого бекенду
    

# enchantbrokersetdictpath

(PHP 5 >= 5.3.1, PHP 7, PHP 8, PECL enchant >= 1.0.1)

enchantbrokersetdictpath — Встановити шлях для заданого бекенду

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
enchant_broker_set_dict_path(EnchantBroker $broker, int $type, string $path): bool
```

Встановити шлях для заданого бекенда.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.html)

`type`

Тип словників, тобто . **`ENCHANT_MYSPELL`** або **`ENCHANT_ISPELL`**

`path`

Шлях до директорії зі словниками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |

### Примітки

> **Зауваження**
> 
> Функція доступна, тільки якщо модуль був скомпільований з Enchant v1.

### Дивіться також

-   [enchant\_broker\_get\_dict\_path()](function.enchant-broker-get-dict-path.html) - Повертає шлях словника для заданого бекенду