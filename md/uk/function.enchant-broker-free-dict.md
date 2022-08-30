Визволяє ресурс словника

-   [« enchantbrokerdictexists](function.enchant-broker-dict-exists.html)
    
-   [enchantbrokerfree »](function.enchant-broker-free.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Визволяє ресурс словника
    

# enchantbrokerfreedict

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantbrokerfreedict - Звільняє ресурс словника

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
enchant_broker_free_dict(EnchantDictionary $dictionary): bool
```

Звільняє словник. Починаючи з PHP 8.0.0, рекомендується знищити об'єкт замість виклику цієї функції.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                 |
|--------|------------------------------------------------------------------------------------------------------------------------------------------|
|        | `dictionary` чекає [EnchantDictionary](class.enchantdictionary.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) - Створити новий словник, використовуючи тег
-   [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.html) - Створити словник, використовуючи файл PWL