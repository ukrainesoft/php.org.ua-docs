---
navigation:
  - function.enchant-broker-request-pwl-dict.html: « enchantbrokerrequestpwldict
  - function.enchant-broker-set-ordering.html: enchantbrokersetordering »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantbrokersetdictpath
---
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

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.md)

`type`

Тип словників, тобто . **`ENCHANT_MYSPELL`** або **`ENCHANT_ISPELL`**

`path`

Шлях до директорії зі словниками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Примітки

> **Зауваження**
> 
> Функція доступна, тільки якщо модуль був скомпільований з Enchant v1.

### Дивіться також

-   [enchantbrokergetdictpath()](function.enchant-broker-get-dict-path.md) - Повертає шлях словника для заданого бекенду
