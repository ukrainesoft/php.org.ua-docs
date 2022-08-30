Визначає, чи існує слово у цій орфографічній сесії

-   [« enchantdictgeterror](function.enchant-dict-get-error.html)
    
-   [enchantdictісінsession »](function.enchant-dict-is-in-session.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Визначає, чи існує слово у цій орфографічній сесії
    

# enchantdictісadded

(PHP 8)

enchantdictісadded - Визначає, чи існує слово в цій орфографічній сесії

### Опис

```methodsynopsis
enchant_dict_is_added(EnchantDictionary $dictionary, string $word): bool
```

Визначає, чи вже існує слово в поточній сесії.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.html)

`word`

Слово для пошуку

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо слово вже існує, інакше повертає **`false`**

### список змін

| Версия | Описание                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [enchantdictaddтоsession()](function.enchant-dict-add-to-session.html) - Додати слово у поточну сесію перевірки