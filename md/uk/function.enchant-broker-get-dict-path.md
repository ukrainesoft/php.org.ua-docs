---
navigation:
  - function.enchant-broker-free.md: « enchantbrokerfree
  - function.enchant-broker-get-error.md: enchantbrokergeterror »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantbrokergetdictpath
---
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

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.md)

`type`

Тип словників, тобто . **`ENCHANT_MYSPELL`** або **`ENCHANT_ISPELL`**

### Значення, що повертаються

Повертає шлях до директорії словника у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Примітки

> **Зауваження**
> 
> Функція доступна, тільки якщо модуль був скомпільований з Enchant v1.

### Дивіться також

-   [enchantbrokersetdictpath()](function.enchant-broker-set-dict-path.md) - Встановити шлях для заданого бекенду
