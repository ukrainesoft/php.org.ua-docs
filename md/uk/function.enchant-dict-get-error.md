Повертає останню помилку поточної сесії перевірки

-   [« enchant\_dict\_describe](function.enchant-dict-describe.html)
    
-   [enchant\_dict\_is\_added »](function.enchant-dict-is-added.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Повертає останню помилку поточної сесії перевірки
    

# enchantdictgeterror

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantdictgeterror — Повертає останню помилку поточної сесії перевірки

### Опис

```methodsynopsis
enchant_dict_get_error(EnchantDictionary $dictionary): string|false
```

Повертає останню помилку поточної сесії перевірки.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.html) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.html)

### Значення, що повертаються

Повертає рядок з помилкою або **`false`**якщо такої немає.

### список змін

| Версия | Описание                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |