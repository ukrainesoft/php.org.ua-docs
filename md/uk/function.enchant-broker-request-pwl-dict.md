Створити словник, використовуючи файл PWL

-   [« enchantbrokerrequestdict](function.enchant-broker-request-dict.html)
    
-   [enchantbrokersetdictpath »](function.enchant-broker-set-dict-path.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Створити словник, використовуючи файл PWL
    

# enchantbrokerrequestpwldict

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantbrokerrequestpwldict — Створити словник, використовуючи файл PWL

### Опис

```methodsynopsis
enchant_broker_request_pwl_dict(EnchantBroker $broker, string $filename): EnchantDictionary|false
```

Створює словник, використовуючи файл PWL. Файл PWL - це файл користувача зі словами, за одним словом на рядок.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.html)

`filename`

Шлях до PWL-файлу. Якщо файл відсутній, буде створено новий з таким ім'ям, якщо можливо.

### Значення, що повертаються

Повертає ресурс словника у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | У разі успішного виконання функція повертає екземпляр [EnchantDictionary](class.enchantdictionary.html); Раніше повертався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [enchantdictdescribe()](function.enchant-dict-describe.html) - Повертає інформацію про словник
-   [enchantbrokerdictexists()](function.enchant-broker-dict-exists.html) - Перевіряє, чи є словник чи ні. Використовується не пустий тег
-   [enchantbrokerfreedict()](function.enchant-broker-free-dict.html) - звільняє ресурс словника