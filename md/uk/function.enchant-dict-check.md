Перевіряє, чи правильно задано слово

-   [« enchantdictadd](function.enchant-dict-add.html)
    
-   [enchantdictdescribe »](function.enchant-dict-describe.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Enchant](ref.enchant.md)
    
-   Перевіряє, чи правильно задано слово
    

# enchantdictcheck

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantdictcheck — Перевіряє, чи правильно задано слово

### Опис

```methodsynopsis
enchant_dict_check(EnchantDictionary $dictionary, string $word): bool
```

Повертає **`true`**, якщо слово написано без помилок або \*\*`false`\*\*якщо з помилками.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.html)

`word`

Слово для перевірки

### Значення, що повертаються

Повертає **`true`**, якщо слово написано без помилок або \*\*`false`\*\*якщо з помилками.

### список змін

| Версия | Описание                                                                                                                                          |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |