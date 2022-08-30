Повертає останню помилку поточної сесії перевірки

-   [« enchantdictdescribe](function.enchant-dict-describe.html)
    
-   [enchantdictісadded »](function.enchant-dict-is-added.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Enchant](ref.enchant.md)
    
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

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.html)

### Значення, що повертаються

Повертає рядок з помилкою або \*\*`false`\*\*якщо такої немає.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |