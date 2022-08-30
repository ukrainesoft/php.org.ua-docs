Створити новий словник, використовуючи тег

-   [« enchantbrokerlistdicts](function.enchant-broker-list-dicts.html)
    
-   [enchantbrokerrequestpwldict »](function.enchant-broker-request-pwl-dict.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Створити новий словник, використовуючи тег
    

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

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.html)

`tag`

Тег опису локалі, наприклад enUS, ruРУ

### Значення, що повертаються

Повертає ресурс словника у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                    |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.html); Раніше очікувався ресурс ([resource](language.types.resource.html)                                   |
|        | У разі успішного виконання функція повертає екземпляр [EnchantDictionary](class.enchantdictionary.html); Раніше повертався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **enchantbrokerrequestdict()****

Перевіряємо, чи існує словник за допомогою [enchantbrokerdictexists()](function.enchant-broker-dict-exists.html) і потім запитуємо його.

```php
<?php
$tag = 'en_US';
$broker = enchant_broker_init();
if (enchant_broker_dict_exists($broker,$tag)) {
    $dict = enchant_broker_request_dict($r, $tag);
}
?>
```

### Дивіться також

-   [enchantdictdescribe()](function.enchant-dict-describe.html) - Повертає інформацію про словник
-   [enchantbrokerdictexists()](function.enchant-broker-dict-exists.html) - Перевіряє, чи є словник чи ні. Використовується не пустий тег
-   [enchantbrokerfreedict()](function.enchant-broker-free-dict.html) - звільняє ресурс словника