---
navigation:
  - function.enchant-broker-request-dict.md: « enchant\_broker\_request\_dict
  - function.enchant-broker-set-dict-path.md: enchant\_broker\_set\_dict\_path »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_broker\_request\_pwl\_dict
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_broker\_request\_pwl\_dict

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_broker\_request\_pwl\_dict — Створити словник, використовуючи файл PWL

### Опис

```methodsynopsis
enchant_broker_request_pwl_dict(EnchantBroker $broker, string $filename): EnchantDictionary|false
```

Створює словник, використовуючи файл PWL. Файл PWL - це файл користувача зі словами, за одним словом на рядок.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.md)

`filename`

Шлях до PWL-файлу. Якщо файл відсутній, буде створено новий з таким ім'ям, якщо можливо.

### Значення, що повертаються

Повертає ресурс словника у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше повертався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchant\_dict\_describe()](function.enchant-dict-describe.md) \- Повертає інформацію про словник
-   [enchant\_broker\_dict\_exists()](function.enchant-broker-dict-exists.md) \- Перевіряє, чи є словник чи ні. Використовується не пустий тег
-   [enchant\_broker\_free\_dict()](function.enchant-broker-free-dict.md) \- звільняє ресурс словника
