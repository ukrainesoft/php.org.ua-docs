---
navigation:
  - function.enchant-broker-list-dicts.md: « enchant\_broker\_list\_dicts
  - function.enchant-broker-request-pwl-dict.md: enchant\_broker\_request\_pwl\_dict »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_broker\_request\_dict
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_broker\_request\_dict

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_broker\_request\_dict — Створити новий словник, використовуючи тег

### Опис

```methodsynopsis
enchant_broker_request_dict(EnchantBroker $broker, string $tag): EnchantDictionary|false
```

Створює новий словник, використовуючи не порожній мовний тег ("en\_US", "ru\_RU", ...)

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.md)

`tag`

Тег опису локалі, наприклад en\_US, ru\_RU

### Значення, що повертаються

Повертає ресурс словника у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**enchant\_broker\_request\_dict()\*\*\*\*

Перевіряємо, чи існує словник за допомогою [enchant\_broker\_dict\_exists()](function.enchant-broker-dict-exists.md) і потім запитуємо його.

```php
<?php
$tag = 'en_US';
$broker = enchant_broker_init();
if (enchant_broker_dict_exists($broker,$tag)) {
    $dict = enchant_broker_request_dict($r, $tag);
}
?>
```

### Дивіться також

-   [enchant\_dict\_describe()](function.enchant-dict-describe.md) \- Повертає інформацію про словник
-   [enchant\_broker\_dict\_exists()](function.enchant-broker-dict-exists.md) \- Перевіряє, чи є словник чи ні. Використовується не пустий тег
-   [enchant\_broker\_free\_dict()](function.enchant-broker-free-dict.md) \- звільняє ресурс словника
