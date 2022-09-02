---
navigation:
  - function.enchant-broker-request-dict.md: « enchantbrokerrequestdict
  - function.enchant-broker-set-dict-path.md: enchantbrokersetdictpath »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantbrokerrequestpwldict
---
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

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.md)

`filename`

Шлях до PWL-файлу. Якщо файл відсутній, буде створено новий з таким ім'ям, якщо можливо.

### Значення, що повертаються

Повертає ресурс словника у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | У разі успішного виконання функція повертає екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше повертався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [enchantdictdescribe()](function.enchant-dict-describe.md) - Повертає інформацію про словник
-   [enchantbrokerdictexists()](function.enchant-broker-dict-exists.md) - Перевіряє, чи є словник чи ні. Використовується не пустий тег
-   [enchantbrokerfreedict()](function.enchant-broker-free-dict.md) - звільняє ресурс словника
