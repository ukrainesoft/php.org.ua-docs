---
navigation:
  - function.enchant-broker-list-dicts.md: « enchantbrokerlistdicts
  - function.enchant-broker-request-pwl-dict.md: enchantbrokerrequestpwldict »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantbrokerrequestdict
---
# enchantbrokerrequestdict

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantbrokerrequestdict — Створити новий словник, використовуючи тег

### Опис

```methodsynopsis
enchant_broker_request_dict(EnchantBroker $broker, string $tag): EnchantDictionary|false
```

Створює новий словник, використовуючи не порожній мовний тег ("enUS", "ruRU", ...)

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.md)

`tag`

Тег опису локалі, наприклад enUS, ruРУ

### Значення, що повертаються

Повертає ресурс словника у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | У разі успішного виконання функція повертає екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **enchantbrokerrequestdict()****

Перевіряємо, чи існує словник за допомогою [enchantbrokerdictexists()](function.enchant-broker-dict-exists.md) і потім запитуємо його.

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

-   [enchantdictdescribe()](function.enchant-dict-describe.md) - Повертає інформацію про словник
-   [enchantbrokerdictexists()](function.enchant-broker-dict-exists.md) - Перевіряє, чи є словник чи ні. Використовується не пустий тег
-   [enchantbrokerfreedict()](function.enchant-broker-free-dict.md) - звільняє ресурс словника
