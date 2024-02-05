---
navigation:
  - function.enchant-broker-free.md: « enchant\_broker\_free
  - function.enchant-broker-get-error.md: enchant\_broker\_get\_error »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_broker\_get\_dict\_path
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_broker\_get\_dict\_path

(PHP 5 >= 5.3.1, PHP 7, PHP 8, PECL enchant >= 1.0.1)

enchant\_broker\_get\_dict\_path — Повертає шлях словника для заданого бекенду

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
enchant_broker_get_dict_path(EnchantBroker $broker, int $type): string|false
```

Повертає шлях словника для заданого бекенда.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.md)

`type`

Тип словників, тобто . **`ENCHANT_MYSPELL`** або **`ENCHANT_ISPELL`**

### Значення, що повертаються

Повертає шлях до директорії словника у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Примітки

> **Зауваження** :
> 
> Функція доступна, тільки якщо модуль був скомпільований з Enchant v1.

### Дивіться також

-   [enchant\_broker\_set\_dict\_path()](function.enchant-broker-set-dict-path.md) \- Встановити шлях для заданого бекенду
